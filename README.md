# PCF Twitter Personalization

[![Screenshot](https://raw.githubusercontent.com/bbertka/pcf-twitter-personalization/master/screenshot.jpg)](#)

About:<br>
Users authenticating with Twitter are able to view their timeline, and receive news article recommendations based on top 20 hashtags.  Hacker news network is used to fetch the related stories.

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

Note this app no longer uses Diego Lattice, so real time streaming is locked for now. With the new 1.6 runtime, managing personalized workloads for users authenticating with Twitter will be managed by CF API.  Currently this app does not scale out as it uses sessions in local memory. Plans to update sessions are in the works using Web2py integration with DB service provided by marketplace. 
