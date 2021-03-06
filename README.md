# ts-partten
使用typescript实现设计模式演示代码

### 观察者模式 observer.ts
```
定义：观察者模式定义一个一对多的依赖关系，让一个或多个观察者对象监听一个主题对象。这样一来，当被监听的主题对象发生改变时，需要通知相应的观察者，使这些观察者能够自动更新。
```
- 主题（subject），是被观察者观察的对象
    * 持有那些监听这个主题的观察者的引用，即observerList
    * 支持增加和删除观察者，即 addObserve & removeObaser
    * 主题发生改变是去通知观察者，即 notify
- 观察者
    * 对主题发出的通知，需要进行具体的处理，即 update

- 松耦合
    * 观察者增加或删除无需修改主题的代码，只需调用主题对应的增加或者删除的方法即可。
    * 主题只负责通知观察者，但无需了解观察者如何处理通知。举个例子，送奶站只负责送递牛奶，不关心客户是喝掉还是洗脸。
    * 观察者只需等待主题通知，无需观察主题相关的细节。还是那个例子，客户只需关心送奶站送到牛奶，不关心牛奶由哪个快递人员，使用何种交通工具送达
- 由于数主题发生改变是，对任何的观察者是一视同仁的，所以正常情况下不会出现观察者无法被通知的情况

### 单例模式 singleton.ts
```
定义：单例模式是创建一个全局唯一的实体对象，一旦创建该对象后，后续创建行为将失效。
```
- 特点
    * 单例模式类只能有一个实例
    * 单例模式类必须自己穿件自己的唯一实例
    * 单例模式类必须给外部提供访问这一实例的方法

