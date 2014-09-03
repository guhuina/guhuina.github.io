---
title: Jquery attr(“checked”) 返回checked或undefined 获取选中失效
author: luna
layout: post
categories:
  - jQuery
---
    <input type='checkbox' id='cb'/>
    <script>
    //获取是否选中
    var isChecked = $('#cb').prop('checked');
    //或
    var isChecked = $('#cb').is(":checked");
    //设置选中
    $('#cb').prop('checked',true);
    </script>