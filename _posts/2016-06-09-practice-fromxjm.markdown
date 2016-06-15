---
layout: post
title:  "js实现萧井陌python教学题"
date:   2016-06-09 19:45:31 +0530
categories: ["2016"]
tag: ["#技能基础"]
---
在知乎看到萧大神计划做python培训的消息，并放出了5道编程基础测试题，便随手拿来用js写了下答案，算作一个小练习：

    // 题 1
    // 检查密码规则合法性
    // 考察基本编码能力和字符串处理

    // 给定一个字符串，用以下规则检查合法性
    // 完全符合返回 true，否则返回 false
    // 1，第一位是字母
    // 2，只能包含字母、数字、下划线
    // 3，只能字母或数字结尾
    // 4，最小长度2
    // 5，最大长度10

    function valid_password(str) {
      if (str.match(/^[a-zA-Z][a-zA-Z0-9_]{0,8}[a-zA-Z0-9]$/)) {
        console.log(true)
      } else {
        console.log(false)
      }
    }

    // 题 2
    // 返回 100 内的素数数组
    // 考察基本的循环和选择概念、数组的使用

    function prime_numbers() {
      var arr = [];
      function isPrime(number) {
        for (i of arr) {
          if (number % i === 0) {
            return false;
          }
        }
        return true;
      }
      for (var i = 3; i < 100; i++) {
        if (isPrime(i)) {
          arr.push(i)
        }
      }
      console.log(arr)
    }

    // 题 3
    // 给定一个只包含字母的字符串，返回单个字母出现的次数
    // 考察字典的概念和使用
    // 返回值为一个对象，格式如下
    // 参数 "hello"
    // 返回值 {h: 1, e: 1, l: 2, o: 1}

    function letter_count(str) {
      var obj = {};
      for (var i = 0; i < str.length; i++) {
        var letter = str.substring(i, i+1)
        obj[letter] = obj[letter] || 0
        obj[letter] += 1
      }
      console.log(obj)
    }

    // 题 4
    // 给定一个英文句子（一个只有字母的字符串），将句中所有单词变为有且只有首字母大写的形式

    function cap_string(str) {
      return str.replace(/\w\S*/g, function(txt){
        return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
      });
    }
