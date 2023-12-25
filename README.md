## Notification !

Note! This Is A Product Remade By Aditta Datta Joyanto (Because Of Schmavery's Facebook-Chat-Api, The Author Does Not Take Any Responsibility!), If There Are Errors, Please Try Using Another Product!, DongDev Restores 


# Api Cho ChatBot Messenger

Facebook Already Has And Allows Users To Create Api For Chatbots 😪 Here => [Here Ne](https://developers.facebook.com/docs/messenger-platform).

### This Api Can Make You Payy Acc Like You Never Had Acc, Please Pay Attention =))

Note ! If You Want To Use This Api Please See Document At [Here](https://github.com/Schmavery/facebook-chat-api).

## Download 

If You Want To Use It, Download It By:
```bash
npm i fca-dongdev-remake
```
or
```bash
npm install fca-dongdev-remake
```

It Will Download To node_modules (Your Lib) - Note Replit Will Not Show Anywhere To Find 😪

## If You Want To Test Api 

The benefit of this is that you won't waste time paying and having an account 😪
Please Use With Demo Account => [Facebook Whitehat Accounts](https://www.facebook.com/whitehat/accounts/).

## Using

```javascript
const login = require("fca-dongdev-remake"); // taken from lib 

// log in
login({email: "Gmail Account", password: "Your Facebook Password"}, (err, api) => {

    if(err) return console.error(err); // error case

    // Create a bot that automatically imitates you:
    api.listenMqtt((err, message) => {
        api.sendMessage(message.body, message.threadID);
    });

});
```

As a result, it will imitate you as shown below:
<img width="517" alt="screen shot 2016-11-04 at 14 36 00" src="https://cloud.githubusercontent.com/assets/4534692/20023545/f8c24130-a29d-11e6-9ef7-47568bdbc1f2.png">

If You Want Advanced Use Then Use The Bot Types Listed Above!

## List

You Can Read Full Api Tai => [here](DOCS.md).

## Settings For Mirai: 

You Need To Go To File Mirai.js, Then Find Line
```js
    var login = require('tùy bot'); 
    /* Có thể là :
        var login = require('@maihuybao/fca-Unofficial');
        var login = require('fca-xuyen-get');
        var login = require('fca-unofficial-force');
    ...   
    */
```

And Replace It With:

```js
    var login = require('fca-dongdev-remake')
```

After that, run normally!

## Self-study

If You Want To Research Or Create Your Own Bot, Go To This To Read Its Functions And How To Use It => [Link](https://github.com/Schmavery/facebook-chat-api#Unofficial%20Facebook%20Chat%20API)

------------------------------------

### Save Login Information.

To Save, You Need 1 Apstate Type (Cookie, etc,..) To Save Or Use Login Code As Above To Log In!

Và Chế Độ Này Đã Có Sẵn Trong 1 Số Bot Việt Nam Nên Bạn Cứ Yên Tâm Nhé !

__Instructions With Appstate__

```js
const fs = require("fs");
const login = require("fca-dongdev-remake");

var credentials = {email: "FB_EMAIL", password: "FB_PASSWORD"}; // thông tin tk

login(credentials, (err, api) => {
    if(err) return console.error(err);
    // đăng nhập
    fs.writeFileSync('appstate.json', JSON.stringify(api.getAppState(), null,'\t')); //tạo appstate
});
```

Or Easier (Professional) You Can Use => [c3c-fbstate](https://github.com/c3cbot/c3c-fbstate) Để Lấy Fbstate And Rename Lại Thành Apstate Cũng Được ! (appstate.json)

------------------------------------

## FAQS

FAQS => [Link](https://github.com/Schmavery/facebook-chat-api#FAQS)