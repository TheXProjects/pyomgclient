# PyOMGClient
> A PYTHON OMEGLE CLIENT
>> Well Maintained
>>> `V 1.1.0`
# installation

```bash
pip install pyomgclient
```

# usage

```python 
from pyomgclient.omgclient import Client

client = Client()

@client.set_on_start_cb
def on_open ():
  print ("stranger connected")

@client.set_on_disconnect_cb
def on_close ():
  print ("stranger disconnected")
  # to restart
  client.start()

@client.set_on_typing_cb
def on_typing ():
  print ("stranger typing")

@client.set_on_message_cb
def on_message (msg):
  print ("message: "+msg)
  # sends a message
  # set typ = True for type and send
  client.send_message ("hi", typ = True)
  # or
  client.start_typing()
  time.sleep (1)
  # stop typing must be called otherwise the typing wont turn off
  client.stop_typing()

# solving recaptcha is not implemented on this project
# so you can set event handler for that and notify the client to 
# solve the captcha on the borwser
@client.set_on_recaptcha_cb
def on_captcha (key):
  # do something with the key 
  print ("point your browser at https://omegle.com/ and click start and solve the captcha")

# always call the start function
# atfer setting callbacks
# otherwise client will connect without
# any callbacks

client.start()

# returns client configuration in json format
print (client.credentials())
```

# Solving Recaptcha

**this project cannot solve captcha but you can set handler for that with an arg(key) the key goes somewhere on https://front1.omegle.com/recaptcha with other payloads**

# Example Projects

> example projects will be promoted here

# ⚠️ DISCLAIMER

`this projects was made for educational purposes
do not spam people with this 
and we are not responsible for any illegal purpose done with this project`

  `omegle may ban your ip address so be careful`

`Thankyou For The Likes`

**© XProjects**
