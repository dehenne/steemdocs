# getState

Returns the posts for a given tag/category.

**Arguments**

`name` String - Path for the category. \('created', 'created/steem'\)

```
steem.api.getState(path, function(err, result) {
  console.log(err, result);
});
```

**Response**

```
{
  "id": 1,
  "result": {
    "current_route": "created",
    "props": {
      "id": 0,
      "head_block_number": 12379153,
      "head_block_id": "00bce411bf2d255ecf8f5edf079226c2ebb1350a",
      "time": "2017-05-30T10:23:48",
      "current_witness": "clayop",
      "total_pow": 514415,
      "num_pow_witnesses": 172,
      "virtual_supply": "251204037.060 STEEM",
      "current_supply": "249751654.171 STEEM",
      "confidential_supply": "0.000 STEEM",
      "current_sbd_supply": "1368144.682 SBD",
      "confidential_sbd_supply": "0.000 SBD",
      "total_vesting_fund_steem": "178613324.070 STEEM",
      "total_vesting_shares": "370147659880.253369 VESTS",
      "total_reward_fund_steem": "0.000 STEEM",
      "total_reward_shares2": "0",
      "pending_rewarded_vesting_shares": "113189619.701268 VESTS",
      "pending_rewarded_vesting_steem": "54585.058 STEEM",
      "sbd_interest_rate": 0,
      "sbd_print_rate": 10000,
      "average_block_size": 2567,
      "maximum_block_size": 65536,
      "current_aslot": 12434876,
      "recent_slots_filled": "340282366920938463463374607431768211455",
      "participation_count": 128,
      "last_irreversible_block_num": 12379134,
      "max_virtual_bandwidth": "5986734968066277376",
      "current_reserve_ratio": 20000,
      "vote_regeneration_per_day": 40
    },
    "category_idx": {
      "active": [],
      "recent": [],
      "best": []
    },
    "tag_idx": {
      "trending": ["life", "", "steemit", "introduceyourself", "steem", "story", "blog", "steemsquad", "art", "travel", "writing", "minnowsunite", "news", "photography", "health", "creativity", "cryptocurrency", "nature", "history", "funny", "money", "introduction", "filmmaker", "philosophy", "mining", "steemitphotochallenge", "sports", "benutzererfahrung-gegen-sicherhe", "steemjs", "cn", "howto", "beyondbitcoin", "tutorials", "community", "bitcoin", "food", "crowdsourcing", "real", "estate", "motors", "steemtofiat", "blockchain", "politics", "video", "freedom", "steemthought", "beauty", "ethereum", "ecommerce", "science"]
    },
    "categories": {},
    "tags": {},
    "content": {
      "abh12345/graffiti-admiration-in-valencia-spain": {
        "id": 3199334,
        "author": "abh12345",
        "permlink": "graffiti-admiration-in-valencia-spain",
        "category": "graffiti",
        "parent_author": "",
        "parent_permlink": "graffiti",
        "title": "Graffiti admiration in Valencia, Spain",
        "body": "The city of Valencia is my current home, summer is just around the corner and oh man it gets pretty hot on the east coast of Spain.  The heat however will not keep me off my bike, the city is as flat as a pancake and filled with cycle routes which means you can get around and explore without too much effort; you can ask me next month if this is still true!\n\n![header.jpg](https://steemitimages.com/DQmWWCMyJweeqWzpsx6AgbxoaAiLpJYEcCQqdMtdtPQxj87/header.jpg)\n\nOn my adventures around the city, I’ve noticed they are rather liberal when it comes to Graffiti and this is the context of my Blog today.  In the UK, Graffiti is for the most part seen as a nuisance and vandalism, but here it’s almost embraced and the *artists are respectful in the surfaces they choose to display their skills.*\n\n**So without further ado, here’s what I’ve found so far...**\n\n**A Veterinary Clinic**\n![IMG_8050.JPG](https://steemitimages.com/DQmQR73m2rXheRzb1Ncg8EBX3mhTzkko6rj71ZTWG8hUuKv/IMG_8050.JPG)\n\n**Underground Car Park**\n![IMG_8",
        "json_metadata": "{\"tags\":[\"graffiti\",\"art\",\"valencia\",\"drawing\",\"photography\"],\"image\":[\"https://steemitimages.com/DQmWWCMyJweeqWzpsx6AgbxoaAiLpJYEcCQqdMtdtPQxj87/header.jpg\",\"https://steemitimages.com/DQmQR73m2rXheRzb1Ncg8EBX3mhTzkko6rj71ZTWG8hUuKv/IMG_8050.JPG\",\"https://steemitimages.com/DQmZ2qFfXNXQTpPbFsko5bEd9PxE5Qmi1ofjvxjUwpXqHA3/IMG_8049.JPG\",\"https://steemitimages.com/DQmP5pDzU8keBXG5uEDxPKJaGQegg8vWs4KaSQNu4CcoaR8/IMG_8071.JPG\",\"https://steemitimages.com/DQmTNdJsqZ1a8xgcrms764JGTk4N1QM3HFDcfnHXFJ55wwH/IMG_8075.JPG\",\"https://steemitimages.com/DQmRnAwFApxVzNsekytfaxcn9ZGVkbvrWWKJ7boEGMeh2fV/IMG_8080.JPG\",\"https://steemitimages.com/DQmR7djkMRfwrGPuy8HoND65dndX11hy3h4VnLfqAiHgfBY/IMG_8081.JPG\",\"https://steemitimages.com/DQmXzW1oBfSo675Ps75hbav5YDsfWFG9LZPvRQgvLx8TFYE/IMG_8079.JPG\",\"https://steemitimages.com/DQmSDuqRDAtqtmDq8Z9VAYu4uGtp4zKmyLqysgP6m2paBuz/IMG_8078.JPG\",\"https://steemitimages.com/DQmdAUPwj2Kykmv9Vx4n7KLrQDWxaYjGeouCurWCbCDFksM/IMG_8077.JPG\",\"https://steemitimages.com/DQmZTq4E6wCnRH6HktnCNDaaR3wmBNJqW6Ks3fMKvxBUYCa/IMG_8069.JPG\",\"https://steemitimages.com/DQmeZeQU1AYHEXPzyUPf4nwcNRptBXsgxo9q8uW3BFCQj1Z/IMG_8082.JPG\",\"https://steemitimages.com/DQmS75Q5HW2G7zLBKqDkvQ8XGgNhg9BuboXzfuB4hwd1LUJ/IMG_8076.JPG\",\"https://steemitimages.com/DQmaxpZuRXmLyJ3xAHMJPs2edyqKb1kCBdufoSnZucsM81i/IMG_8060.JPG\",\"https://steemitimages.com/DQmRyPUBMk1ssEWJSQPdwP1Q8r2ez4fTAo9xmCSB9QTTLwq/IMG_8065.JPG\",\"https://steemitimages.com/DQme8WHFcqGeC9DJazxoH3LcA4mWR8j4d9WwC4fbxUtJBEw/IMG_8072.JPG\",\"https://steemitimages.com/DQmNv2LoGbjTYDuLndymSR7pkNoLx7GwTYqAYE949sQeUTL/IMG_8073.JPG\",\"https://steemitimages.com/DQmcn5PDKabXAYwE2VUqY9DZRFXBSpGYbwr5cuT5EFnjQVK/IMG_8058.JPG\",\"https://steemitimages.com/DQmf2W36mGBZ4NodXSXznFMHx5DeTZxmETkuyYYHmSBEvci/IMG_8066.JPG\",\"https://steemitimages.com/DQmTew8FXyCefBjEw6QnB7x2QYCtNx5YWdeEcnzPUPEu9Kc/IMG_8074.JPG\",\"https://steemitimages.com/DQmdmwBHuLtKpAaLjYDRey5iZ58wkqXVT5E6zUza2R9zJKq/IMG_8085.JPG\",\"https://steemitimages.com/DQmeZTjogvCrp3jj9zQcigwidi9JfetwbHyw7poe1jYFf3Q/IMG_8084.JPG\"],\"app\":\"steemit/0.1\",\"format\":\"markdown\"}",
        "last_update": "2017-05-30T10:23:12",
        "created": "2017-05-30T10:23:12",
        "active": "2017-05-30T10:23:12",
        "last_payout": "1970-01-01T00:00:00",
        "depth": 0,
        "children": 0,
        "children_rshares2": "0",
        "net_rshares": 0,
        "abs_rshares": 3037678264,
        "vote_rshares": 3037678264,
        "children_abs_rshares": 3037678264,
        "cashout_time": "2017-06-06T10:23:12",
        "max_cashout_time": "1969-12-31T23:59:59",
        "total_vote_weight": "13998187880804352",
        "reward_weight": 10000,
        "total_payout_value": "0.000 SBD",
        "curator_payout_value": "0.000 SBD",
        "author_rewards": 0,
        "net_votes": 0,
        "root_comment": 3199334,
        "max_accepted_payout": "1000000.000 SBD",
        "percent_steem_dollars": 10000,
        "allow_replies": true,
        "allow_votes": true,
        "allow_curation_rewards": true,
        "beneficiaries": [],
        "url": "/graffiti/@abh12345/graffiti-admiration-in-valencia-spain",
        "root_title": "Graffiti admiration in Valencia, Spain",
        "pending_payout_value": "0.000 SBD",
        "total_pending_payout_value": "0.000 STEEM",
        "active_votes": [{
          "voter": "abh12345",
          "weight": 0,
          "rshares": 0,
          "percent": 0,
          "reputation": "302636352187",
          "time": "2017-05-30T10:23:21"
        }],
        "replies": [],
        "author_reputation": "302636352187",
        "promoted": "0.000 SBD",
        "body_length": 3430,
        "reblogged_by": []
      },
      "adrianmada321/ice-cream": {
        "id": 3199197,
        "author": "adrianmada321",
        "permlink": "ice-cream",
        "category": "life",
        "parent_author": "",
        "parent_permlink": "life",
        "title": "Ice cream 🍨",
        "body": "![IMG_5069.JPG](https://steemitimages.com/DQmUXsqQYit8PttqMYMqdLFk5fhpwytMBPCRZXeHTT6wDh1/IMG_5069.JPG)\nIce cream could be a good decision in the warms days.",
        "json_metadata": "{\"tags\":[\"life\",\"photography\",\"sun\"],\"image\":[\"https://steemitimages.com/DQmUXsqQYit8PttqMYMqdLFk5fhpwytMBPCRZXeHTT6wDh1/IMG_5069.JPG\"],\"app\":\"steemit/0.1\",\"format\":\"markdown\"}",
        "last_update": "2017-05-30T10:15:00",
        "created": "2017-05-30T10:15:00",
        "active": "2017-05-30T10:15:00",
        "last_payout": "1970-01-01T00:00:00",
        "depth": 0,
        "children": 0,
        "children_rshares2": "0",
        "net_rshares": "14102077875",
        "abs_rshares": "14102077875",
        "vote_rshares": "14102077875",
        "children_abs_rshares": "14102077875",
        "cashout_time": "2017-06-06T10:15:00",
        "max_cashout_time": "1969-12-31T23:59:59",
        "total_vote_weight": "64805880971855935",
        "reward_weight": 10000,
        "total_payout_value": "0.000 SBD",
        "curator_payout_value": "0.000 SBD",
        "author_rewards": 0,
        "net_votes": 2,
        "root_comment": 3199197,
        "max_accepted_payout": "1000000.000 SBD",
        "percent_steem_dollars": 10000,
        "allow_replies": true,
        "allow_votes": true,
        "allow_curation_rewards": true,
        "beneficiaries": [],
        "url": "/life/@adrianmada321/ice-cream",
        "root_title": "Ice cream 🍨",
        "pending_payout_value": "0.018 SBD",
        "total_pending_payout_value": "0.000 STEEM",
        "active_votes": [{
          "voter": "clayboyn",
          "weight": "1311298463799337",
          "rshares": "13172827983",
          "percent": 10000,
          "reputation": "23048628822272",
          "time": "2017-05-30T10:15:39"
        }, {
          "voter": "adrianmada321",
          "weight": 0,
          "rshares": 929249892,
          "percent": 10000,
          "reputation": "302048712672",
          "time": "2017-05-30T10:15:00"
        }],
        "replies": [],
        "author_reputation": "302048712672",
        "promoted": "0.000 SBD",
        "body_length": 157,
        "reblogged_by": []
      },
      ...
      
      

```



