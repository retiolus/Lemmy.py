# Lemmy.py

**The source code for this project is hosted on Codeberg: https://codeberg.org/retiolus/Lemmy.py**

Python wrapper for the [Lemmy](https://github.com/LemmyNet/lemmy) API. Based on the official [Lemmy TS library](https://github.com/LemmyNet/lemmy-js-client).

```bash
pip install Lemmy.py
```

```py
from lemmy import Lemmy

# Login to your account
lemmy = Lemmy("https://lemmy.ml")
lemmy.log_in("username_or_email", "password")

# Get a community ID
community_id = lemmy.discover_community("community_name")

# Get all posts from a community by ID
community_posts = lemmy.post.list(community_id=community_id)

# Get the modlog of your server
modlog = lemmy.modlog.get()

# Post a new publication on a community
lemmy.post.create(community_id=community_id, name="First Post!", body="This is the first community post.")
```
