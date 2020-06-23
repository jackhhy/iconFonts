# iconFonts 图标选择器

#### 介绍
iconFonts图标选择器， [layui](https://www.layui.com/doc/element/icon.html) 图标 140个

#### 使用教程

1. 加载iconFonts

```
 layui.config({
        base: "{__FRAME_PATH}js/"  // 配置你下载的iconFonts文件夹路径
    }).extend({
        IconFonts: 'iconFonts/iconFonts',
    });

```


2. layui 使用iconFonts

```
 layui.use(['element','form', 'jquery', 'IconFonts'], function () {
        var element = layui.element;
        var form = layui.form;
        var $ = layui.jquery;
        var IconFonts=layui.IconFonts;

        //图标选择器
        IconFonts.render({
           // 选择器，推荐使用input
                elem: '#iconFonts',
                // 数据类型：fontClass/unicode，推荐使用fontClass
                type: 'fontClass',
                // 是否开启搜索：true/false，默认true
                search: true,
                // 是否开启分页：true/false，默认true
                page: true,
                // 每页显示数量，默认12
                limit: 12,
                // 点击回调
                click: function (data) {
                    console.log(data);
                }
                // 渲染成功后的回调
                success: function(d) {
                    console.log(d);
                }
        });

       /**
         * 默认选选中图标
         */
        IconFonts.checkIcon("iconFonts","layui-icon-star");

```

3. html

```
 <div class="layui-form-item">
      <label class="layui-form-label">选择图标</label>
           <div class="layui-input-block">
               <input type="text" name="icon" id="iconFonts"  lay-filter="iconFonts" value=""   class="layui-input">
           </div>
  </div>
```

4. 项目截图
（1、layui 图标）
![输入图片说明](https://images.gitee.com/uploads/images/2019/0705/112511_b95f4287_1513275.png "屏幕截图.png")


#### 特别鸣谢

1. [font-awesome](https://fontawesome.com/?from=io)
2. [layui](https://www.layui.com/)
3. [font-awesome-cdn](https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css)
4. [iconPicker选择器](https://fly.layui.com/extend/iconPicker/)


#### 疑问联系

1. 使用 [iconFonts](https://gitee.com/luckygyl/iconFonts) 过程中有任何问题请联系：jackhhy520@qq.com
   或者在下方评论留言。
2. 如果觉得不错，点个  **Star**  再走也不迟呀！