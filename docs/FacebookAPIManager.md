# FacebookAPIManager

A client for the Facebook Graph API.

https://developers.facebook.com/docs/graph-api

The Graph API is made up of the objects in Facebook (e.g., people,
pages, events, photos) and the connections between them (e.g.,
friends, photo tags, and event RSVPs). This client provides access
to those primitive types in a generic way. For example, given an
OAuth access token, this will fetch the profile of the active user
and the list of the user's friends:

```python
graph = facebook.GraphAPI(access_token)
user = graph.get_object("me")
friends = graph.get_connections(user["id"], "friends")
```

You can see a list of all of the objects and connections supported
by the API at https://developers.facebook.com/docs/graph-api/reference/.

You can obtain an access token via OAuth or by using the Facebook
JavaScript SDK. See
https://developers.facebook.com/docs/facebook-login for details.

If you are using the JavaScript SDK, you can use the
get_user_from_cookie() method below to get the OAuth access token
for the active user from the cookie saved by the SDK.

## Prerequisites

```bash
pip install facebook
```

and

Token obtained from Facebook Developers (<https://developers.facebook.com/docs/facebook-login>
)

## Functions 

### 1. facebookShare
```python
def facebookShare(info, img):
```

Args: 

info (String): Message to post to facebook.\
msg (Image): Image to post to facebook


Result:

Post is made to linked Facebook account
