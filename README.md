# TwitterArchiveToGithubPages

## Steps to Use for the Paranoid

1. View the source code [here](https://script.google.com/d/1E3MlTiAgsjVHdSExaYoOCd0-WEXwKAJGpB8Pjd8ReALs2JxN0aGVtST7/edit?usp=drive_web)
1. Go to File -> Make a Copy and give is a nice friendly name.
1. Select the `TwitterService.gs` file from the list on the left.
1. Copy the big long string that occurs `https://script.google.com/macros/d/[  HERE  ]/edit?usp=drive_web` and paste it into the `projectKey` field replacing the value already there.
1. Go to https://apps.twitter.com and register a new app. There's no need to enter a valid callback URL, but you should set one. I used `http://localhost/foo`. Set the permissions to read-only, just to be safe. Take note of the consumer key and secret.
1. Go to https://github.com/settings/applications/new and register a new OAuth app. Use the URL you noted in step 2, but end it with `/exec`. Take note of the Client ID and Client Secret.
1. Back on Google, go to File -> Project properties -> Script properties and add the following keys:

  `tw_consumerKey` = [the Twitter consumer key from step 3]  
  `tw_consumerSecret` = [the Twitter consumer secret from step 3]  
  `git_clientId` = [the GitHub client ID from step 4]  
  `git_clientSecret` = [the GitHub client secret from step 4]
  
  Click Save.
1. Go to Publish -> Deploy as web app, enter all the details and copy the URL.
1. Open this URL in a new tab and follow the instructions to set it all up.

I discovered this functionality and repo etc when I stumbled upon https://mashe.hawksey.info/2016/08/keeping-your-twitter-archive-fresh-and-freely-hosted-on-github-pages/ whilst disappearing down a rabbit hole completely unrelated.
