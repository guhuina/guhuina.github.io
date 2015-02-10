---
title:  "Sass's Function"
author: luna
layout: post
categories: 
  - tools
tags: 
  - sass
---


## Deep Get in Maps	

	@function map-deep-get($map, $keys...) {
    	@each $key in $keys {
        	$map: map-get($map, $key);
    	}
    	@return $map;
	}
## Set Property
	
	@function set-property($element,$property,$value){
        @if $property == default {
            $property: map-get($element, $value);
            @return $property;
        }@else{
            @return $property;
        }
    }

## Set Theme

    @mixin set-theme($obj,$class){
        @each $name, $value in map-deep-get($obj, theme) {
            #{$class}-#{$name} {
                background: nth($value,1);
                color: nth($value,2);
                border-color:nth($value,3);
            }
        }    
    }