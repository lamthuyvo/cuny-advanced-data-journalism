# Getting credentials for YouTube's API

For social media networks like YouTube, you’ll usually get credentials on the social media platform’s website. Let’s try getting credentials from YouTube now. To sign up for Google’s YouTube developer credentials, you’ll first need to have a Google account. If you don’t have an account, you should sign up for one at http://www.google.com. Once you have a Google account, you need to sign in and navigate to a separate page that Google has set up for developers: https://console.developers.google.com/apis/credentials.

Follow the instructions from Google to create credentials and in particular, create an API key. (For some APIs, you may encounter the term app or application, which refers to a software or phone app. This is because many developers signing up for certification will use the API to create third party apps. In our case, we’re using the API for data gathering, but we still need to sign up the way other app developers would.)

This should create a generic API key for you. The default name for your key is API key, but you can rename it by double clicking the key name. I named mine data gathering credentials.

Once you have these keys, navigate to the Library page. Google offers a variety of APIs, so you’ll need to activate access to only the API you want. To do this, navigate to YouTube Data API v3 and click on “Enable.” Now you’re ready to access YouTube through your API key!
The key is connected to your Google account and acts much like a username and password that will allow you to access the Google API. Thus, you should treat this information with the same care and caution you would treat any other username and password. Other developers may abuse your credentials if they get their hands on them and that may bar you from accessing services in the future.

When you have your credentials create a file called `youtube-api-key.txt`, put the string of your API key in there (and nothing else!) and then save it in the `data` folder of today's exercise.  
