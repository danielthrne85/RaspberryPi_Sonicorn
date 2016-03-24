It's time to start the music, it's time to light the lights...



Setup:

Unicorn hat:  https://github.com/pimoroni/unicorn-hat
Python WebSocket server:   sudo pip install git+https://github.com/dpallot/simple-websocket-server.git
Ruby WebSocket Client:  sudo gem install websocket-client-simple


Running:

```
sudo python sonicorn_server.py
```


Add this aat the top of the Sonic Pi program:

```
require 'websocket-client-simple'
ws = WebSocket::Client::Simple.connect 'ws://localhost:8000'
``



Add this where you want the rainbow pulse to trigger, this send a string to the Python server to trigger the rainbow pulse

```
ws.send "rainbow"
```



At the moment it doesnt actually matter what you send, but I expect it will in the future :)
