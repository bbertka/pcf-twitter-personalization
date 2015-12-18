# PCF Twitter Personalization

[![Screenshot](https://raw.githubusercontent.com/bbertka/pcf-twitter-personalization/master/screenshot.jpg)](#)

About:<br>
Users authenticating with Twitter are able to view their timeline, and receive news article recommendations based on top 20 hashtags.  Hacker news network is used to fetch the related stories.

Upon pressing 'Stream', a personalized twitter stream is spawned for each user, and runs on the lattice cluster. This streamer is pulled for each user from Dockerhub

See deplpoyed app 'About' page for more info

Setup:<br>

0) Install Lattice: http://lattice.cf/docs/getting-started/

1) Go to http://apps.twitter.com and create application keys

2) Update the manifest.yml environment variables with your lattice IP, twitter app keys, since this app needs to authenticate users with Twitter
<pre>
  env:
    APP_KEY:
    APP_SECRET:
    ACCESS_TOKEN:
    ACCESS_TOKEN_SECRET:
    DIEGO_RECEPTOR: 
</pre>

3) Deploy to cloud foundry with command:  <b>cf push</b>

4) Login with twitter and have fun!
<br>
<br>

