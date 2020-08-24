# HTTP学习随笔

#### 1.GET和POST的区别

- GET

当访问 Web 服务器获取网页数据的时候，使用的几乎都是 Get 方法。在请求消息中表明使用Get方法，然后在URI 中表明文件名，比如是 /manage/index.html。服务器收到消息后，会打开/manage/index.html并读取里面的数据，然后存放于相应消息中并返回给客户端，最后在屏幕中完成呈现。

- POST

当我们在购物填写地址信息，或者填写问卷信息的时候，将内容填写到表格中，然后点击提交这个过程，实际上通常就是采用的POST方式。这样看来，采用POST的方式提交数据，我们需要准备三样东西，分别为：**所提供的方法**，**URL** 和**服务端**。服务器收到请求数据后发送给 URI 所指定的应用程序，然后服务端获取应用程序的执行结果并在响应信息中返回给客户端。



#### 2.

![image-20200818151314306](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20200818151314306.png)



#### 3.响应码

![image-20200818151403941](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20200818151403941.png)