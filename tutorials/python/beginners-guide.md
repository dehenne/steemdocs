# Setting up your Python development environment in Ubuntu 

In order to use steem-python we need to have at least Python version 3.5 or higher.

## Checking your Python version

````$ python3 -V ````

Which should give you an output similar to this:

```` $ Python 3.5.2````

Your version number might be different but as long as we have version 3.5 or higher we're good to go. If you get an error or your version is lower than 3.5 then you'll need to get the correct version first before continuing. 

## Installing pip

Next we'll be installing pip which we'll use later to install the steem-python library. 

 ````$ apt-get install -y python3-pip ```` 

The -y flag just means that we automatically agree to all the things that need to be installed. Pip can be used to install packages or libraries with the following command: 

```` $ pip3 install package_name````

Now we need to install some extra packages in order to create a nice robust programming environment: 

## Installing essential packages

```` $ sudo apt-get install build-essential libssl-dev libffi-dev python-dev ````

## Creating our virtual environment

Now we'll be setting up our virtual environment where we'll be playing around with the steem-python library. A virtual environment will allow us to develop our programs in an isolated safe space where we can play around in and brake things without breaking the things outside of the environment. You can have as many virtual environments as you want. We can install the virtual environment module with the following command: 

```` $ sudo apt-get install -y python3-venv````

Now that we have the module installed we can start creating our virtual environment. Navigate to the folder where you would like to keep all your environments, I'll be keeping mine in my Documents folder so I'll be navigating there with the following command: 

````$ cd Documents/  ````


Now we'll create our folder where we'll be keeping our virtual environments. I'll be naming mine "environments" but you can name it whatever you want, just remember what you named it: 

````$ mkdir environments````

Now we need to navigate into our created folder: 

````$ cd environments```` 

Now we can create our virtual environment in here with the following command. I'll be naming mine "steemit_env": 

```` $ python3 -m venv steemit_env ```` 

Now that we have created our virtual environment we can run the following command to get the contents of our environment: 

````$ ls steemit_env ````

and we should get the following output: 

```` bin include lib lib64 pyvenv.cfg share ```` 

In order to use our environment we need to activate it first so that Python knows which environment we're using: 

```` $ source steemit_env/bin/activate````

your command line should look similar to this after activating your environment: 

````
(steemit_env) root@BennieBanana-TheBestLaptop:~/Documents/environments# 
 ````
## Testing your virtual environment

Sweet! Our virtual environment is set up and activated so we can start playing around. The prefix "(steemit_env)" means that we're currently using our created virtual environment. Lets create a little demo program to test out our virtual environment. I'll be using Notepadqq which you can get by running the following commands: 

````
$ sudo add-apt-repository ppa:notepadqq-team/notepadqq
$ sudo apt-get update
$ sudo apt-get install notepadqq
````

or you can use gedit or nano which comes packed with Ubuntu by default. Open up a new python file in your editor of choice by running the following command. I'll be calling mine "steemit.py": 

````$ notepaddqq steemit.py ````  

Now that we have our file opened up we can start coding. Add in the following line to the file: 

```` print("Steemit is Awesome!")````

Save it and close it. We can now check if everything is working properly by running our program with the following command:

````$ python steemit.py ```` 

and we should get the following output: 

````$ Steemit is Awesome! ````

# Setting up Steem-Python with an example 

Lets install the steem-python library using pip: 

```` $ pip install steem````

Once the library is installed we can create a new file where we will be playing. I'll be opening the previous file we created and I'll delete the print statement so that we can have a blank file to work with: 

````$ notepadqq steemit.py ````

The first line we need to add to our file will be our import statement: 

```` from steem import Steem ````

The second line we need to add is our instance of Steem where we will be adding in our private posting key as well as our private active keys: 

```` s = Steem(keys='your-private-posting-key', 'your-private-active-key') ````

You can get your private posting and active keys by going to your Wallet on Steemit, clicking on Permissions and then clicking on "SHOW PRIVATE KEY" next to your posting and active keys. 

![keys.png](https://steemitimages.com/DQmbK5BpvcckpRKV9dfLDedYYE1VduSQTr2seyYPY9AxEy5/keys.png)

Now we can start doing cool stuff with the library. Our first little experiment will be to upvote a post by adding the following lines to our file: 

```` 
s.vote('@benniebanana/creating-your-first-program-on-the-steemit-network-using-steem-python-beginnermode-tutorial', 100.0)
print('Yay we just upvoted Bennies post!')
 ````
Your file should look this by now: 

![lastTry.png](https://steemitimages.com/DQmSy3CkLjZybk8nN6CuiMPigy9xzdjUMAyhGPzdtaRAXXa/lastTry.png) 

The first argument is the posts identifier and the second is the weight at which we would like to vote. Save the file, exit and run the program with the following command: 

````$ python steemit.py````

we should get the following output: 

````$ Yay we just upvoted Bennies post!````

Well done! You just wrote your first little program using the steem-python library!

Our next little experiment will be to resteem a post. First we have to remove or comment out the s.vote... statement since we can't upvote the same post twice. We'll comment out the vote and print statement and replace them with the following: 

````
s.resteem('@benniebanana/creating-your-first-program-on-the-steemit-network-using-steem-python-beginnermode-tutorial')
print('Yay we just resteemed Bennies post!') 
````

Save, exit and run your file like you did previously and you should get the following output: 

```` Yay we just resteemed Bennies post!````

These are just two methods from the steem-python library that you can use. The library contains lots and lots of other cool methods which you can use in your programs.

You can visit their site for the full <a href="http://steem.readthedocs.io/en/latest/index.html">documentation</a>

