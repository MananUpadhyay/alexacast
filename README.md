# alexacast

Alexa skill to control local Chromecast devices. You will need to run it on the same network as your Chromecast.

 - Setup the Alexa skill in Amazon Developer console and enable test mode for the skill.
 - Login on Alexa enabled device (e.g. Echo Dot) with the same credentials as the Developer account.

# Running Instructions

 - Run the Alexa Service as above
   ```
   $ pip install -r requirements.txt
   $ python server.py --device='Your Chromecast Name'
   ```
 - Expose local server to web
   ```
    $ ngrok http -bind-tls=true -host-header=rewrite [port]
   ```


## usage

Trigger word for the service is "chromecast"

- "alexa, ask chromecast to skip this"
- "alexa, ask chromecast to pause"
- "alexa, ask chromecast to play"
- "alexa, ask chromecast to reconnect"
  - if everything stops working this might fix it
- "alexa, ask chromecast to reboot"
  - sometimes the chromecast gets itself into dumb states and needs to be
    restarted.


## References

- https://github.com/erik/alexandra
- https://medium.com/@cnadeau_/allow-alexa-to-run-your-locally-hosted-skill-1786e3ca7a1b
