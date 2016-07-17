---

title: JS���-undefined��null
date: 20160717032719
categories: [WEB]
tags: [js]

---

`undefined`��`null`������ûʲô����ֻ���÷��ϴ���ĺ��岻һ�����ˡ�

## ǰ��

Ϊʲô˵��`undefined`��`null`������ûʲô����

ͨ�������������

```js
undefined == null //true
null == undefined //true
```

���⣬�ٿ�����֮ǰ���������ȿ�����һ����ʦ�Ĳ��ͣ��Ա��˽�������ߵ���ʷ��

[��һ�� > undefined��null������](http://www.ruanyifeng.com/blog/2014/03/undefined-vs-null.html)

## ����

* `null`����ʾһ�����ޡ��Ķ���
* `undefined`����ʾһ�����ޡ���ԭʼֵ��

��������2�����壿�������ӣ�

```js
typeof(null) //object
typeof(undefined) //undefined
```

���⣬����ת��ΪNumber�Ľ��Ҳ��һ����

```js
Number(null) // 0
Number(undefined) //NAN
```

> NAN��Not a Number����IEEE������������׼��IEEE 754���ж��壬��ʾһЩ������ֵ��
> INF��Infinity����д����������˼�����磺1/0���������Infinity

## ��;

˵�������ҿ��ܾͷ��Ժ��ˣ���һ����˵ûʲô����������һ����ͨ�������������������Ϸ�����Ǻã�

�ðɣ�������������;���ž�����ΪʲôJs��ô��������ˡ�

����������;��ͬ���� `�׶β�ͬ`��

* `undefined`�����ڱ�������ʱ��
* `null`�����ڱ�����ֵʱ��

����֪�������������͸�ֵ��2����ͬ�׶Σ�ֻ����ʱ������������д���ˣ����磺

```js
var name = 'night';
```

������ʵ���������͸�ֵһ��д�ˣ���ֿ�ʼ������

```js
var name; // ��������
name = 'night'; //������ֵ
```

���ˣ���������������߼��У�������������˵�Ķ��ߵ��� `�׶β�ͬ` ��ʲô��˼��

����������������ӣ�����ܾ���Ȼ�ˣ�

```js
var name;
console.log(name); //undefined
name = 'night';
console.log(name); //night
name = null;
console.log(name); //null
```

��������������ӣ�

* �ȶ���һ���������������δ��ֵ����ô���� `undefined`;
* �����ֵ�ˣ���ô `undefined` ������Ҳ������ˣ�
* �������ֵΪһ�� `null`����ô���Ҳ���� `null` �ˣ�


˵�����������ֻ��ʣ����ö˶˵��Ҹ�ֵһ��Null��������

�ðɣ�����һ�����������ĵ��ˣ�������������������

### ����Null

��Js�У��������ô���ࣺ�����˻������������⣬�������ȫ���Ƕ��󡱡�

������仰�����£�

* �����������ͣ�������undefined,null,number,string,boolean�����˾��ò�Ӧ��object��
* ���еĺ������ɹ��Ϊ����ֻ������������ĺ�������ѭ����ĸҪ��д���ˣ�

���������ô���࣬��ônull��һ�����þ�͹���ˡ�

��һ��������ֵ�������������Ϳ���ֱ�Ӹ�ֵ����ô��Ҫ��ֵһ�����󣬻������һ������ĸ�ֵ������ô���أ�

�Ǿͷ���һ���յĶ���ɣ�����null��

��Ȼ��������ֵΪNull�󣬻�����һ�����ã��Ǿ��Ƿ���JS�����������������������ա�

��JS�У����ǲ��õı�����JS�ᶨ��������������ǰ�һ����������Ϊnullʱ����ʵҲ�͵��ڰ����������Ϊ�����ˣ��������������ˡ�

## �ο�

* [http://www.ruanyifeng.com/blog/2014/03/undefined-vs-null.html](http://www.ruanyifeng.com/blog/2014/03/undefined-vs-null.html)
* [http://stackoverflow.com/questions/5076944/what-is-the-difference-between-null-and-undefined-in-javascript](http://stackoverflow.com/questions/5076944/what-is-the-difference-between-null-and-undefined-in-javascript)
* [Mozilla > ��������](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_Management)




