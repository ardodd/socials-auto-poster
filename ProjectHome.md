# Post To Social Networks #

### Post to **Facebook, Twitter, Google Plus** ###

---


Latest version: 1.1


---


```

require_once "SocialAutoPoster/SocialAutoPoster.php";

$autoposter = new SocialAutoPoster();

$facebook = $autoposter->getApi('facebook',array(
    'page_id' => 'PAGE_ID',
    'appid' => 'APP_ID',
    ['appsecret' => 'APP_SECRET']
));

$facebook->getLoginBox();
$facebook->postToWall('Hello FB');
$facebook->getErrors();

$twitter = $autoposter->getApi('twitter',array(
        'consumer_key' => 'CONSUMER_KEY',
        'consumer_secret' => 'CONSUMER_SECRET',
        'access_token' => 'ACCESS_TOKEN',
        'access_secret' => 'ACCESS_SECRET'
));

$twitter->postToWall('Hello TW');
$twitter->getErrors();

$googleplus = $autoposter->getApi('googleplus',array(
        'email' => 'YOUR_EMAIL',
        'pass' => 'YOUR_PASS',
));

$googleplus->begin('PAGE_ID');
$googleplus->postToWall('First Hello to G+');
$googleplus->postToWall('Second Hello to G+');
$googleplus->end();
$googleplus->isHaveErrors();
$googleplus->getErrors();

```


---


#### Facebook ####
Create App - https://developers.facebook.com/apps
<br />
Create Page - http://www.facebook.com/pages/create.php

#### Twitter ####
Create Account - https://twitter.com/
<br />
Create App - https://dev.twitter.com/apps/new

#### Google+ ####
Create Page - https://plus.google.com/pages/create
<pre>Your Page - https://plus.google.com/b/PAGE_ID/</pre>