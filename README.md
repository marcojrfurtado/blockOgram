## [blockOgram](https://blockogram.com) — Telegram in the Blockstack


blockOgram is a [Telegram](https://www.telegram.org) web-based client for the Blockstack. It is forked from [Webogram](https://github.com/zhukov/webogram), the official Telegram web client. Log in to your Telegram account, and have it associated to your Blockstack Id. Access it on any device. The app will not store any of your information in a central server, the data is ownded by you. Log-in session is persisted according to your [Gaia](https://github.com/blockstack/gaia) storage preferences. 

So why bother using the having Blockstack support? As a start, the app will allow you to store the log-in session. However, there is at least one major Telegram feature that could benefit from Gaia storage. Telegram allows us to create **Secret chats**, which offer end-to-end encryption of your conversation, and would not work be valuable with some sort of persistence support. The long term goal is to support it in blockOgram.


### Unsupported at the moment

* Secret chats
* Black list
* ...


### Maintained locations


| Description        | URL           | Type  |
| ------------- |-------------| -----:|
| Online Web-version | https://blockogram.com/ | hosted


## Technical details

The app is based on the AngularJS JavaScript framework, and written in pure JavaScript. jQuery is used for DOM manipulations, and Bootstrap as the CSS-framework.


### Running locally


The project repository is based on angularjs-seed and includes gulp tasks, so it's easy to launch the app locally on your desktop.
Install [node.js](http://nodejs.org/).

Install dependencies with:

```lang=bash
npm install
```

Optionaly, run the following commands in the project directory to install gulp globally:

```lang=bash
sudo npm install -g gulp
```

This will install all the needed dependencies.

The app only runs on HTTPS. You will need a valid certificate. When running locally, you may simply create a self-signed certificate as follows:
```lang=bash
bash scripts/create_self_signed_cert.sh
```

You will be prompted to enter the details of the certificate. Ensure that you are using `localhost` as the domain. The certificate will be created in the local directory.

#### Running web-server

Just run `npm start` (`gulp watch`) to start the web server and the livereload task.
Open https://localhost:8000/index.html in your browser.


#### Running in production

Run `npm run clean` (`gulp clean`), then `npm run build` (`gulp publish`) to build the minimized production version of the app. Copy `dist` folder contents to your web server. Don't forget to set `X-Frame-Options SAMEORIGIN` header ([docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/X-Frame-Options)).


### Third party libraries

Besides the frameworks mentioned above, other libraries are used for protocol and UI needs. Here is the short list:

* [JSBN](http://www-cs-students.stanford.edu/~tjw/jsbn/)
* [CryptoJS](https://code.google.com/p/crypto-js/)
* [zlib.js](https://github.com/imaya/zlib.js)
* [UI Bootstrap](http://angular-ui.github.io/bootstrap/)
* [jQuery Emojiarea](https://github.com/diy/jquery-emojiarea)
* [nanoScrollerJS](https://github.com/jamesflorentino/nanoScrollerJS)
* [gemoji](https://github.com/github/gemoji)
* [emoji-data](https://github.com/iamcal/emoji-data)
* [blockstack](https://github.com/blockstack/blockstack.js)

Many thanks to all these libraries' authors and contributors. A detailed list with descriptions and licenses is available [here](/app/vendor).


### Licensing

The source code is licensed under GPL v3. License is available [here](/LICENSE).


### [Contribute](CONTRIBUTING.md)
