You will need to add a dependency called `webbot`:

`pip install webbot`

Then, create a file called `gen.py`, and add this inside the file:
```py
from webbot import Browser
import secrets
import time	
while True:
	time.sleep(150)
	hash = secrets.token_hex(nbytes=16)
	print('Creating an account: ')
	print(hash)
	web = Browser()
	web.go_to('discord.gg/nF37bVa3pb')
	web.type(hash)
	web.click("Continue")
	web.quit()
	time.sleep(150)
```

Then run the file, using python:

`python gen.py`
