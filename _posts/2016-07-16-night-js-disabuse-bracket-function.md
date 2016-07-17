---

title: JS���-()���ʽ�ĺ���
date: 20160714050413
categories: [WEB]
tags: [js]

---

JS�о����ܿ��� `(function(){...})()`����ô˫����()������ʲô��˼�أ�

## ����

������������һЩʵ�ʹ������õ���()�����ӡ�

��ʽ�������ģ�

```js
(function(){
    //TODO
})();
```

��Ȼ��jquery�У���ʱ��Ϊ�˱������$��ͻ��Ҳ������ô�ã�

```js
jQuery.noConflict();
(function($){
    //TODO
})(jQuery);
```

## ����


���� `Ecma-262` �� `12.2.10.4�½�` ����䣺

```
ParenthesizedExpression : ( Expression ) 
   1. Return the result of evaluating Expression. This may be of type Reference.
```

�Ҹ��˵���ⷭ�룺

```
Բ�����������ı��ʽ��(���ʽ)

���ؼ�����ʽ�Ľ�����������һ�����á�
```

**���ؼ�����ʽ�Ľ��**

��仰��ô����أ��ٸ����ӣ�

```js
(function(){
    console.log(123456);
});
```

��ӡ����������function�ĺ������ʽ������

```js
function(){
    console.log(123456);
}
```

�����������ӣ������ټ�һ��()����ô��������ִ���������������

```js
(function(){
    console.log(123456);
})();
```

�����123456

���꣺

д�������ҿ��ܻ��ʣ�ΪʲôҪ��ô���أ�

2�����ã�

* ����ִ�к���������self-executing function
* ��������������Ⱦ�Ŀ鼶������

��������ִ�к������ο���֮ǰд����һƬ���£�

* [JS���-functionǰ����+��!�������ַ�](http://www.night123.com/2016/night-js-disabuse-function/)

���⣬����֪��JS��ES6֮ǰ��û�п鼶������ģ���ôͨ������ `(��������)` ����ʽ�����Ա�֤ `()` ������ӵ�ж����������򣬶��ⲿ�޷����ʡ�

> ʲô�ǿ鼶������
> ������һЩ������C���Եı�������У��������ڵ�ÿһ�δ��붼���и��Ե������򣬶��ұ������������ǵĴ����֮���ǲ��ɼ��ġ�
> ���ԡ�JavaScript Ȩ��ָ�ϡ���`3.10.1`�½ڣ���`57ҳ`

���磺

```js
for(var i=0;i<10;i++){
   //TODO
};
console.log(i);
```

���Ϊ��10��Ҳ����˵������for�ж���ı���i����for��������Ȼ��Ч��


**�������һ������**

��仰��ô����أ��ٸ����ӣ�

```js
var obj = {
    name : 'night',
    sayHi : function(){
        console.log('hello ' + this.name);
    }
};
(obj);
```

����������obj�Ķ�����Ҳ�Ͷ�����˵�ģ��Ƕ�obj�����ã���

```js
Object {name: "night"}
    name:"night"
    sayHi:()
    __proto__:Object
```

��Ȼ����������ô����������Ͳ��Զ����˰ɣ�

```js
(obj.sayHi)();//hello night
//ע�⣺(obj.sayHi())()���ǲ���ȷ��Ŷ������
//��Ϊ(obj.sayHi)����ͷ�����һ�����ö��󣬲�����()����ֱ�Ӿ�����Ŷ������Ҫ����()��û���ˡ�
```

�һ��Ƿ����°ɣ�

* (obj) = obj;//������obj������
* (obj.sayHi) = obj.sayHi();//�������ö����Լ���sayHi����

���꣺

`JavaScript �߼�������ƣ������棩` �� `7.2.2 ����this����` ���и����ӣ��������ϸ����ҿ϶���������ˡ�

�������Ȿ��� `183ҳ` ���ս����My Object������Լ�ȥ����

## ����

`(expression)` ����⣺

* ���ؼ�����ʽ�Ľ��
* �����ܷ��ص���һ������

`(expression)()` �����ã�

* ����ִ�к���
* ��������������Ⱦ��������

## �ο�

1. [Ecma-262](http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-262.pdf)
1. [http://stackoverflow.com/questions/4043647/what-does-this-function-a-function-inside-brackets-mean-in-javascript](http://stackoverflow.com/questions/4043647/what-does-this-function-a-function-inside-brackets-mean-in-javascript)
1. [http://stackoverflow.com/questions/440739/what-do-parentheses-surrounding-a-javascript-object-function-class-declaration-m](http://stackoverflow.com/questions/440739/what-do-parentheses-surrounding-a-javascript-object-function-class-declaration-m)

