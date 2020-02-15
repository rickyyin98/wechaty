# Wechaty 中文版 | [英文版](./README.md)<!-- omit in toc -->

[![Wechaty](https://wechaty.github.io/wechaty/images/wechaty-logo-en.png)](https://github.com/wechaty/wechaty)

[![NPM Version](https://badge.fury.io/js/wechaty.svg)](https://www.npmjs.com/package/wechaty)
[![Downloads](https://img.shields.io/npm/dm/wechaty.svg?style=flat-square)](https://www.npmjs.com/package/wechaty)
[![GitHub stars](https://img.shields.io/github/stars/wechaty/wechaty.svg?label=github%20stars)](https://github.com/wechaty/wechaty)
[![Docker Pulls](https://img.shields.io/docker/pulls/zixia/wechaty.svg?maxAge=2592000)](https://hub.docker.com/r/zixia/wechaty/)
[![TypeScript](https://img.shields.io/badge/%3C%2F%3E-TypeScript-blue.svg)](https://www.typescriptlang.org/)
[![Greenkeeper badge](https://badges.greenkeeper.io/wechaty/wechaty.svg)](https://greenkeeper.io/)
[![Gitter](https://badges.gitter.im/Chatie/wechaty.svg)](https://gitter.im/Chatie/wechaty?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![NPM](https://github.com/wechaty/wechaty/workflows/NPM/badge.svg)](https://github.com/wechaty/wechaty/actions?query=workflow%3ANPM)
[![Docker](https://github.com/wechaty/wechaty/workflows/Docker/badge.svg)](https://github.com/wechaty/wechaty/actions?query=workflow%3ADocker)

## 聊天机器人

Wechaty 是一个为微信**个人号**提供的聊天机器人SDK， 能帮助你用最短6行Javascript代码生成你的聊天机器人, 它跨平台支持 [Linux, Windows, MacOS](https://github.com/wechaty/wechaty/actions?query=workflow%3ANPM) 和 [Docker](https://github.com/wechaty/wechaty/actions?query=workflow%3ADocker)。

:octocat: <https://github.com/Wechaty/wechaty>  
:beetle: <https://github.com/Wechaty/wechaty/issues>  
:book: <https://github.com/Wechaty/wechaty/wiki>  
:whale: <https://hub.docker.com/r/zixia/wechaty>  

## 开发者之声

> "Wechaty is a great solution, I believe there would be much more users recognize it." [link](https://github.com/Wechaty/wechaty/pull/310#issuecomment-285574472)  
> &mdash; <cite>@Gcaufy, Tencent Engineer, Author of [WePY](https://github.com/Tencent/wepy)</cite>
>
> "太好用，好用的想哭"  
> &mdash; <cite>@xinbenlv, Google Engineer, Founder of HaoShiYou.org</cite>
>
> "最好的微信开发库" [link](http://weibo.com/3296245513/Ec4iNp9Ld?type=comment)  
> &mdash; <cite>@Jarvis, Baidu Engineer</cite>
>
> "Wechaty让运营人员更多的时间思考如何进行活动策划、留存用户，商业变现" [link](http://mp.weixin.qq.com/s/dWHAj8XtiKG-1fIS5Og79g)  
> &mdash; <cite>@lijiarui, CEO of BotOrange.</cite>
>
> "If you know js ... try Wechaty, it's easy to use."  
> &mdash; <cite>@Urinx Uri Lee, Author of [WeixinBot(Python)](https://github.com/Urinx/WeixinBot)</cite>

See more at [Wiki:Voice Of Developer](https://github.com/Wechaty/wechaty/wiki/Voice%20Of%20Developer)

### 加入开发者社区

Wechaty 目前已经被数千位开发者使用并用于大量的开源项目。如果你愿意与他们交流并成为其中之一, 可以扫描下方二维码并回复 _wechaty_, 加入 **Wechaty Developers' Home**。

![Wechaty Developers' Home](docs/images/juzi-qr-code.jpeg)


## 全世界最简单的聊天机器人: 只需6行JavaScript

```javascript

const { Wechaty } = require('wechaty') // import { Wechaty } from 'wechaty'

Wechaty.instance() // Global Instance
.on('scan', (qrcode, status) => console.log(`Scan QR Code to login: ${status}\nhttps://api.qrserver.com/v1/create-qr-code/?data=${encodeURIComponent(qrcode)}`))
.on('login',            user => console.log(`User ${user} logined`))
.on('message',       message => console.log(`Message: ${message}`))
.start()
```

> **Wechaty 需要 Node.js 版本 >= 10**

这个六行的聊天机器人可以将登陆后收到的消息全部输出到控制台中。

Wechaty 的更多案例请见 [Wiki](https://github.com/Wechaty/wechaty/wiki/Examples) 和 [Example Directory](https://github.com/Wechaty/wechaty/blob/master/examples/).

## 开始之前需要

1. Node.js v10
1. `sudo apt-get install build-essential && sudo snap install shellcheck`

## 开始

[![node](https://img.shields.io/node/v/wechaty.svg?maxAge=604800)](https://nodejs.org/)

* Wechaty 入门指南 - <https://github.com/wechaty/wechaty-getting-started>

我们设置了一个只需要开发者进行简单设置就能使用 Wechaty 的代码仓库。其中的代码 **只需要** 在 `clone` & `npm install` & `npm start`之后就能使用。

如果你是想第一次尝试Wechaty的新手，我们强烈建议你从这个仓库开始，并将其用作项目的入门模板。

或者你也可以保存上文提到的 _全世界最简单的聊天机器人: 只需6行JavaScript_ 并以 `mybot.js`命名， 在你可以使用 NPM 或者 Docker 之后，运行这段代码。

### 1. Npm

[![NPM Version](https://badge.fury.io/js/wechaty.svg)](https://www.npmjs.com/package/wechaty)
[![npm (tag)](https://img.shields.io/npm/v/wechaty/next.svg)](https://www.npmjs.com/package/wechaty?activeTab=versions)
[![Downloads](https://img.shields.io/npm/dm/wechaty.svg?style=flat-square)](https://www.npmjs.com/package/wechaty)
[![install size](https://packagephobia.now.sh/badge?p=wechaty)](https://packagephobia.now.sh/result?p=wechaty)

```shell
npm init
npm install wechaty

# create your first mybot.js file, you can copy/paste from the above "The World's Shortest ChatBot Code: 6 lines of JavaScript"
# then:
node mybot.js
```

### 2. Docker

[![Docker Pulls](https://img.shields.io/docker/pulls/zixia/wechaty.svg?maxAge=2592000)](https://hub.docker.com/r/zixia/wechaty/)
[![Docker Layers](https://images.microbadger.com/badges/image/zixia/wechaty.svg)](https://microbadger.com/#/images/zixia/wechaty)

* 在 Wechaty 入门指南仓库中查看 Docker - <https://github.com/wechaty/docker-wechaty-getting-started>

> Wechaty Docker 同时支持 JavaScript 和 TypeScript. 当使用 TypeScript 时，遵循 TypeScript 语法并保存为`.ts`，因为我们使用了 `ts-node` 去运行代码，所以无需编译。

2.1. 运行 JavaScript

```shell
# for JavaScript
docker run -ti --rm --volume="$(pwd)":/bot zixia/wechaty mybot.js
```

2.2. 运行 TypeScript

```shell
# for TypeScript
docker run -ti --rm --volume="$(pwd)":/bot zixia/wechaty mybot.ts
```

> Learn more about Wechaty Docker at [Wiki:Docker](https://github.com/Wechaty/wechaty/wiki/Docker).

### 3. 变更协议(Puppet)

Wechaty 的强大之处在于，你可以换用不同的微信个人号协议来使其可以运行。 你可以通过设置不同的环境变量 `WECHATY_PUPPET` 变更至不同的协议。

如果你被提示不能使用 Web 端的协议，你可以按照提示申请: <https://github.com/wechaty/wechaty/wiki/Support-Developers> 我们提供了免费的Token帮助任意微信号都可以登录。

目前我们提供:

| 协议 | Puppet | 环境变量 |
| --- | --- | --- |
| Web | PuppetPuppeteer | `export WECHATY_PUPPET=wechaty-puppet-puppeteer` |
| iPad | PuppetPadplus | `export WECHATY_PUPPET=wechaty-puppet-padplus` |
| Mac | PuppetMacpro | `export WECHATY_PUPPET=wechaty-puppet-macpro` |
| Mock | PuppetMock | `export WECHATY_PUPPET=wechaty-puppet-mock` |
| Web | PuppetWechat4u | `export WECHATY_PUPPET=wechaty-puppet-wechat4u` |
| iPad | PuppetPadpro **已弃用** | `export WECHATY_PUPPET=wechaty-puppet-padpro` |
| iPad | PuppetPadchat **已弃用** | `export WECHATY_PUPPET=wechaty-puppet-padchat` |

Learn more about Wechaty Puppet from the Puppet Wiki:

1. Puppet Directory: <https://github.com/Wechaty/wechaty-puppet/wiki/Directory>
1. Puppet Compatibility: <https://github.com/Wechaty/wechaty-puppet/wiki/Compatibility>

## API

Read the Full Documentation at [Wechaty Official API Reference](https://wechaty.github.io/wechaty/)

### 1 Class `Wechaty`

Main bot class.

A `Bot` is a Wechaty instance that control a specific [wechaty-puppet](https://github.com/Wechaty/wechaty/wiki/Puppet).

* `new Wechaty(options?: WechatyOptions)`
    1. `options.name?: string` the name of this bot(optional)
    2. `optoins.puppet?: string` select which puppet provider we want to use. must be one of the:
        1. [wechaty-puppet-puppeteer](https://github.com/Wechaty/wechaty-puppet-puppeteer) - Angular Hook for Web Wechat <- This is the DEFAULT
        2. [wechaty-puppet-wechat4u](https://github.com/Wechaty/wechaty-puppet-wechat4u) - HTTP API for Web Wechat
        3. [wechaty-puppet-padpro](https://github.com/botorange/wechaty-puppet-padpro) - iPad App Protocol
        4. [wechaty-puppet-ioscat](https://github.com/linyimin-bupt/wechaty-puppet-ioscat) - iPhone App Hook
        5. [wechaty-puppet-mock](https://github.com/Wechaty/wechaty-puppet-mock) - Mock for Testing
    3. `optoins.puppetOptions?: PuppetOptions` options for the puppet provider.

| Wechaty | API | Description |
| :--- | :--- | :---        |
| event | [`login`](https://wechaty.github.io/wechaty/#Wechaty+on) | emit after bot login full successful |
| event | [`logout`](https://wechaty.github.io/wechaty/#Wechaty+on) | emit after the bot log out |
| event | [`friendship`](https://wechaty.github.io/wechaty/#Wechaty+on) | emit when someone sends bot a friend request|
| event | [`message`](https://wechaty.github.io/wechaty/#Wechaty+on) | emit when there's a new message |
| event | [`room-join`](https://wechaty.github.io/wechaty/#Wechaty+on) | emit when anyone join any room |
| event | [`room-topic`](https://wechaty.github.io/wechaty/#Wechaty+on) | emit when someone change room topic |
| event | [`room-leave`](https://wechaty.github.io/wechaty/#Wechaty+on) | emit when anyone leave the room |
| event | [`room-invite`](https://wechaty.github.io/wechaty/#Wechaty+on) | emit when there is a room invitation |
| event | [`scan`](https://wechaty.github.io/wechaty/#Wechaty+on) | emit when the bot needs to show you a QR Code for scanning |
| method | [`start(): Promise<void>`](https://wechaty.github.io/wechaty/#Wechaty+start) | start the bot |
| method | [`stop(): Promise<void>`](https://wechaty.github.io/wechaty/#Wechaty+stop) | stop the bot |
| method | [`logonoff(): boolean`](https://wechaty.github.io/wechaty/#Wechaty+logonoff) | bot login status |
| method | [`logout(): Promise<void>`](https://wechaty.github.io/wechaty/#Wechaty+logout) | logout the bot |
| method | [`userSelf(): ContactSelf`](https://wechaty.github.io/wechaty/#Wechaty+userSelf) | get the login-ed bot contact |
| method | [`say(text: string): Promise<void>`](https://wechaty.github.io/wechaty/#Wechaty+say) | let bot say `text` to itself |

### 2 Class `Contact`

All wechat contacts(friends/non-friends) will be encapsulated as a Contact.

| Contact | API | Description |
| :--- | :--- | :---        |
| static | [`find(query: string): Promise<null \| Contact>`](https://wechaty.github.io/wechaty/#Contact.find) | find contact by name or alias, if the result more than one, return the first one. |
| static | [`findAll(query: string): Promise<Contact[]>`](https://wechaty.github.io/wechaty/#Contact.findAll) | find contact by `name` or `alias` |
| static | [`load(query: string): Contact`](https://wechaty.github.io/wechaty/#Contact.load) | get contact by id |
| property | `id: readonly string` | get contact id |
| method | [`sync(): Promise<void>`](https://wechaty.github.io/wechaty/#Contact+sync) | force reload data for contact , sync data from lowlevel API again|
| method | [`say(text: string): Promise<void | Message>`](https://wechaty.github.io/wechaty/#Contact+say) | send text, Contact, or file to contact, return the message which the bot sent (only `puppet-padplus` supported). |
| method | [`self(): boolean`](https://wechaty.github.io/wechaty/#Contact+self) | check if contact is self |
| method | [`name(): string`](https://wechaty.github.io/wechaty/#Contact+name) | get the name from a contact |
| method | [`alias(): Promise<string>`](https://wechaty.github.io/wechaty/#Contact+alias) | get the alias for a contact |
| method | [`alias(newAlias: string): Promise<void>`](https://wechaty.github.io/wechaty/#Contact+alias) | set or delete the alias for a contact |
| method | [`friend(): boolean`](https://wechaty.github.io/wechaty/#Contact+friend) | check if contact is friend |
| method | [`type(): ContactType`](https://wechaty.github.io/wechaty/#Contact+type) | return the type of the Contact |
| method | [`province(): string`](https://wechaty.github.io/wechaty/#Contact+province) | get the region 'province' from a contact |
| method | [`city(): string`](https://wechaty.github.io/wechaty/#Contact+city) | get the region 'city' from a contact |
| method | [`avatar(): Promise<FileBox>`](https://wechaty.github.io/wechaty/#Contact+avatar) | get avatar picture file stream |
| method | [`gender(): ContactGender`](https://wechaty.github.io/wechaty/#Contact+gender) | get gender from a contact |

#### 2.1 Class `ContactSelf`

Class `ContactSelf` is extended from `Contact`.

| ContactSelf | API | Description |
| :--- | :--- | :---        |
| method | [`avatar(file: FileBox): Promise<void>`](https://wechaty.github.io/wechaty/#ContactSelf+avatar) | set avatar for bot |
| method | [`qrcode(): Promise<string>`](https://wechaty.github.io/wechaty/#ContactSelf+qrcode) | get qrcode for bot |
| method | [`signature(text: string): Promise<void>`](https://wechaty.github.io/wechaty/#ContactSelf+signature) | set signature for bot |

#### 2.2 Class `Friendship`

Send, receive friend request, and friend confirmation events.

| Friendship | API | Description |
| :--- | :--- | :---        |
| static | [`add(contact: Contact, hello?: string): Promise<void>`](https://wechaty.github.io/wechaty/#Friendship.add) | send a friend invitation to contact |
| method | [`accept(): Promise<void>`](https://wechaty.github.io/wechaty/#Friendship+accept) | accept Friend Request |
| method | [`hello(): string`](https://wechaty.github.io/wechaty/#Friendship+hello) | get the hello string from a friendship invitation |
| method | [`contact(): Contact`](https://wechaty.github.io/wechaty/#Friendship+contact) | get the contact from friendship |
| method | [`type(): FriendshipType`](https://wechaty.github.io/wechaty/#Friendship+type) | return the Friendship Type(unknown, confirm, receive, verify) |

### 3 Class `Message`

All wechat messages will be encapsulated as a Message.

| Message | API | Description |
| :--- | :--- | :---        |
| static | [`find(query: string): Promise<null \| Message>`](https://wechaty.github.io/wechaty/#Message.find) | find message in cache and return the first one |
| static | [`findAll(query: string): Promise<Message[]>`](https://wechaty.github.io/wechaty/#Message.findAll) | find messages in cache, return a message list |
| method | [`from(): Contact`](https://wechaty.github.io/wechaty/#Message+from) | get the sender from a message |
| method | [`to(): Contact`](https://wechaty.github.io/wechaty/#Message+to) | get the destination of the message |
| method | [`room(): null \| Room`](https://wechaty.github.io/wechaty/#Message+room) | get the room from the message.(If the message is not in a room, then will return `null`) |
| method | [`text(): string`](https://wechaty.github.io/wechaty/#Message+text) | get the text content of the message |
| method | [`say(text: string): Promise<void | Message>`](https://wechaty.github.io/wechaty/#Message+say) | reply a Text, Media File , or contact message to the sender, return the message which the bot sent (only `puppet-padplus` supported). |
| method | [`type(): MessageType`](https://wechaty.github.io/wechaty/#Message+type) | get the type from the message |
| method | [`self(): boolean`](https://wechaty.github.io/wechaty/#Message+self) | check if a message is sent by self |
| method | [`mention(): Contact[]`](https://wechaty.github.io/wechaty/#Message+mention) | get message mentioned contactList. |
| method | [`mentionSelf(): boolean`](https://wechaty.github.io/wechaty/#Message+mentionSelf) | check if a message is mention self |
| method | [`forward(to: Contact): Promise<void>`](https://wechaty.github.io/wechaty/#Message+forward) | Forward the received message |
| method | [`age(): number`](https://wechaty.github.io/wechaty/#Message+age) | the number of seconds since it has been created |
| method | `date(): Date` | the time it was created |
| method | [`toFileBox(): Promise<FileBox>`](https://wechaty.github.io/wechaty/#Message+toFileBox) | extract the Media File from the Message, and put it into the FileBox. |
| method | [`toContact(): Promise<Contact>`](https://wechaty.github.io/wechaty/#Message+toContact) | get Share Card of the Message |

### 4 Class `Room`

All wechat rooms(groups) will be encapsulated as a Room.

| Room | API | Description |
| :--- | :--- | :---        |
| static | [`create(contactList: Contact[], topic?: string): Promise<Room>`](https://wechaty.github.io/wechaty/#Room.create) | create a new room |
| static | [`find(query: string): Promise<null \| Room>`](https://wechaty.github.io/wechaty/#Room.find) | Try to find a room by filter. If get many, return the first one. |
| static | [`findAll(query: string): Promise<Room[]>`](https://wechaty.github.io/wechaty/#Room.findAll) | Find all contacts in a room |
| static | [`load(query: string): Room`](https://wechaty.github.io/wechaty/#Room.load) | load room by room id |
| property | `id: readonly string` |  |
| event | [`join`](https://wechaty.github.io/wechaty/#Room+on) | emit when anyone join any room |
| event | [`topic`](https://wechaty.github.io/wechaty/#Room+on) | emit when someone change room topic |
| event | [`leave`](https://wechaty.github.io/wechaty/#Room+on) | emit when anyone leave the room |
| event | [`invite`](https://wechaty.github.io/wechaty/#Room+on) | emit when receive a room invitation |
| method | [`sync(): <Promise<void>`](https://wechaty.github.io/wechaty/#Room+sync) | force reload data for room, sync data from lowlevel API again.
| method | [`say(text: string): Promise<void \| Message>`](https://wechaty.github.io/wechaty/#Room+say) | Send text,media file, contact card, or text with mention @mention contact inside Room, return the message which the bot sent (only `puppet-padplus` supported). |
| method | [`add(contact: Contact): Promise<void>`](https://wechaty.github.io/wechaty/#Room+add) | Add contact in a room |
| method | [`del(contact: Contact): Promise<void>`](https://wechaty.github.io/wechaty/#Room+del) | Delete a contact from the room |
| method | [`quit(): Promise<void>`](https://wechaty.github.io/wechaty/#Room+quit) | Bot quit the room itself |
| method | [`topic(): Promise<string>`](https://wechaty.github.io/wechaty/#Room+topic) | GET topic from the room |
| method | [`topic(newTopic: string): Promise<void>`](https://wechaty.github.io/wechaty/#Room+topic) | SET topic from the room |
| method | [`announce(text: string): Promise<void>`](https://wechaty.github.io/wechaty/#Room+announce) | SET/GET announce from the room |
| method | [`qrcode(): Promise<string>`](https://wechaty.github.io/wechaty/#Room+qrcode) | Get QR Code of the Room from the room, which can be used as scan and join the room. |
| method | [`alias(contact: Contact): Promise<string>`](https://wechaty.github.io/wechaty/#Room+alias) | Return contact's roomAlias in the room |
| method | [`roomAlias(contact: Contact): Promise<string \| null>`](https://wechaty.github.io/wechaty/#Room+roomAlias) | Same as function alias |
| method | [`has(contact: Contact): Promise<boolean>`](https://wechaty.github.io/wechaty/#Room+has) | Check if the room has member `contact` |
| method | [`memberAll(query?: string): Promise<Contact[]>`](https://wechaty.github.io/wechaty/#Room+memberAll) | Find all contacts or with specific name in a room |
| method | [`member(query: string): Promise<null \| Contact>`](https://wechaty.github.io/wechaty/#Room+member) | Find all contacts in a room, if get many, return the first one. |
| method | [`memberList():Promise<Contact[]>`](https://wechaty.github.io/wechaty/#Room+memberList) | get all room member from the room |
| method | [`owner(): null \| Contact`](https://wechaty.github.io/wechaty/#Room+owner) | Get room's owner from the room. |

#### 4.1 Class `RoomInvitation`

Accept room invitation

| RoomInvitation | API | Description |
| :--- | :--- | :---        |
| method | [`accept(): Promise<void>`](https://wechaty.github.io/wechaty/#RoomInvitation+accept) | accept Room Invitation |
| method | [`inviter(): Contact`](https://wechaty.github.io/wechaty/#RoomInvitation+inviter) | get the inviter from room invitation |
| method | [`roomTopic(): Promise<string>`](https://wechaty.github.io/wechaty/#RoomInvitation+inviter) | get the room topic from room invitation |
| method | [`date(): Promise<Date>`](https://wechaty.github.io/wechaty/#RoomInvitation+date) | the time it was created |
| method | `age(): Promise<number>` | the number of seconds since it has been created |

## TEST

[![NPM](https://github.com/wechaty/wechaty/workflows/NPM/badge.svg)](https://github.com/wechaty/wechaty/actions?query=workflow%3ANPM)
[![Docker](https://github.com/wechaty/wechaty/workflows/Docker/badge.svg)](https://github.com/wechaty/wechaty/actions?query=workflow%3ADocker)
[![Coverage Status](https://coveralls.io/repos/github/Wechaty/wechaty/badge.svg?branch=master)](https://coveralls.io/github/Wechaty/wechaty?branch=master)
[![Known Vulnerabilities](https://snyk.io/test/github/Wechaty/wechaty/badge.svg)](https://snyk.io/test/github/Wechaty/wechaty)

Wechaty is fully automatically tested by unit and integration tests, with Continious Integration & Continious Deliver(CI/CD) support powered by CI like Travis, Shippable and Appveyor.

To test Wechaty, run:

```shell
npm test
```

Get to know more about the tests from [Wiki:Tests](https://github.com/Wechaty/wechaty/wiki/Tests)

## RELEASE NOTES

* [Latest Release](https://github.com/Wechaty/wechaty/releases/latest)(All releases [here](https://github.com/Wechaty/wechaty/releases))
* [Changelog](https://github.com/Wechaty/wechaty/blob/master/CHANGELOG.md)

### Views Since Feb 15, 2019

[![HitCount](http://hits.dwyl.io/wechaty/wechaty.svg)](http://hits.dwyl.io/wechaty/wechaty)

## POWERED BY WECHATY

[![Powered by Wechaty](https://img.shields.io/badge/Powered%20By-Wechaty-blue.svg)](https://github.com/Wechaty/wechaty)

### Wechaty Badge

```markdown
[![Powered by Wechaty](https://img.shields.io/badge/Powered%20By-Wechaty-blue.svg)](https://github.com/Wechaty/wechaty)
```

Get more embed html/markdown code from [Wiki:PoweredByWechaty](https://github.com/Wechaty/wechaty/wiki/PoweredByWechaty)

### Projects Using Wechaty

1. [一个用CNN深度神经网络给图片评分的wechaty项目](https://github.com/huyingxi/wechaty_selfie)
2. [Relay between Telegram and WeChat](https://github.com/Firaenix/TeleChatRelay)
3. [A chat bot managing the HaoShiYou wechat groups run by volunteers of haoshiyou.org](https://github.com/xinbenlv/haoshiyou-bot)
4. [An interactive chat bot to manage a TODO list](https://github.com/coderbunker/candobot)
5. [Forward WeChat messages to telegram](https://github.com/luosheng/Wegram)
6. [koa与wechaty实现的微信小助手，可定时提醒与发消息设定定时任务](https://github.com/gengchen528/wechat-assistant)
7. [Wechaty Pay - 让线上没有难做的生意](https://github.com/coderwhocode/wechaty-pay)
8. [开源社的微信机器人项目](https://github.com/kaiyuanshe/wechat-robot)

Pull Request is welcome to add yours!

Learn more about Projects Using Wechaty at [Wiki:PoweredByWechaty](https://github.com/Wechaty/wechaty/wiki/PoweredByWechaty)

## Find a Good Server

The best practice for running Wechaty Docker/NPM is using a VPS(Virtual Private Server) outside of China, which can save you hours of time because `npm install` and `docker pull` will run smoothly without any problem.

The following VPS providers are used by the Wechaty team, and they worked perfectly in production. You can use the following link to get one in minutes. Also, doing this can support Wechaty because you are referred by us.

| Location  | Price | Ram     | Payment           | Provider |
| ---       | ---   | ---     | ---               | ---      |
| Singapore | $5    | 512MB   | Paypal            | [DigitalOcean](https://m.do.co/c/01a54778df5c) |
| Japan     | $5    | 1GB     | Paypal            | [Linode](https://www.linode.com/?r=5fd2b713d711746bb5451111df0f2b6d863e9f63) |
| Korea     | $10   | 1GB     | Alipay, Paypal    | [Netdedi](https://www.netdedi.com/?affid=35) |
| Singapore | $3.5  | 512MB   | Alipay, Wechat    | [Vultr](https://www.vultr.com/?ref=6986613) |

## See Also

* [RelatedProject](https://github.com/Wechaty/wechaty/wiki/RelatedProject)

## The Story

In 2017 ...

Huan's daily life/work depends on too much chat on wechat.

* Almost 14,000 wechat friends in May 2014, before wechat restricts a total number of friends to 5,000.
* Almost 400 wechat rooms, and most of them have more than 400 members.

Can you imagine that? He was dying...

So a tireless bot working for me 24x7 on wechat, monitoring/filtering the most important message is badly needed. For example, it highlights discussion which contains the KEYWORDS which he want to follow up(especially in a noisy room). ;-)

At last, It's built for huan's personal study purpose of Automatically Testing.

## Contributors

[![GitHub issues](https://img.shields.io/github/issues/wechaty/wechaty.svg)](https://github.com/Wechaty/wechaty/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/wechaty/wechaty.svg)](https://github.com/Wechaty/wechaty/pulls)
[![Open Collective Backers](https://opencollective.com/wechaty/backer/badge.svg?label=open%20collective%20backers&color=blue)](https://opencollective.com/wechaty/)
[![Open Collective Sponsors](https://opencollective.com/wechaty/sponsors/badge.svg?label=open%20collective%20sponsors&color=blue)](https://opencollective.com/wechaty/)

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].
[![Contribute](https://opencollective.com/wechaty/contributors.svg?width=890&button=false)](https://github.com/Wechaty/wechaty/graphs/contributors)

## Backers

[![Backers on Open Collective](https://opencollective.com/wechaty/backers/badge.svg)](#backers)

Thank you to all our backers! 🙏 [[Become a backer](https://opencollective.com/wechaty#backer)]

[![Open Collective Wechaty](https://opencollective.com/wechaty/backers.svg?width=890)](https://opencollective.com/wechaty#backers)

## Sponsors

[![Sponsors on Open Collective](https://opencollective.com/wechaty/sponsors/badge.svg)](#sponsors)

Support this project by becoming a sponsor. Your logo will show up here with a link to your website. [[Become a sponsor](https://opencollective.com/wechaty#sponsor)]

[![Wechaty Sponsor](https://opencollective.com/wechaty/sponsor.svg?width=890)](https://opencollective.com/wechaty/#sponsor)

## Author

1. [Huan](https://github.com/huan) [(李卓桓)](http://linkedin.com/in/zixia) \<huan@chatie.io\>
1. [Rui (李佳芮)](https://pre-angel.com/peoples/jiarui-li/)

[![Profile of Huan LI (李卓桓) on StackOverflow](https://stackoverflow.com/users/flair/1123955.png)](https://stackoverflow.com/users/1123955/huan)

## Copyright & License

* Code & Docs © 2016-now Huan LI \<zixia@zixia.net\>
* Code released under the Apache-2.0 License
* Docs released under Creative Commons
