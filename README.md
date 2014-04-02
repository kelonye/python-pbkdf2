
Install
---

copy ```lib/__init__.py```

Usage
---

```python

# register user

from lib import key

user.salt, user.hash = key(password)


```

```python
# login user

user = User.find(username)

salt, hash = key(password, user.salt)
auntheticated = hash == user.hash

```