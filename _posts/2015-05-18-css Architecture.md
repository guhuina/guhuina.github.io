---
title:  "漫谈css架构方法"
author: luna
layout: post
categories: 
  - html+css
tags: 
  - css OOCSS SMACSS BEM
---


# 良好的css架构：

 * 预测 ：predictable
 * 复用：reusable
 * 维护：maintainable
 * 延展： scalable

# CSS Methodology

## OOCSS
> Object Oriented CSS

* 两大原则：结构与外观分离，容器与内容分离 

## SMACSS：
> Scalable & Modular Architecture for css


### rule：
* 将结构分类，命名规则，css与html分离
* Base，Layout，Module，State，Theme

### BASE
* css Reset，css Normalize ，no need to use !important

### Layout 

* Header，sidebar，content

### Module

* 页面上可单独存在并且可重复使用的原件
* 定义模块时应避免使用id或标记名称做选择器
* 子模块以原模块名加dash（-）作为名称：.module-title,.module-header,.module-body

## state
* 与layout，module搭配
* 表示layout或module的状态变化
* 由class定义
* 命名规则是。is-*开头
	
	.is-hidden{
		display: none;
	}
	
	.is-error{
		font-weight: 700;
		color: #f00;
	}
	
	
### Theme

* 定义网站主视觉
* 类似Layout，但影响的是网站整体视觉的变化
* class名称通常以.theme-*做开头


## BEM
> Block,Element,Modifier
	
	.{block}__{element}
	.{block}__{element}--{modifier}
	.{block}--{modifier}
	
### Block
* 在页面上独立存在并可重复使用的元件
* 如同SMACSS的Module，Layout
* 每个Block都是独立存在的

### Element
* 为Block的一部分
* 无法独立于Block之外
* 有些Block可能没有Element

### Modifier
* 用来定义Block或Element的状态或属性
* 类似SMACSS的state
* 同一个Block或Element可以允许多组modifier同时存在


