---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - Usage

toc_footers:
  # - <a href='#'>Sign Up for a Developer Key</a>

includes:
  # - errors

search: true
---

# Introduction

Welcome to the React Native Elastos Carrier Bridges! You can use our bridges in javascript to access Elastos Carrier Core RPC endpoints, which can interact with Elastos Blockchain.

You can view usage in the dark area to the right.

# Carrier Bridges

## getVersion

```javascript
static getVersion(){
  return exec('getVersion');
}
```
<!-- > Output Example:
```javascript
cry mechanic bean they discover vendor couple adapt walk room edit dinner
``` -->

Get current carrier version

## isValiAddress

```javascript
static isValidId(nodeId){
  return exec('isValidId', nodeId);
}
```
check given address is a valid carrier address or not

### Parameters

Parameter | Description
--------- | -----------
address | address to check


## isValidId

```javascript
static isValidId(nodeId){
  return exec('isValidId', nodeId);
}
```
Check given nodeId is a valid carrier node id or not

## start

```javascript
start(){
  return exec('createObject', this.config);
}
```
connect the local node to carrier network

## getAddress

```javascript
getAddress(){
  return exec('getAddress', this.id);
}
```
get current node address

## getNodeId

```javascript
getNodeId(){
  return exec('getNodeId', this.id);
}
```
get current node id.

## getSelfInfo

```javascript
getSelfInfo(){
  return exec('getSelfInfo', this.id);
}
```
get current node profile

## setSelfInfo

```javascript
setSelfInfo(info){
	const user_info = _.extend({
	  name : '',
	  description : '',
	  email : '',
	  phone : '',
	  gender : '',
	  region : ''
	}, info);
return exec('setSelfInfo', this.id, user_info);
}
```
set value to node profile

## setSelfPresence

```javascript
setSelfPresence(presence){
return exec('setSelfPresence', this.id, presence);
}
```
set current node presence status

## addFriend

```javascript
addFriend(address, msg){
return exec('addFriend', this.id, address, msg);
}
```
compare with a node address as friend

## acceptFriend

```javascript
acceptFriend(userId){
return exec('acceptFriend', this.id, userId);
}
```
accept the friend compare request

### Parameters

Parameter | Description
--------- | -----------
userId | friend's user ID

## getFriendInfo

```javascript
getFriendInfo(friendId){
return exec('getFriendInfo', this.id, friendId);
}
```
get friend info

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID

## sendMessage

```javascript
sendMessage(friendId, msg){
return exec('sendFriendMessageTo', this.id, friendId, msg);
}
```
send message to friend node

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
msg | message to send

## removeFriend


```javascript
removeFriend(friendId){
return exec('removeFriend', this.id, friendId);
}
```
remove friend from friend list

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID

## setLabel

```javascript
setLabel(friendId, label){
  return exec('setLabel', this.id, friendId, label);
}
```
set label for a friend

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
label | label to set

## getFriendList

```javascript
getFriendList(){
  return exec('getFriendList', this.id);
}
```
get friends info list
  
## close

```javascript
close(){
  return exec('close', this.id);
}
```
close carrier

## clean

```javascript
clean(){
  return exec('clean', this.id);
}
```
clean carrier

## createSession

```javascript
createSession(friendId, streamType, streamMode){
  return exec('createSession', this.id, friendId, streamType, streamMode);
}
```
create carrier session

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
streamType | stream type
streamMode | stream mode

## sessionRequest

```javascript
sessionRequest(friendId){
return exec('sessionRequest', this.id, friendId);
}
```
request to connect as session

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID

## sessionReplyRequest

```javascript
sessionReplyRequest(friendId, status, reason){
  return exec('sessionReplyRequest', this.id, friendId, status, reason);
}
```
reply the session request

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
status | status
reason | reason

## writeStream

```javascript
writeStream(streamIdOrFriendId, data){
  return exec('writeStream', this.id, streamIdOrFriendId, data);
}
```
send data to the session stream

### Parameters

Parameter | Description
--------- | -----------
streamIdOrFriendId | friend's user ID
data | data to write

## removeStream

```javascript
removeStream(friendId){
  return exec('removeStream', this.id, friendId);
}
```
remove the session stream for friend node

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID


## closeSession

```javascript
closeSession(friendId){
  return exec('closeSession', this.id, friendId);
}
```
close the session for friend node

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
data | data to write


## addService

```javascript
addService(friendId, serviceName, host, port){
  return exec('addService', this.id, friendId, serviceName, host, port);
}
```
add session service to friend node

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
serviceName | name of the service to add
host | host of the service
port | port of the service


## removeService

```javascript
removeService(friendId, serviceName){
  return exec('removeService', this.id, friendId, serviceName);
}
```
remove session service

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
serviceName | name of the service to remove


## openPortForwarding

```javascript
openPortFowarding(friendId, serviceName, host, port){
  return exec('openPortFowarding', this.id, friendId, serviceName, host, port);
}
```
connect the server with carrier port forwarding

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
serviceName | name of the service to forward
host | host of the service
port | port of the service


## closePortForwarding

```javascript
closePortForwarding(friendId, portForwardingId){
  return exec('closePortForwarding', this.id, friendId, portForwardingId);
}
```
close the server connection with carrier port forwaring

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
portForwardingId | port


## openChannel

```javascript
openChannel(friendId, cookie){
  return exec('openChannel', this.id, friendId, cookie);
}
```
open the channel for friend node.

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
cookie | cookie


## closeChannel

```javascript
closeChannel(friendId, channelId){
  return exec('closeChannel', this.id, friendId, channelId);
}
```
close the channel with channel id

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
channelId | ID of the channel

## writeChannel

```javascript
writeChannel(friendId, channelId, data){
  return exec('writeChannel', this.id, friendId, channelId, data)
}
```
send data to the friend channel

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
channelId | ID of the channel
data | data to write


## pendChannel

```javascript
pendChannel(friendId, channelId){
  return exec('pendChannel', this.id, friendId, channelId);
}
```
pend the channel with channel id

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
channelId | ID of the channel


## resumeChannel
```javascript
resumeChannel(friendId, channelId){
  return exec('resumeChannel', this.id, friendId, channelId);
}
```
resume the channel with channel id

### Parameters

Parameter | Description
--------- | -----------
friendId | friend's user ID
ChannelId | ID of the channel

