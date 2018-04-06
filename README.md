# Building an incoming webhook with Slack API

An incoming webhook is a way to post messages into a slack channel from outside sources. 
This particular incoming webhook displays the current time within a specific channel called `#time`, it then proceeds to run a search for messages for the current time. 

Before you start coding you need to have a few things set up: 
1. Create a Slack app if you don't already have one. 
2. Watch for your APP Credentials, these will be important.
3. Activate you incoming webhooks option under features and functionality, a URL will be provided.
4. Navigate to the OAuth and Permissions section and take note of your access token. 
5. Select the scope of your webhook, the scope, the scope defines the methods and capabilites of your app. In this one I used `search:read`.

Once you've set up your app on Node.js (or language of choice) you'll need to npm install `@slack/client` you'll need to import two classes from this library, the `IncomingWebhook` and `WebClient` classes. 

This app works by using HTTP request methods and JSON files to output the desired infromation in specified channels. 

You'll notice everytime you run your app on the terminal with node webhook.js, the time is posted to the time channel and in return you'll get a JSON file displayed on your terminal with response queries that match your message search. 

1. On you workspace settings open your App Directory, select incoming webhook and change the integrations settings to your fit your app. You'll notice the webhook url is already there. 
2. Save settings and test app! 

![Alt text](/img/ss1.png?raw=true)
![Alt text](/img/ss2.png?raw=true)





