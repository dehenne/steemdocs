<h1>Create a little Python program to view raw block data from the Steem blockchain</h1> 


<p>In this tutorial I'll be showing you how to create a little graphical program to view the raw data of a block on the STEEM blockchain using the <a href="http://steem.readthedocs.io/en/latest/" rel="nofollow noopener">steem-python</a> library and Tkinter which is Pythons most popular GUI (Graphical User Interface) toolkit. Our little program won't be the most beautiful program out there but hopefully it will show you how you could implement the steem-python library into your own programs and if you're new to Tkinter you'll learn something useful as well. When we're done our little program should look like this:</p>
<p><img src="https://steemitimages.com/0x0/https://steemitimages.com/DQmYabYDxfrVskrGpK4p3hswq3b1t8GkdZZMpiRSzCr5akd/blockviewer.png" alt="blockviewer.png" /></p>
<p>Awesome! Lets get started. It's generally bad to make assumptions but I'll be making the following ones before we start:</p>
<ol>
<li><p>You have at least Python version 3.5</p></li>
<li><p>You're in your virtual environment where you installed the steem-python library. You can get the steem-python library by running the following command: <code>pip install steem</code> .If you're sitting there thinking &quot;The F#ck is that???&quot; then please go read my previous <a href="https://steemit.com/steemdev/@benniebanana/creating-your-first-program-on-the-steemit-network-using-steem-python-beginnermode-tutorial">post</a>.</p></li>
</ol>
<p>Cool let's start by opening up a blank file in our favourite text editor, I'll be using Notepadqq and I'll call my program blockviewer.py:</p>
<pre><code>$ notepadqq blockviewer.py
</code></pre>
<p>Now we can start coding so lets start with our imports. We need to import Steem, tkinter and json so lets add the following lines to our file:</p>
<pre><code>from tkinter import *
from steem import Steem
import json
</code></pre>
<p>Now we create our instances so we'll add the following:</p>
<pre><code>s = Steem()
root = Tk()
</code></pre>
<p>and we'll set the dimensions of our little gui by adding:</p>
<pre><code>root.geometry('800x400')
</code></pre>
<p>Lets add in the function that will do all the work. The function will be triggered when the button is pressed and will get our input, retrieve the block information based on our input, format the data to make it a little more readable and then spit it out into our output box so that we can have a look at it. So let's add in our function:</p>
<pre><code>def buttonPress():
    text = Entry.get(textInput)
    data = s.get_block(text)
    formatteddata = json.dumps(data, indent=4, sort_keys= True)
    textOutput.delete('1.0', END)
    textOutput.insert(END, formatteddata)
</code></pre>
<p>Each line of our function explained:</p>
<p><strong>line 1:</strong> We define our function<br />
<strong>line 2:</strong> We get the users input<br />
<strong>line 3:</strong> We pass the input to  the<code>get_block()</code> method from the steem-python library to retrieve the block information<br />
<strong>line 4:</strong> We format the retrieved data to make it more readable<br />
<strong>line 5:</strong> We clear our output box in case there's some text in there from previous retrievals<br />
<strong>line 6:</strong> We add our block information to the output box so we can see it.</p>
<p>Lets create our input, output and add them to our gui:</p>
<pre><code>textInput = Entry(root)
textInput.pack()

textOutput = Text(root,width = 300)
textOutput.pack()
</code></pre>
<p>We can also add in our button and assign our created function to the button so the function will be triggered when the button is pressed:</p>
<pre><code>button = Button(root, height = 1, width = 10, text = &quot;Get STEEM Block&quot;, command=lambda : buttonPress()).pack()
</code></pre>
<p>And finally we can add our last line of code so that our gui would actually work:</p>
<pre><code>root.mainloop()
</code></pre>
<p>Your file should hopefully look like this by now:</p>
<p><img src="https://steemitimages.com/0x0/https://steemitimages.com/DQmfHWdCKZyB3F7gjo9NkgFfdC7xhcFSs4HKS7mwSYWJfxh/preview.png" alt="preview.png" /></p>
<p>Cool! Save your file, exit and run your file:</p>
<pre><code>$ python blockviewer.py 
</code></pre>
<p>We should see our gui pop up(hopefully):</p>
<p><img src="https://steemitimages.com/0x0/https://steemitimages.com/DQmSQScveDKsahxLjHQgVsDhaQXCqn7iALewV9HQFyzoqCC/gui1.png" alt="gui1.png" /></p>
<p>Now lets get all the block information for block 8888888 so lets type that into our input field:</p>
<p><img src="https://steemitimages.com/0x0/https://steemitimages.com/DQmQ9w2RsRXZY2bi14CD3BJcEqedcN7pGPrtaTcsDqzHMwR/gui2.png" alt="gui2.png" /></p>
<p>Press the button and we should get the following output:</p>
<p><img src="https://steemitimages.com/0x0/https://steemitimages.com/DQmYCpfeFgFv5gAXdwHRthorxJ3QRqwNgoUDWJyybCfvwN3/gui3.png" alt="gui3.png" /></p>
<p>Awesome! It's not pretty but it's something and now you have an idea of some of  the data contained in a block withing the blockchain. We can dissect the block to get data such as the time the block was added, the witness and the witness signature of the specific block. If the block was a comment such as this one then we can get information such as the author, the body of the comment and the link to the comment.</p>
<p>You can get the block information for a very very very wide range of block numbers so feel free to try out a few numbers and see what you get. I made this tutorial with the purpose of showing you some of the ways that we can implement the steem-python library into little apps to get information about steem and the network. The library contains tons of other cool methods which allows us to interface with Steemit to do cool things. Be sure to go check out the documentation linked at the top of this post for more information.</p>
