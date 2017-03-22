---
layout:     post
title:      "Frontend Interview Question"
subtitle:   "Frontend Interview Question"
date:       2017-03-22
author:     "Asher"
header-img: "home-bg.jpg"
header-mask: 0.3
catalog:    true
tags:
    - Frontend
---

# Lazy Man

```javascript

function _LazyMan(name){
    this.task = [];
    var self = this;
    var fn = (function(n){
        var name = n;
        return function(){
            console.log('Hi This is ' + name + '!');
            self.next();
        }
    })(name)

    this.task.push(fn);
    setTimeout(function(){
        self.next();
    }, 0)
}

_LazyMan.prototype.next = function(){
    var fn = this.task.shift();
    fn && fn();
}

_LazyMan.prototype.eat = function(name){
    var self = this;
    var fn = (function(name){
        return function(){
            console.log('Eat ' + name + '~');
            self.next();
        }
    })(name)
    this.task.push(fn);
    return this;
}

_LazyMan.prototype.sleep = function(time){
    var self = this;
    var fn = (function(time){
        return function(){
            setTimeout(function(){
                console.log('Wake up after ' + time + 's!');
                self.next();
            }, time*1000)
        }
    })(time);
    this.task.push(fn);
    return this;
}


function LazyMan(name){
    return new _LazyMan(name);
}

LazyMan('Hank').sleep(1).eat('sss')

```

# Functional add

```javascript

var puls = (num) => {
	var adder = function() {
		var _args = []
		var _adder = function _adder() {
			[].push.apply(_args, [].slice.call(arguments))

			return _adder
		}

		_adder.toString = function() {
			return _args.reduce(function(a, b) {
				return a + b
			})
		}

		return _adder
	}

	return adder()(num)
}

puls(1)(2)

```
