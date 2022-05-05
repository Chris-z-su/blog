---
title: ActiveMQ入门
excerpt: ActiveMQ是一个基于Java的消息队列服务器，它提供了一个简单的消息队列服务器，可以用来支持多个客户端进行消息的发送和接收。
date: 2022-04-21 09:51:39
update: 2022-04-21 23:09:00
categories: 
  - Java
  - 消息队列
tags: 
  - Java
  - 编程语言
  - 面试
---

## 1 ActiveMQ简介

### 1.1 ActiveMQ是什么

ActiveMQ是一个消息队列应用服务器（推送服务器）。支持JMS规范。

#### 1.1.1 JMS概述

JMS 全称：Java Message Service ，即为 Java 消息服务，是一套 java 消息服务的 API 接口。实现了 JMS 标准的系统，称之为 JMS Provider。

#### 1.1.2 消息队列

消息队列是在消息的传输过程中保存消息的容器，提供一种不同进程或者同一进程不同线程直接通讯的方式。

![](images/消息队列通讯方式.png)

- Producer：消息生产者，负责产生和发送消息到 Broker；
- Broker：消息处理中心。负责消息存储、确认、重试等，一般其中会包含多个 queue；
- Consumer：消息消费者，负责从 Broker 中获取消息，并进行相应处理；

常见消息队列应用：

1. ActiveMQ

> ActiveMQ 是Apache出品，最流行的，能力强劲的开源消息总线。ActiveMQ 是一个完全支持JMS1.1和J2EE 1.4规范的 JMS Provider实现。

2. RabbitMQ

> RabbitMQ是一个在AMQP基础上完成的，可复用的企业消息系统。他遵循Mozilla Public License开源协议。开发语言为Erlang。

3. RocketMQ

> 由阿里巴巴定义开发的一套消息队列应用服务。

### 1.2 ActiveMQ能做什么

1. 实现两个不同应用(程序)之间的消息通讯。
2. 实现同一个应用，不同模块之间的消息通讯。（确保数据发送的稳定性）

### 1.3 ActiveMQ主要特点

1. 支持多语言、多协议客户端。语言: Java,C,C++,C#,Ruby,Perl,Python,PHP。应用协议： OpenWire, Stomp REST, WS Notification, XMPP, AMQP
2. 对Spring的支持，ActiveMQ可以很容易整合到Spring的系统里面去。
3. 支持高可用、高性能的集群模式。

## 2 入门示例

### 2.1 需求

使用 ActiveMQ 实现消息队列模型。

### 2.2 配置步骤说明

1. 搭建ActiveMQ消息服务器。
2. 创建一个java项目。
3. 创建消息生产者，发送消息。
4. 创建消息消费者，接收消息。

### 2.3 第一部分：搭建ActiveMQ消息服务器

#### 2.3.1 第一步：下载、上传至Linux，并解压

![img](https://app.yinxiang.com/shard/s10/res/6a1c4753-556e-4e59-aa9a-bc0f61794b97/fcf934ecb4c6bfc3d35b41acdcd0db48.jpg)

#### 2.3.2 第二步：启动ActiveMQ服务器

```

```

#### 2.3.3 第三步：浏览器访问 ActiveMQ 管理界面

##### 2.3.3.1 Step1：查看ActiveMQ管理界面的服务端口。在 `/conf/jetty.xml` 中

![img](https://app.yinxiang.com/shard/s10/res/13c2f74c-102a-4933-94f8-ff55698af2e5/bd4af40805acdeba73490f709b45c11d.jpg)

默认端口为: 8161

##### 2.3.3.2 Step2：查看ActiveMQ用户、密码。在 `/conf/users.properties` 中

默认用户名密码均为 admin

##### 2.3.3.3 Step3：访问ActiveMQ管理控制台。地址：[http://ip:8161/](https://link.zhihu.com/?target=http%3A//ip%3A8161/)

> 注意：若防火墙没有配置该服务的端口，必须在防火墙中配置。

![img](https://app.yinxiang.com/shard/s10/res/1d95eea4-3427-46eb-b9db-450fe2567071/42221aa2fdb66d6d7320b8f65b8ffe89.jpg)

点击图示选项后，进行登录

![img](https://app.yinxiang.com/shard/s10/res/4aeef141-e4a9-45cd-9135-570efa6396e8/c66e1d41d6cc07c91a4252fa8619b66c.jpg)

然后成功进入管理界面

![img](https://app.yinxiang.com/shard/s10/res/3350677b-b14f-4d11-bcec-93de7e3ac31a/f18b1758998494e99858d9bcc91bdcc7.jpg)

### 2.4 第二部分：创建java项目，导入jar包

ActiveMQ 的解压包中，提供了运行 ActiveMQ 需要的 jar 包。

![img](https://app.yinxiang.com/shard/s10/res/c458e8b9-fa52-4024-9b52-8b0fdb9b03f7/d4ba9a1079b2ae843bd4489eaae6ac75.jpg)

ActiveMQ 是实现了 JMS 规范的。在实现消息服务的时候，必须基于 API 接口规范。

#### 2.4.1 JMS 常用的 API 说明

下述 API 都是接口类型，定义在 javax.jms 包中，是 JMS 标准接口定义。ActiveMQ 完全实现这一套 api 标准。

##### 2.4.1.1 ConnectionFactory

链接工厂, 用于创建链接的工厂类型。

##### 2.4.1.2 Connection

链接，用于建立访问ActiveMQ连接的类型, 由链接工厂创建。

##### 2.4.1.3 Session

会话, 一次持久有效、有状态的访问，由链接创建。

##### 2.4.1.4 Destination & Queue & Topic

目的地, 即本次访问ActiveMQ消息队列的地址，由Session会话创建。

1. interface Queue extends Destination
2. Queue：队列模型，只有一个消费者。消息一旦被消费，默认删除。
3. Topic：主题订阅中的消息，会发送给所有的消费者同时处理。

##### 2.4.1.5 Message

消息，在消息传递过程中数据载体对象，是所有消息【文本消息TextMessage，对象消息ObjectMessage等】具体类型的顶级接口，可以通过会话创建或通过会话从 ActiveMQ 服务中获取。

##### 2.4.1.6 MessageProducer

消息生成者, 在一次有效会话中, 用于发送消息给ActiveMQ服务的工具，由Session会话创建。

##### 2.4.1.7 MessageCustomer

消息消费者【消息订阅者，消息处理者】, 在一次有效会话中, 用于ActiveMQ服务中获取消息的工具，由Session会话创建。

### 2.5 第三部分：创建消息生成者，发送消息

> 注意：ActiveMQ 服务接受消息的入口是 61616 端口，防火墙还需要开放此端口

```Java
package com.shubao.mq.activemq.ptp;

import org.apache.activemq.ActiveMQConnectionFactory;
import org.junit.Test;

import javax.jms.*;

/**
 * @version 1.0
 * @program: spring
 * @description: 消息生产者
 * @author: chris
 * @create: 2022-04-21 10:30
 * @since JDK1.8
 **/
public class MyProducer {

    //定义连接工厂
    ConnectionFactory connectionFactory;

    //定义连接
    Connection connection;

    //定义session会话
    Session session;

    //定义消息目的地
    Destination destination;

    //定义消息生产者
    MessageProducer producer;

    //定义消息
    Message message;

    public void init() throws JMSException {
        //创建连接工厂
        connectionFactory = new ActiveMQConnectionFactory("tcp://localhost:61616");
        //创建连接
        connection = connectionFactory.createConnection();
        //启动连接
        connection.start();
        //创建session会话，第一个参数是是否开启事务，第二个参数是自动确认模式
        session = connection.createSession(false, Session.AUTO_ACKNOWLEDGE);
        //创建消息目的地，Queue：消息类型是队列，Topic：消息类型是主题
        destination = session.createQueue("myQueue");
        //创建消息生产者
        producer = session.createProducer(destination);
        //设置消息生产者的持久化
        // producer.setDeliveryMode(DeliveryMode.PERSISTENT);
        //创建消息
        message = session.createTextMessage("hello world");
    }

    public void sendMessage(String message) throws JMSException {
        //创建消息
        TextMessage textMessage = session.createTextMessage(message);
        //发送消息
        producer.send(textMessage);
    }

    public void close() throws JMSException {
        //关闭消息生产者
        producer.close();
        //关闭会话
        session.close();
        //关闭连接
        connection.close();
    }

    @Test
    public void sentToActiveMQ(){
        try {
            /*
             * 创建连接工厂，由 ActiveMQ 实现。构造方法参数
             * userName 用户名
             * password 密码
             * brokerURL 访问 ActiveMQ 服务的路径地址，结构为: 协议名://主机地址:端口号
             */
            connectionFactory = new ActiveMQConnectionFactory("admin", "admin", "tcp://127.0.0.1:61616");
            //创建连接
            connection = connectionFactory.createConnection();
            //启动连接
            connection.start();
            /*
             * 创建会话，参数含义:
             * 1.transacted - 是否使用事务
             * 2.acknowledgeMode - 消息确认机制，可选机制为：
             *  1）Session.AUTO_ACKNOWLEDGE - 自动确认消息
             *  2）Session.CLIENT_ACKNOWLEDGE - 客户端确认消息机制
             *  3）Session.DUPS_OK_ACKNOWLEDGE - 有副本的客户端确认消息机制
             */
            session = connection.createSession(false, Session.AUTO_ACKNOWLEDGE);
            //创建消息目的地，也就是队列名，Queue：消息类型是队列，Topic：消息类型是主题
            destination = session.createQueue("myQueue");
            //创建消息生产者
            producer = session.createProducer(destination);
            //创建消息
            message = session.createTextMessage("hello world");
            //发送消息
            producer.send(message);
        } catch (JMSException e) {
            e.printStackTrace();
        } finally {
            try {
                //关闭消息生产者
                if (producer != null) {
                    producer.close();
                }
                //关闭会话
                if (session != null) {
                    session.close();
                }
                //关闭连接
                if (connection != null) {
                    connection.close();
                }
            } catch (JMSException e) {
                e.printStackTrace();
            }
        }
    }
}
```

使用测试方法执行后，可以看到成功将消息加入队列

![img](https://app.yinxiang.com/shard/s10/res/e7587e63-6b06-4825-aab8-de07cfd1c3cb/03a630300f7b7dc980e409180a66a95c.jpg)

### 2.6 第四部分：创建消息消费者，消费消息

```java
package com.shubao.mq.activemq.ptp;

import org.apache.activemq.ActiveMQConnectionFactory;

import javax.jms.*;

/**
 * @version 1.0
 * @program: spring
 * @description: 消费者
 * @author: chris
 * @create: 2022-04-21 10:30
 * @since JDK1.8
 **/
public class MyConsumer {

    //定义连接工厂
    ConnectionFactory connectionFactory;

    //定义连接
    Connection connection;

    //定义会话
    Session session;

    //定义目的地
    Destination destination;

    //定义消费者
    MessageConsumer consumer;

    //定义消息
    Message message;

    public void init() throws Exception {
        //创建连接工厂
        connectionFactory = new ActiveMQConnectionFactory("tcp://localhost:61616");
        //创建连接
        connection = connectionFactory.createConnection();
        //启动连接
        connection.start();
        //创建会话
        session = connection.createSession(false, Session.AUTO_ACKNOWLEDGE);
        //创建目的地
        destination = session.createQueue("myQueue");
        //创建消费者
        consumer = session.createConsumer(destination);

        //接收消息
        message = consumer.receive();
    }

    public void close() throws Exception {
        //关闭消费者
        consumer.close();
        //关闭会话
        session.close();
        //关闭连接
        connection.close();
    }

    public static void main(String[] args) throws Exception {
        MyConsumer myConsumer = new MyConsumer();
        myConsumer.init();
        System.out.println("接收到的消息是：" + ((TextMessage) myConsumer.message).getText());
        myConsumer.close();
    }
}
```

测试结果

且后台管理界面也可以看到已被消费

![img](https://app.yinxiang.com/shard/s10/res/48b94acc-3d5a-4b7a-918a-c0bec206414d/3b846106d078408c3474da63593fe92a.jpg)

## 3 ActiveMQ监听器

在前面的示例中，我们发现消费者每次只能消费一条消息。当队列中有多条消息的时候，我们需要多次运行消费者，才能消费完这些消息。我们希望一次将所有的消息全部接收，可以使用 ActiveMQ 监听器来监听队列，持续消费消息。

答：使用ActiveMQ监听器来监听队列，持续消费消息。

### 3.1 配置步骤说明

1. 创建一个监听器对象。
2. 修改消费者代码，加载监听器

### 3.2 配置步骤

#### 3.2.1 第一步：创建监听器 MyListener 类

> 自定义监听器需要实现 MessageListener 接口

```java
package com.shubao.mq.activemq.ptp;

import javax.jms.Message;
import javax.jms.MessageListener;
import javax.jms.TextMessage;

/**
 * @version 1.0
 * @program: spring
 * @description: 消息监听器
 * @author: chris
 * @create: 2022-04-21 10:30
 * @since JDK1.8
 **/
public class MyListener implements MessageListener {

    @Override
    public void onMessage(Message message) {
        try {
            TextMessage textMessage = (TextMessage) message;
            System.out.println("收到消息：" + textMessage.getText());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }

}
```

#### 3.2.2 第二步：修改MyConsumer代码，加载监听器

> 监听器需要持续加载，因此需要使消费程序不结束。这里我们使用输入流阻塞消费线程结束。（实际开发中，使用web项目加载）

```java
package com.shubao.mq.activemq.ptp;

import org.apache.activemq.ActiveMQConnectionFactory;

import javax.jms.*;

/**
 * @version 1.0
 * @program: spring
 * @description: 消费者
 * @author: chris
 * @create: 2022-04-21 10:30
 * @since JDK1.8
 **/
public class MyConsumer {

    //定义连接工厂
    ConnectionFactory connectionFactory;

    //定义连接
    Connection connection;

    //定义会话
    Session session;

    //定义目的地
    Destination destination;

    //定义消费者
    MessageConsumer consumer;

    //定义消息
    Message message;

    public void init() throws Exception {
        //创建连接工厂
        connectionFactory = new ActiveMQConnectionFactory("tcp://localhost:61616");
        //创建连接
        connection = connectionFactory.createConnection();
        //启动连接
        connection.start();
        //创建会话
        session = connection.createSession(false, Session.AUTO_ACKNOWLEDGE);
        //创建目的地
        destination = session.createQueue("myQueue");
        //创建消费者
        consumer = session.createConsumer(destination);

        //接收消息
        // message = consumer.receive();

        //加载监听器
        consumer.setMessageListener(new MyListener());

        //监听器需要持续加载，所以需要一直调用，使用输入流的方式阻塞当前线程结束
        System.in.read();
    }

    public void close() throws Exception {
        //关闭消费者
        consumer.close();
        //关闭会话
        session.close();
        //关闭连接
        connection.close();
    }

    public static void main(String[] args) throws Exception {
        MyConsumer myConsumer = new MyConsumer();
        myConsumer.init();
        System.out.println("接收到的消息是：" + ((TextMessage) myConsumer.message).getText());
        myConsumer.close();
    }
}
```

### 3.3 测试

先添加 5 条消息到队列

![img](https://app.yinxiang.com/shard/s10/res/b08580b7-5fd2-46af-bef0-370a52c88a71/5ebde2abd78a62620dd3b467d56bc19a.jpg)

运行 Consumer 的测试程序，可以看到连续接受了 5 条消息，且接续添加会继续输出消息。

## 4 ActiveMQ消息服务模式

在入门示例中，只能向一个消费者发送消息。但是有一些场景，需求有多个消费者都能接收到消息，比如：美团 APP 每天的消息推送。该如何实现呢？

ActiveMQ是通过不同的服务模式来解决这个问题的。要搞清楚这个问题，必须知道ActiveMQ有哪些应用模式。

### 4.1 PTP模式（point to point）

消息模型

![img](https://app.yinxiang.com/shard/s10/res/07d3b4e3-5424-4029-810a-2821c1d4fbc9/521364d5b2704bd9d94707f611fab6ee.jpg)

1. 消息生产者生产消息发送到queue中，然后消息消费者从queue中取出并且消费消息。
2. 消息被消费以后，queue中不再有存储，所以消息消费者不可能消费到已经被消费的消息。
3. Queue支持存在多个消费者，但是对一个消息而言，只会有一个消费者可以消费、其它的则不能消费此消息了。
4. 当消费者不存在时，消息会一直保存，直到有消费消费

> 入门示例就是采用的这种 PTP 服务模式

### 4.2 TOPIC（主题订阅模式）

消息模型

![img](https://app.yinxiang.com/shard/s10/res/64d3faa7-7e49-49c2-9819-95af7d6184ee/2209959e1f5abf1d75100faa40807c91.jpg)

1. 消息生产者（发布）将消息发布到topic中，同时有多个消息消费者（订阅）消费该消息。
2. 和点对点方式不同，发布到topic的消息会被所有订阅者消费。
3. 当生产者发布消息，不管是否有消费者。都不会保存消息

所以，主题订阅模式下，==一定要先有消息的消费者(订阅者)，后有消息的生产者(发布者)==。

## 5 Topic模式实现

### 5.1 配置步骤说明

1. ~~搭建ActiveMQ消息服务器。~~
2. 创建主题订阅者。
3. 创建主题发布者。

### 5.2 配置步骤

#### 5.2.1 ~~第一部分：搭建消息服务器。（已实现）~~

#### 5.2.2 第二部分：创建主题订阅者 MySubscriber

主题订阅模式下，可以有多个订阅者。我们这里用多线程来模拟。创建 MySubscriber 类，实现 Runnable 接口

```java
package com.shubao.mq.activemq.topic;

import org.apache.activemq.ActiveMQConnectionFactory;

import javax.jms.*;

/**
 * @version 1.0
 * @program: spring
 * @description: 主题订阅者
 * @author: chris
 * @create: 2022-04-21 10:52
 * @since JDK1.8
 **/
public class MySubscriber implements Runnable {

    // 定义连接工厂
    TopicConnectionFactory factory;

    // JMS连接，属于Pub/Sub方式的连接
    TopicConnection connection;

    // JMS会话，属于Pub/Sub方式的会话
    TopicSession session;

    // 定义消息队列，消息队列名称为：TEST_QUEUE
    Topic topic;

    // 主题订阅者
    TopicSubscriber subscriber;

    // 定义消息
    Message message;

    @Override
    public void run() {
        try {
            // 创建连接工厂
            factory = new ActiveMQConnectionFactory("tcp://localhost:61616");
            // 通过工厂创建连接
            connection = factory.createTopicConnection();
            // 开启连接
            connection.start();
            // 创建会话
            session = connection.createTopicSession(false, TopicSession.AUTO_ACKNOWLEDGE);
            // 创建消息队列 参数：主题名称，是否独占，是否支持事务（topic模型）
            topic = session.createTopic("topic");
            // 创建订阅者
            subscriber = session.createSubscriber(topic);
            // 接收消息，会阻塞线程
            message = subscriber.receive();
            // 打印消息
            System.out.println("收到消息：" + ((TextMessage) message).getText());
        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            try {
                // 关闭资源
                if (subscriber != null) {
                    subscriber.close();
                }
                if (session != null) {
                    session.close();
                }
                if (connection != null) {
                    connection.close();
                }
            } catch (JMSException e) {
                e.printStackTrace();
            }
        }
    }
}
```

注意 ==junit 不支持多线程测试==，需要使用 main 方法执行测试

```java
package com.shubao.mq.activemq.topic;

/**
 * @version 1.0
 * @program: spring
 * @description: Topic模式测试类
 * @author: chris
 * @create: 2022-04-21 11:03
 * @since JDK1.8
 **/
public class ActiveMQTest {

    public static void main(String[] args) {
        MySubscriber subscriber = new MySubscriber();
        Thread t1 = new Thread(subscriber);
        Thread t2 = new Thread(subscriber);
        t1.start();
        t2.start();
    }
}
```

启动程序后可以从管理面板看到该 topic 下有两个订阅者

![img](https://app.yinxiang.com/shard/s10/res/7eb93ed8-6261-48ef-b45b-c06f8053e104/523443a72c1ea5b8a7ba4f557f2b8c3a.jpg)

#### 5.2.3 第三部分：创建主题发布者 MyPublisher

创建 MyPublish 类

```java
package com.shubao.mq.activemq.topic;

import org.apache.activemq.ActiveMQConnectionFactory;

import javax.jms.*;

/**
 * @version 1.0
 * @program: spring
 * @description: 主题发布者
 * @author: chris
 * @create: 2022-04-21 11:07
 * @since JDK1.8
 **/
public class MyPublisher {

    // 定义连接工厂
    TopicConnectionFactory factory;

    // 定义连接
    TopicConnection connection;

    // 定义会话
    TopicSession session;

    // 定义发布者
    TopicPublisher publisher;

    // 定义主题
    Topic topic;

    // 定义消息
    Message message;

    public void publishTopic(String topicName, String publishText) {
        try {
            // 创建连接工厂
            factory = new ActiveMQConnectionFactory("tcp://localhost:61616");
            // 通过连接工厂创建连接
            connection = factory.createTopicConnection();
            // 启动连接
            connection.start();
            // 创建会话
            session = connection.createTopicSession(false, TopicSession.AUTO_ACKNOWLEDGE);
            // 创建主题
            topic = session.createTopic(topicName);
            // 创建发布者
            publisher = session.createPublisher(topic);
            // 创建消息
            message = session.createTextMessage(publishText);
            // 发送消息
            publisher.send(message);
        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            try {
                // 关闭资源
                if (null != publisher) {
                    publisher.close();
                }
                if (null != session) {
                    session.close();
                }
                if (null != connection) {
                    connection.close();
                }
            } catch (JMSException e) {
                e.printStackTrace();
            }
        }
    }
}
```

新增测试方法，发布主题消息

```java
package com.shubao.mq.activemq.topic;

import org.junit.Test;

/**
 * @version 1.0
 * @program: spring
 * @description: 发布Topic消息测试类
 * @author: chris
 * @create: 2022-04-21 11:18
 * @since JDK1.8
 **/
public class PublisherTest {

    @Test
    public void topicPublishTest() {
        MyPublisher publisher = new MyPublisher();
        publisher.publishTopic("topic", "hello, topic");
    }
}
```

#### 5.2.4 第四部分：执行测试

执行 topicPublisherTest，可以看到订阅者立即收到了消息

![img](https://app.yinxiang.com/shard/s10/res/f2078f97-4c7e-4c8e-ba43-24c470248206/31f1441e8725ffbd6523ddf15f63d0e0.jpg)

同时在管理页面也能看到一条消息进入，被读取了两次。

![img](https://app.yinxiang.com/shard/s10/res/eb6a652f-51cb-439b-995f-065c893be329/bf6562f900272d674d66f13010f90f16.jpg)

## 6 ActiveMQ持久化

当队列中有未被消费的消息时，我们重新启动ActiveMQ服务器后，发现消息仍然在队列中。

ActiveMQ 是支持持久化的，可以永久保存消息。消息是保存在内存中的。当内存空间不足，或者ActiveMQ服务关闭的时候，消息会被持久化到磁盘上。被消费的时候，再加载到内存空间中。

ActiveMQ持久化方式在 `activemq/conf/activemq.xml` 中指定

### 6.1 kahadb 方式

kahadb 方式是 ActiveMQ 默认的持久化策略。不会保存已经被消费过的消息。从配置文件中可以看到默认的存储地址，也就是 `/usr/local/activemq/data/kahadb`

![image-20220421122020902](images/image-20220421122020902.png)

### 6.2 AMQ方式（已过时）

5.3 版本之前，现在已经过时，不考虑。

### 6.3 JDBC持久化方式

ActiveMQ 可以将数据持久化到数据库中，支持使用任意的数据库。

#### 6.3.1 配置步骤说明

1. 创建数据库
2. 添加数据库连接 jar 依赖到 ActiveMQ 服务器
3. 修改 ActiveMQ 配置，创建数据源。
4. 修改 ActiveMQ 配置，修改持久化方式为 jdbc

#### 6.3.2配置步骤

##### 6.3.2.1 第一步：创建数据库

数据库最好不要跟 ActiveMQ 服务器在同一台机器。因为当 cpu 线程资源不足时，往队列中写入消息时，如果数据库上一次持久化还没结束，容易造成线程阻塞。

这里数据库建立在宿主机上，ActiveMQ 服务部署在虚拟机。

##### 6.3.2.2 第二步：添加jar依赖

配置数据源时，是支持连接池的，这里使用 druid 作为连接池。将 jdbc 驱动、druid 的 jar 包上传到 `activemq/lib/` 目录下

![img](https://app.yinxiang.com/shard/s10/res/f5d55b1a-d428-4084-978e-9c7c92187a2d/35b7bdcbdda625f4ed5e4e114e14ad76.jpg)

##### 6.3.2.3 第三步：修改 `activemq/conf/activemq.xml`，创建数据源

注意在 `<broker>` 节点外，创建数据源。

```xml
<bean id="mysql-ds" class="com.alibaba.druid.pool.DruidDataSource" destroy-method="close">
    <property name="driverClassName" value="com.mysql.cj.jdbc.Driver" />
    <property name="url" value="jdbc:mysql://127.0.0.1:3306/activemq?serverTimezone=UTC&amp;useUnicode=true&amp;characterEncoding=utf8&amp;useSSL=false" />
    <property name="username" value="root" />
    <property name="password" value="1106135" />
    <property name="maxActive" value="10" />
    <property name="poolPreparedStatements" value="true" />
</bean>
```

![image-20220421115732271](images/image-20220421115732271.png)

##### 6.3.2.4 第四步：修改 `/conf/activemq.xml` ，修改为 jdbc 持久化方式

在 `<broker>` 节点内部，注释 kahadb 方式，添加 jdbc 方式。

```xml
<persistenceAdapter>
    <jdbcPersistenceAdapter dataSource="#mysql-ds" createTablesOnStartup="true"/>
</persistenceAdapter>
```

![image-20220421115832777](images/image-20220421115832777.png)

#### 6.3.3 测试

进入 `activemq/bin` 目录，使用命令 `./activemq restart` 重新启动 ActiveMQ。可以看到，数据库中新增了三张表。

运行入门示例中的测试类，往队列中写入一条消息，可以在表activemq_msgs中，看到新写入了一条数据

![image-20220421120024482](images/image-20220421120024482.png)

#### 6.3.4 三张表说明

- activemq_msgs ：存储消息，Queue和Topic都存储在这个表中
- activemq_acks ：用于存储订阅关系。订阅模式下有效
- activemq_lock ：集群模式下，存储主从节点关系

#### 6.3.5 补充说明

jdbc 持久化方式，只要Mysql数据库稳定运行，就能保证队列中消息的安全。安全级别高，但是效率低。因此，在实际开发中，除非是像银行这类对数据安全极高的业务，我们一般都是使用默认持久化方式 kahadb。

## 7 ActiveMQ应用场景

### 7.1 多模块解耦(模块之间消息通讯)

我们判断一个程序的优劣，有一个很重要的指标：高内聚、低耦合。

- 高内聚：同一个模块中，功能是高度紧密的。
- 低耦合：各模块之间，业务尽量不要交叉。

但是有一些业务功能，必须涉及到两个不同的业务，那我们就要想办法，尽量将它们解耦。以我们前面学习的 solr 为例，我们知道 solr 的数据来自数据库。这就意味着，当数据库中的商品发生变化时，我们需要同步更新索引库。这个时候我们就可以使用消息队列模型来解耦，添加添加业务和同步索引库业务。

![img](https://app.yinxiang.com/shard/s10/res/18dbf7b9-0912-49e5-8a5b-f87864e079cd/59175f7ca391dc4894ffc8318207cd01.jpg)

### 7.2 流量削峰（解决并发请求）

![img](https://app.yinxiang.com/shard/s10/res/6bfd8e9d-f568-4599-a860-0ed37b310c63/7f30e7239dbbc2274e1f19efa84f8bcb.jpg)

订单处理，就可以由前端应用将订单信息放到队列，后端应用从队列里依次获得消息处理，高峰时的大量订单可以积压在队列里慢慢处理掉。由于同步通常意味着阻塞，而大量线程的阻塞会降低计算机的性能。

### 7.3 日志处理

日志处理是指将消息队列用在日志处理中，比如Kafka的应用，解决大量日志传输的问题。架构简化如下：

![img](https://app.yinxiang.com/shard/s10/res/69941a8e-44bd-48e7-bd48-2c6668972014/52b799e3f6942ac8e960368d2a80ede9.jpg)

### 7.4 同步业务异步处理

需要：当我们在网站注册的时候，有时候需要认证邮箱或者手机号，这个时候保存数据到数据库之前，需要先等待认证结束。如果说认证程序耗时比较大，会影响影响用户注册的业务。这个时候，我们可以使用消息队列模型，将同步执行的业务，通过队列，变成异步处理。

![img](https://app.yinxiang.com/shard/s10/res/5b72f020-058a-455f-8e70-a6c660f7954b/387a9ba2ea3b172a45726d5d4acd9eb0.jpg)

1. 在保存数据到数据库的时候，只需要将用户的邮箱写入队列，不需要等待邮箱认证程序执行结束，才把数据保存到数据库。
2. 认证程序，通过监听队列，从中获取用户的邮箱地址，发送认证链接。

## 8 Spring 整合 ActiveMQ

### 8.1 必要性

Spring已经整合了jms规范了(spring-jms.jar)，而ActiveMQ是实现了jms规范的。这就意味着Spring整合ActiveMQ是非常方便的。并且Spring-jms，提供了一个JmsTemplate类，用来简化消息读写的业务代码。Spring整合ActivMQ之后，就可以使用该类，简化开发。

### 8.2 需求

使用Spring整合ActiveMQ，模拟限时抢购下的流量削峰问题。

### 8.3 配置步骤

#### 8.3.1 第一部分：创建项目（使用maven）

```
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd"><modelVersion>4.0.0</modelVersion><groupId>org.oza</groupId><artifactId>activemq-demo04-spring</artifactId><version>0.0.1-SNAPSHOT</version><packaging>war</packaging><dependencies><!-- activemq --><dependency><groupId>org.apache.activemq</groupId><artifactId>activemq-all</artifactId><version>5.15.9</version></dependency><dependency><groupId>org.apache.activemq</groupId><artifactId>activemq-pool</artifactId><version>5.15.9</version></dependency><!-- spring jms --><dependency><groupId>org.springframework</groupId><artifactId>spring-jms</artifactId><version>5.1.8.RELEASE</version></dependency><dependency><groupId>org.springframework</groupId><artifactId>spring-webmvc</artifactId><version>5.1.8.RELEASE</version></dependency><!-- jsp相关 --><dependency><groupId>javax.servlet</groupId><artifactId>jstl</artifactId><version>1.2</version></dependency><dependency><groupId>javax.servlet</groupId><artifactId>javax.servlet-api</artifactId><version>3.1.0</version><scope>provided</scope></dependency><dependency><groupId>javax.servlet.jsp</groupId><artifactId>javax.servlet.jsp-api</artifactId><version>2.2.1</version><scope>provided</scope></dependency><!-- jms api --><dependency><groupId>javax.jms</groupId><artifactId>javax.jms-api</artifactId><version>2.0.1</version></dependency></dependencies></project>
```

#### 8.3.2 第二部分：spring整合springmvc

##### 8.3.2.1 第一步：修改web.xml，配置springmvc核心控制器

```
<?xml version="1.0" encoding="UTF-8"?><web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://java.sun.com/xml/ns/javaee" xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd" version="2.5"><display-name>activemq-demo04-spring</display-name><filter><filter-name>characterEncodingFilter</filter-name><filter-class>org.springframework.web.filter.CharacterEncodingFilter</filter-class><init-param><param-name>encoding</param-name><param-value>UTF-8</param-value></init-param></filter><filter-mapping><filter-name>characterEncodingFilter</filter-name><url-pattern>/*</url-pattern></filter-mapping><servlet><servlet-name>dispatcherServlet</servlet-name><servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class><init-param><param-name>contextConfigLocation</param-name><param-value>classpath:spring*.xml</param-value></init-param><load-on-startup>1</load-on-startup></servlet><servlet-mapping><servlet-name>dispatcherServlet</servlet-name><url-pattern>/</url-pattern></servlet-mapping></web-app>
```

#### 8.3.2.2 第二步：配置springmvc.xml核心配置文件

```
<?xml version="1.0" encoding="UTF-8"?><beans xmlns="http://www.springframework.org/schema/beans"xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"xmlns:context="http://www.springframework.org/schema/context"xmlns:mvc="http://www.springframework.org/schema/mvc"xmlns:jms="http://www.springframework.org/schema/jms"xsi:schemaLocation="http://www.springframework.org/schema/jms http://www.springframework.org/schema/jms/spring-jms-4.3.xsdhttp://www.springframework.org/schema/mvc http://www.springframework.org/schema/mvc/spring-mvc-4.3.xsdhttp://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsdhttp://www.springframework.org/schema/context http://www.springframework.org/schema/context/spring-context-4.3.xsd"><context:component-scan base-package="org.oza.activemq"/><mvc:annotation-driven/></beans>
```

##### 8.3.2.3 第三步：创建相关jsp页面

订单页面：order.jsp

```
<%@ page language="java" contentType="text/html; charset=UTF-8"pageEncoding="UTF-8"%><!DOCTYPE html><html><head><meta charset="UTF-8"><title>Insert title here</title></head><body><form action="save" method="post">用户编号：<input type="text" name="userId"><br>订单金额：<input type="text" name="price"><br><input type="submit" value="提交"></form></body></html>
```

结果页面：success.jsp

```
<%@ page language="java" contentType="text/html; charset=UTF-8"pageEncoding="UTF-8"%><!DOCTYPE html><html><head><meta charset="UTF-8"><title>Insert title here</title></head><body>订单提交成功!!!请稍后去结算中心支付。。。</body></html>
```

##### 8.3.2.4 第四步：java代码实现

创建 Order 类

```
package org.oza.activemq.pojo;import java.io.Serializable;public class Order implements Serializable{private static final long serialVersionUID = 3622062034498580108L;private Integer id;private Integer userId;private Float price;public Integer getId() {return id;}public void setId(Integer id) {this.id = id;}public Integer getUserId() {return userId;}public void setUserId(Integer userId) {this.userId = userId;}public Float getPrice() {return price;}public void setPrice(Float price) {this.price = price;}@Overridepublic String toString() {return "Order [id=" + id + ", userId=" + userId + ", price=" + price + "]";}}
```

创建 OrderController 类

```
package org.oza.activemq.controller;import org.oza.activemq.pojo.Order;import org.oza.activemq.producer.OrderProducer;import org.springframework.beans.factory.annotation.Autowired;import org.springframework.stereotype.Controller;import org.springframework.web.bind.annotation.RequestMapping;@Controllerpublic class OrderController {@Autowiredprivate OrderProducer producer;@RequestMapping("/save")public String save(Order order) {System.out.println("当前提交的订单用户是:" + order.getUserId() + ",订单金额:" + order.getPrice());return "/success.jsp";}}
```

##### 8.3.2.5 第五步：整合测试

访问 order 页面下订单，确定 springmvc 正常工作，然后进行下一步。

#### 8.3.3 第三部分：Spring整合ActiveMQ

##### 8.3.3.1 第一步：创建消息生成者 OrderProducer

在这里，我们注入 JmsTemplate 类，来简化代码。另外要注意：

1. ActiveMQ 处理对象时，对象必须实现序列化。
2. 匿名内部类访问外部类属性，该属性需要用final修饰。

```
package org.oza.activemq.producer;import javax.jms.JMSException;import javax.jms.Message;import javax.jms.Session;import org.oza.activemq.pojo.Order;import org.springframework.beans.factory.annotation.Autowired;import org.springframework.jms.core.JmsTemplate;import org.springframework.jms.core.MessageCreator;import org.springframework.stereotype.Component;@Componentpublic class OrderProducer {@Autowiredprivate JmsTemplate jmsTemplate;//注意：内部类调用外部类属性，需要用final修饰public void sendToMQ(final Order order) {//使用 jmsTemplate 进行发送消息，参数一是队列名；参数二是一匿名内部类，指定生成消息的方式jmsTemplate.send("order-mq", new MessageCreator() {public Message createMessage(Session session) throws JMSException {Message message = session.createObjectMessage(order);return message;}});}}
```

##### 8.3.3.2 第二步：创建消息消费者OrderListener类

这里使用监听器模式

```
package org.oza.activemq.listener;import javax.jms.Message;import javax.jms.MessageListener;import javax.jms.ObjectMessage;import org.oza.activemq.pojo.Order;import org.springframework.stereotype.Component;@Componentpublic class OrderListener implements MessageListener {public void onMessage(Message message) {ObjectMessage oMsg = (ObjectMessage)message;try {Order order = (Order)oMsg.getObject();System.out.println("当前提交的订单用户是:"+order.getUserId()+",订单金额:"+order.getPrice());} catch (Exception e) {e.printStackTrace();}}}
```

##### 8.3.3.3 第三步：spring整合ActiveMQ

修改 springmvc 的配置文件，添加整合 ActiveMQ 配置

```
<?xml version="1.0" encoding="UTF-8"?><beans xmlns="http://www.springframework.org/schema/beans"xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"xmlns:context="http://www.springframework.org/schema/context"xmlns:mvc="http://www.springframework.org/schema/mvc"xmlns:jms="http://www.springframework.org/schema/jms"xsi:schemaLocation="http://www.springframework.org/schema/jms http://www.springframework.org/schema/jms/spring-jms-4.3.xsdhttp://www.springframework.org/schema/mvc http://www.springframework.org/schema/mvc/spring-mvc-4.3.xsdhttp://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsdhttp://www.springframework.org/schema/context http://www.springframework.org/schema/context/spring-context-4.3.xsd"><context:component-scan base-package="org.oza.activemq"/><mvc:annotation-driven/><!-- 1、配置activemq连接工厂 使用连接池好处：链接只需要初始化一次，每次要使用的时候，直接从连接池获取，用完之后还给连接池。省去了每次创建、销毁连接的时间。--><bean name="pooledConnectionFactory" class="org.apache.activemq.pool.PooledConnectionFactory"><property name="connectionFactory"><bean class="org.apache.activemq.ActiveMQConnectionFactory"><property name="brokerURL" value="tcp://192.168.125.87:61616"/><property name="userName" value="admin"/><property name="password" value="admin"/><property name="trustAllPackages" value="true"/></bean></property><property name="maxConnections" value="20"/></bean><!-- 2、spring整合activemq链接工厂 可以缓存session。--><bean name="cachingConnectionFactory" class="org.springframework.jms.connection.CachingConnectionFactory"><property name="targetConnectionFactory" ref="pooledConnectionFactory"/><property name="sessionCacheSize" value="5"/></bean><!-- 3、spring整合消息操作对象JmsTemplate 使用jmsTemplate可以简化代码，不需要自己去创建消息的发送对象。--><bean name="jmsTemplate" class="org.springframework.jms.core.JmsTemplate"><propertyname="connectionFactory" ref="cachingConnectionFactory"/></bean><!-- 4、spring加载监听器 acknowledge="auto"表示消息获取之后，自动出队列container-type表示的容器的类型 default|simpledefault:支持session缓存。--><jms:listener-container acknowledge="auto" container-type="default" destination-type="queue" connection-factory="cachingConnectionFactory"><!-- 指定监听器destination="order-mq"指定监听的是哪一个队列ref="orderListener" 指定监听器对象使用注解的时候，对象的名称是类名首字母小写 --> <jms:listener destination="order-mq" ref="orderListener"/></jms:listener-container></beans>
```

##### 8.3.3.4 第四步：修改OrderController类

```
package org.oza.activemq.controller;import org.oza.activemq.pojo.Order;import org.oza.activemq.producer.OrderProducer;import org.springframework.beans.factory.annotation.Autowired;import org.springframework.stereotype.Controller;import org.springframework.web.bind.annotation.RequestMapping;@Controllerpublic class OrderController {@Autowiredprivate OrderProducer producer;@RequestMapping("/save")public String save(Order order) {//System.out.println("当前提交的订单用户是:" + order.getUserId() + ",订单金额:" + order.getPrice());producer.sendToMQ(order);return "/success.jsp";}}
```

### 8.4 整合测试

重新启动项目，提交多个订单，可以看到控制台持续输出，测试成功。

![img](https://app.yinxiang.com/shard/s10/res/b5d2f35f-4efb-48ef-8e4b-3aca125b1462/433cb29f2a156911203ff8b5d0750c8a.jpg)