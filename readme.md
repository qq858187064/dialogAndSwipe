#兼容多端的两个组件
##这个demo中其实含有两个功能组件：
###、弹出框组件pop.js
######1、pop组件是一个更轻量的弹出框组件，
传入参数是1个或多个元素id、name， 也可以是对象的数组、集合，<br />
此时需要在传入之前设置对象的p属性，如	fs.p={ box: "dw", bg: "dbg", w: 480, h: 320}; <br />
多个元素时用逗号","分隔，但传入nm时需以"nm”后缀，即"XXXnm"；<br />
 可在元素p属性中设置需要的属性，<br />
如 p="box:'dw',bg:'dbg',w:800,h:640,url:'/part/my/scene'"<br />
 *box：弹出元素id或对象；<br />
 trig：触发弹出的元素，与box属性互斥 <br />
ct：使用与其它实例共用的弹出容器的弹出内容元素 <br />
bg：弹出元素背景元素id或对象；<br />
 tit：指定弹出框标题元素id,该属性缺省时，弹出元素标题列显示值是该元素的innerText，而不需要标题列时请将该属性值设为0
 w、h：用于指定的数字将设为其宽度和高度，单位是px,而用0代表auto<br />
 url：弹出元素内容异步获取时所需要的url；<br />
 fc：用于指定弹出后需要焦点的元素id<br />
 img：用于指定弹预览图片的id <br />
js：当异步获取内容后需要引入的js [考虑将js可以设置成需要引入的js，css则是需要的css，或者在返回分部页时约定对应css和js的传递] 
配置定义在触发元素的p属性中，但当触发元素为集合时，<br />
如弹出图片预览，该集合的弹出框box，此时配置属性p写在box上。<br />
######2、是图片预览切换组件swipe.js html中的p属性中
 s: 用于设置切换源,目前仅考虑图片，未来可扩展<br />
v:用于指定显示媒体的窗口