# Android_IM
In Android to send and receive instant messages

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
