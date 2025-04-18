
# How to use the json files from this folder to generate mention networks?

### Step 1: open a **new** Google Colab notebook.

### Step 2: upload the json file of your interest.

### Step 3: copy the code below to a new code block

Make sure to change baby.json to the name of the json file you uploaded.

The user attributes will be saved in `user_df` and the edge list will be saved in `edge_df`.

```python
!pip install --upgrade --force-reinstall git+https://github.com/tantantan12/itom6219.git

from itom6219 import  user_info, user_tweets, user_tweets_all, search_tweets_by_topic  ,extract_user_mention_edges
import json
with open('baby.json', 'r', encoding='utf-8') as f:
    tweets_dict = json.load(f)

user_df, edge_df = extract_user_mention_edges(tweets_dict)

user_df
```