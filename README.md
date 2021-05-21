### Discord hasn't stated anything about this being against ToS, but you'd might aswell want to use this at your own risk.

You will need to add a dependency called `webbot`:

`pip install webbot`

Then, create a file called `gen.py`, and add this inside the file:
```py
from webbot import Browser
import secrets
import time
hash = secrets.token_hex(nbytes=16)
web = Browser()
web.go_to('https://discord.gg/9rWDYTzdV6')
time.sleep(5)
print('Creating an account: ')
print(hash)
web.type(hash)
web.click("Continue")
time.sleep(5)
web.quit()

```
Replace `PLACE DISCORD INVITE LINK HERE` with your server's invite link.

Then for every time you want an account to join, just run the file using python:

`python gen.py`

You have to delay a few minutes in between the time you run this python file.
