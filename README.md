
Install
---

copy ```lib/__init__.py```

Usage
---

```python

# register user

from lib import key

salt, hash = key(password)
user.salt = salt
user.hash = hash

```

```python
# login user

user = User.find(username)

auntheticated = key(password, user.salt)
```