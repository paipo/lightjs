# lightjs
  一个兼容zepto和jquery，移动端和桌面端都可以使用的简单轻量的常用功能脚本库
  可适用于一般常用的广告单页，活动单页，功能单一页面。优点，不需要引用过大的前端框架就能实现基本的提示，弹窗，计算，存储，浏览器判断等功能
## 功能 
* 页面提示与窗体 
* HashTable
* 时间日期操作
* 浏览器判断
* url操作与cookie
* 按钮点击与选择判断

## 页面提示与窗体
### 确认与取消框
![image](https://raw.githubusercontent.com/paipo/screenshots/master/tc.png)
```javascript
zyalert.showconfirm('提示的标题', '确认按钮文本', '取消按钮文本', function () {
                //点击确认了
            }, function () {
                //点击取消了
});
```
### 等待提示框
![image](https://raw.githubusercontent.com/paipo/screenshots/master/jz.png)
```javascript
zyalert.showloading(' 稍等');
```
### 成功提示框
![image](https://raw.githubusercontent.com/paipo/screenshots/master/cg.png)
```javascript
zyalert.showok(' 成功');
```
### 失败提示框
![image](https://raw.githubusercontent.com/paipo/screenshots/master/cw.png)
```javascript
zyalert.showero(' 失败');
```
### 普通提示框 2.5 秒后关闭
![image](https://raw.githubusercontent.com/paipo/screenshots/master/ts.png)
```javascript
zyalert.showtext('你好啊！');
```
### 普通提示框 5 秒后关闭
![image](https://raw.githubusercontent.com/paipo/screenshots/master/ts.png)
```javascript
zyalert.showtextlong('你好啊！');
```
### 关闭提示框
```javascript
zyalert.closealert();
```
### 提示后自动跳转到指定页面
```javascript
zyalert.alertAndBack('设置成功了！马上为您跳转','www.github.com');
```
### 带选择项目的弹窗
![image](https://raw.githubusercontent.com/paipo/screenshots/master/xz.png)
    列表对象必须包含 text 属性，其他属性可以自定义多个，在回调后可按自定义使用
```javascript
var list = new Array();
var m1 = {
  id: 1,//自定义属性
  type: 2,//自定义属性
  text : 'JEPP'//必须属性text
}
list.push(m1);
var m2 = {
  id: 2,
  type: 2,
  text: '大众'
}
list.push(m2);
zywindow.title = "选择您的车型";
zywindow.content(list);
zywindow.show();
```
#### 点击后的回调
```javascript
zywindow.clickback = function (o) {
    //回调代码
    var id = o.id;
    var type = o.type;
    var text = o.text;
 }
```

## HashTable
```javascript
var hashdatas = new $.zyhash()
```
### 添加
```javascript
hashdatas.add('key',object);
```
### 获取
```javascript
var object = hashdatas.get('key');
```
### 删除
```javascript
hashdatas.remove('key');
```
### 判断 key 存在
```javascript
hashdatas.containsKey('key');
```
### 判断 value 存在
```javascript
hashdatas.containsValue(object);
```
### 清除
```javascript
hashdatas.clear();
```
### 大小
```javascript
hashdatas.size();
```
### 是否空
```javascript
hashdatas.isEmpty();
```
## 其他功能见代码
