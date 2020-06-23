# iconHhysFa 图标选择器

#### 介绍
iconHhysFa图标选择器， [layui](https://www.layui.com/doc/element/icon.html) 图标 140个，
font-awesome 有786个图标。

#### 使用教程

1. 加载iconHhysFa

```
     layui.config({
            base: './module/'
        }).extend({
            iconHhysFa: 'iconHhys/iconHhysFa'
        });


```

2. 静态页面

```
<div class="layui-form">
        <blockquote class="layui-elem-quote">
       layui图标实例
       <a class="layui-btn layui-btn-normal" href="https://gitee.com/luckygyl/iconFonts" target="_blank">码云地址</a>
        </blockquote>   
        <div class="layui-form-item">
            <label for="" class="layui-form-label">默认图标：</label>
            <div class="layui-input-block">
                <input type="text" id="iconHhysFa" lay-filter="" class="hide">
            </div>
        </div>
        <div class="layui-form-item">
            <label for="" class="layui-form-label">自定义图标：</label>
            <div class="layui-input-block">
                <input type="text" id="iconHhysFa2" value="layui-icon-face-smile-fine" lay-filter="iconHhysFa2" class="hide">
            </div>
        </div>
        
         <div class="layui-form-item">
            <label for="" class="layui-form-label">js自定义选中图标：</label>
            <div class="layui-input-block">
                <input type="text" id="iconHhysFa3" value="" lay-filter="iconHhysFa3" class="hide">
            </div>
        </div>


  <blockquote class="layui-elem-quote">
       font-awesome图标实例
        </blockquote>   
        <div class="layui-form-item">
            <label for="" class="layui-form-label">默认图标：</label>
            <div class="layui-input-block">
                <input type="text" id="iconHhys" lay-filter="iconHhys" class="hide">
            </div>
        </div>
        <div class="layui-form-item">
            <label for="" class="layui-form-label">自定义图标：</label>
            <div class="layui-input-block">
                <input type="text" id="iconHhys2" value="fa-home" lay-filter="iconHhys2" class="hide">
            </div>
        </div>
        
         <div class="layui-form-item">
            <label for="" class="layui-form-label">js自定义选中图标：</label>
            <div class="layui-input-block">
                <input type="text" id="iconHhys3" value="" lay-filter="iconHhys3" class="hide">
            </div>
        </div>

```

3. js

```
 <script>
            layui.use(['iconHhysFa', 'form', 'layer'], function() {
                var iconHhysFa = layui.iconHhysFa,
                    form = layui.form,
                    layer = layui.layer,
                    $ = layui.$;

                iconHhysFa.render({
                    // 选择器，推荐使用input
                    elem: '#iconHhysFa',
                    // 数据类型：fontClass/awesome，推荐使用fontClass
                    type: 'fontClass',
                    // 是否开启搜索：true/false，默认true
                    search: true,
                    // 是否开启分页：true/false，默认true
                    page: true,
                    // 每页显示数量，默认12
                    limit: 12,
                    url: '',
                    // 点击回调
                    click: function(data) {
                        console.log(data);
                    },
                    // 渲染成功后的回调
                    success: function(d) {
                        console.log(d);
                    }
                });

                iconHhysFa.render({
                    // 选择器，推荐使用input
                    elem: '#iconHhysFa2',
                    // 数据类型：fontClass/awesome，推荐使用fontClass
                    type: 'fontClass',
                    // 是否开启搜索：true/false
                    search: true,
                    url: '',
                    // 是否开启分页
                    page: true,
                    // 每页显示数量，默认12
                    limit: 12,
                    // 点击回调
                    click: function(data) {
                        console.log(data);
                    },
                    // 渲染成功后的回调
                    success: function(d) {
                        console.log(d);
                    }
                });


               iconHhysFa.render({
                    // 选择器，推荐使用input
                    elem: '#iconHhysFa3',
                    // 数据类型：fontClass/awesome，推荐使用fontClass
                    type: 'fontClass',
                    // 是否开启搜索：true/false，默认true
                    search: true,
                    // 是否开启分页：true/false，默认true
                    page: true,
                    // 每页显示数量，默认12
                    limit: 12,
                    url: '',
                    // 点击回调
                    click: function(data) {
                        console.log(data);
                    },
                    // 渲染成功后的回调
                    success: function(d) {
                        console.log(d);
                    }
                });

               //js 操作自定义选中图标
               iconHhysFa.checkIcon("iconHhysFa3","layui-icon-rate");
               
               ////////font-awesome图标实例
               
                 iconHhysFa.render({
                    // 选择器，推荐使用input
                    elem: '#iconHhys',
                    // 数据类型：fontClass/awesome，推荐使用fontClass
                    type: 'awesome',
                    // 是否开启搜索：true/false，默认true
                    search: true,
                    // 是否开启分页：true/false，默认true
                    page: true,
                    // 每页显示数量，默认12
                    limit: 12,
                    // fa 图标接口
                    url: './font-awesome/less/variables.less',
                    // 点击回调
                    click: function(data) {
                        console.log(data);
                    },
                    // 渲染成功后的回调
                    success: function(d) {
                        console.log(d);
                    }
                });


                iconHhysFa.render({
                    // 选择器，推荐使用input
                    elem: '#iconHhys2',
                    // 数据类型：fontClass/awesome，推荐使用fontClass
                    type: 'awesome',
                    // 是否开启搜索：true/false
                    search: true,
                    // fa 图标接口
                    url: './font-awesome/less/variables.less',
                    // 是否开启分页
                    page: true,
                    // 每页显示数量，默认12
                    limit: 12,
                    // 点击回调
                    click: function(data) {
                        console.log(data);
                    },
                    // 渲染成功后的回调
                    success: function(d) {
                        console.log(d);
                    }
                });


               iconHhysFa.render({
                    // 选择器，推荐使用input
                    elem: '#iconHhys3',
                    // 数据类型：fontClass/awesome，推荐使用fontClass
                    type: 'awesome',
                    // 是否开启搜索：true/false，默认true
                    search: true,
                    // 是否开启分页：true/false，默认true
                    page: true,
                    // 每页显示数量，默认12
                    limit: 12,
                    // fa 图标接口
                    url: './font-awesome/less/variables.less',
                    // 点击回调
                    click: function(data) {
                        console.log(data);
                    },
                    // 渲染成功后的回调
                    success: function(d) {
                        console.log(d);
                    }
                });

               //js 操作自定义选中图标
               iconHhysFa.checkAwesome("iconHhys3","fa-address-book");

            });
        </script>

```


4. 项目截图
  layui 的
  ![输入图片说明](https://images.gitee.com/uploads/images/2020/0623/153917_0171914a_1513275.png "微信截图_20200623153946.png")
  
  font-awesome的
  ![输入图片说明](https://images.gitee.com/uploads/images/2020/0623/154006_6c026cba_1513275.png "_20200623154040.png")



#### 特别鸣谢

1. [font-awesome](https://fontawesome.com/?from=io)
2. [layui](https://www.layui.com/)
3. [font-awesome-cdn](https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css)
4. [iconPicker选择器](https://fly.layui.com/extend/iconPicker/)


#### 疑问联系

1. 使用 [iconHhysFa](https://gitee.com/luckygyl/iconFonts) 过程中有任何问题请联系：jackhhy520@qq.com
   或者在下方评论留言。
2. 如果觉得不错，点个  **Star**  再走也不迟呀！