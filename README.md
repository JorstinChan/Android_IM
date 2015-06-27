# Android_IM
In Android to send and receive instant messages

```java
// 发送消息
ECMessage msg = ECMessage.createECMessage(ECMessage.Type.TXT);
// 设置消息的属性：发出者，接受者，发送时间等
msg.setForm("$Tony的账号");
// 设置消息接收者
msg.setTo("$John的账号");
// 创建一个文本消息体，并添加到消息对象中
ECTextMessageBody msgBody = new ECTextMessageBody("欢迎来到云通讯");
// 将消息体存放到ECMessage中
msg.setBody(msgBody);
// 调用SDK发送接口发送消息到服务器
ECChatManager manager = ECDevice.getECChatManager();
manager.sendMessage(msg, 
new ECChatManager.OnSendMessageListener());


License
===

   Copyright (c) 2015 The CCP project authors. All Rights Reserved.
 
   Use of this source code is governed by a Beijing Speedtong Information Technology Co.,Ltd license
   that can be found in the LICENSE file in the root of the web site.
 
    http://www.yuntongxun.com
 
   An additional intellectual property rights grant can be found
   in the file PATENTS.  All contributing project authors may
   be found in the AUTHORS file in the root of the source tree.
 
