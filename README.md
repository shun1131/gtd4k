# gtd4kuriume


#### MEAN環境　構築方法

>**・nodebrew インストール**

(※すでにnodeとnpmがインストールされている場合は飛ばしてください)
**・ホームディレクトリで以下コマンド**
`curl https://raw.githubusercontent.com/hokaccha/nodebrew/master/nodebrew | perl - setup`

**・パス通す**
`vi ~/.bash_profile`

**以下の1行を追加**
`export PATH=$HOME/.nodebrew/current/bin:$PATH`

**・追加内容の反映**
`source ~/.bash_profile`

`nodebrew install latest`

`nodebrew install v4.2.4`

`nodebrew use v4.2.4`

**・nodeがインストールされているか確認**
`node -v`

**・namがインストールされているか確認**
`npm -v`

`npm install -g npm`


>**・mongodbのインストール、起動**

`sudo brew update`
`sudo brew install mongodb`
`sudo mkdir -p /data/db`
`sudo mongod`


>**・Bowerのインストール**

`npm install -g bower`


>**・mean環境の構築**

`sudo npm install -g yo grunt-cli bower generator-angular-fullstack`

>**・サンプルアプリの作成**

`sudo yo angular-fullstack:app (アプリ名)`


**- 以下質問 -**
・Existing .yo-rc configuration found, would you like to use it?
(No)
・What would you like to write scripts with?
(Babel)
・What would you like to write markup with?
(HTML)
・What would you like to write stylesheets with?
(CSS)
・What Angular router would you like to use?
(uiRouter)
・Would you like to include Bootstrap?
(Yes)
・Would you like to include UI Bootstrap?
(Yes)
・What would you like to use for data modeling?
(Mongoose (MongoDB))
・Would you scaffold out an authentication boilerplate?
(Yes)
・Would you like to include additional oAuth strategies?
(Google, Facebook, Twitter)
・Would you like to use socket.io?
(Yes)
・Would you like to use Gulp or Grunt?
(Grunt)
・What would you like to write tests with?
(Mocha + Chai + Sinon)
・What would you like to write Chai assertions with?
(Expect)


**・起動**
`grunt serve`


~http://localhost:9000で「Allo,Allo!」と画面に出れば成功~
