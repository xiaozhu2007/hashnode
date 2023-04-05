---
title: "jQuery 点击按钮元素移动动画"
seoTitle: "本文实例讲述了 jQuery 使用 animate方法实现控制元素移动。"
seoDescription: "本文实例讲述了 jQuery 使用 animate方法实现控制元素移动。"
datePublished: Tue Feb 28 2023 13:37:11 GMT+0000 (Coordinated Universal Time)
cuid: cleoamhb6001009l09luldnhy
slug: jquery-01
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/VieM9BdZKFo/upload/f8b6eb2aec9af5377ac71670c7d69d57.jpeg

---

本文实例讲述了 jQuery 使用 `animate`方法实现控制元素移动，分享给大家供大家参考。

```xml
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>[实例]jQuery 点击按钮元素移动</title>
    <style type="text/css">
      .box1 {
        width: 100px;
        height: 100px;
        background: pink;
        position: absolute;
      }
      .box2 {
        width: 100px;
        height: 100px;
        background: #00f;
        position: absolute;
        top: 100px;
        left: 50px;
      }
    </style>
    <script type="text/javascript" src="/libs/jquery.min.js"></script>
    <script type="text/javascript">
      $(document).ready(function () {
        $("button").click(function () {
          $(".box1").animate({ left: 500, top: 100 }, 3e3),
            $(".box2").animate({ left: 100, top: 600 }, 3e3);
        });
      });
    </script>
  </head>
  <body>
    <button>按钮</button>
    <div class="box1"></div>
    <div class="box2"></div>
  </body>
</html>
```

%%[post-xxxads]
希望本文所述对大家的 jQuery 程序设计有所帮助。