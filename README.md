<!DOCTYPE html>
<html lang="en">
<head>
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta charset="utf-8"><script type="text/javascript">(window.NREUM||(NREUM={})).loader_config={xpid:"VwMGVVZSGwIIUFBQDwU="};window.NREUM||(NREUM={}),__nr_require=function(t,e,n){function r(n){if(!e[n]){var o=e[n]={exports:{}};t[n][0].call(o.exports,function(e){var o=t[n][1][e];return r(o?o:e)},o,o.exports)}return e[n].exports}if("function"==typeof __nr_require)return __nr_require;for(var o=0;o<n.length;o++)r(n[o]);return r}({QJf3ax:[function(t,e){function n(t){function e(e,n,a){t&&t(e,n,a),a||(a={});for(var c=s(e),f=c.length,u=i(a,o,r),d=0;f>d;d++)c[d].apply(u,n);return u}function a(t,e){f[t]=s(t).concat(e)}function s(t){return f[t]||[]}function c(){return n(e)}var f={};return{on:a,emit:e,create:c,listeners:s,_events:f}}function r(){return{}}var o="nr@context",i=t("gos");e.exports=n()},{gos:"7eSDFh"}],ee:[function(t,e){e.exports=t("QJf3ax")},{}],3:[function(t){function e(t){try{i.console&&console.log(t)}catch(e){}}var n,r=t("ee"),o=t(1),i={};try{n=localStorage.getItem("__nr_flags").split(","),console&&"function"==typeof console.log&&(i.console=!0,-1!==n.indexOf("dev")&&(i.dev=!0),-1!==n.indexOf("nr_dev")&&(i.nrDev=!0))}catch(a){}i.nrDev&&r.on("internal-error",function(t){e(t.stack)}),i.dev&&r.on("fn-err",function(t,n,r){e(r.stack)}),i.dev&&(e("NR AGENT IN DEVELOPMENT MODE"),e("flags: "+o(i,function(t){return t}).join(", ")))},{1:23,ee:"QJf3ax"}],4:[function(t){function e(t,e,n,i,s){try{c?c-=1:r("err",[s||new UncaughtException(t,e,n)])}catch(f){try{r("ierr",[f,(new Date).getTime(),!0])}catch(u){}}return"function"==typeof a?a.apply(this,o(arguments)):!1}function UncaughtException(t,e,n){this.message=t||"Uncaught error with no additional information",this.sourceURL=e,this.line=n}function n(t){r("err",[t,(new Date).getTime()])}var r=t("handle"),o=t(6),i=t("ee"),a=window.onerror,s=!1,c=0;t("loader").features.err=!0,t(5),window.onerror=e;try{throw new Error}catch(f){"stack"in f&&(t(1),t(2),"addEventListener"in window&&t(3),window.XMLHttpRequest&&XMLHttpRequest.prototype&&XMLHttpRequest.prototype.addEventListener&&window.XMLHttpRequest&&XMLHttpRequest.prototype&&XMLHttpRequest.prototype.addEventListener&&!/CriOS/.test(navigator.userAgent)&&t(4),s=!0)}i.on("fn-start",function(){s&&(c+=1)}),i.on("fn-err",function(t,e,r){s&&(this.thrown=!0,n(r))}),i.on("fn-end",function(){s&&!this.thrown&&c>0&&(c-=1)}),i.on("internal-error",function(t){r("ierr",[t,(new Date).getTime(),!0])})},{1:10,2:9,3:7,4:11,5:3,6:24,ee:"QJf3ax",handle:"D5DuLP",loader:"G9z0Bl"}],5:[function(t){t("loader").features.ins=!0},{loader:"G9z0Bl"}],6:[function(t){function e(){}if(window.performance&&window.performance.timing&&window.performance.getEntriesByType){var n=t("ee"),r=t("handle"),o=t(1),i=t(2);t("loader").features.stn=!0,t(3),n.on("fn-start",function(t){var e=t[0];e instanceof Event&&(this.bstStart=Date.now())}),n.on("fn-end",function(t,e){var n=t[0];n instanceof Event&&r("bst",[n,e,this.bstStart,Date.now()])}),o.on("fn-start",function(t,e,n){this.bstStart=Date.now(),this.bstType=n}),o.on("fn-end",function(t,e){r("bstTimer",[e,this.bstStart,Date.now(),this.bstType])}),i.on("fn-start",function(){this.bstStart=Date.now()}),i.on("fn-end",function(t,e){r("bstTimer",[e,this.bstStart,Date.now(),"requestAnimationFrame"])}),n.on("pushState-start",function(){this.time=Date.now(),this.startPath=location.pathname+location.hash}),n.on("pushState-end",function(){r("bstHist",[location.pathname+location.hash,this.startPath,this.time])}),"addEventListener"in window.performance&&(window.performance.addEventListener("webkitresourcetimingbufferfull",function(){r("bstResource",[window.performance.getEntriesByType("resource")]),window.performance.webkitClearResourceTimings()},!1),window.performance.addEventListener("resourcetimingbufferfull",function(){r("bstResource",[window.performance.getEntriesByType("resource")]),window.performance.clearResourceTimings()},!1)),document.addEventListener("scroll",e,!1),document.addEventListener("keypress",e,!1),document.addEventListener("click",e,!1)}},{1:10,2:9,3:8,ee:"QJf3ax",handle:"D5DuLP",loader:"G9z0Bl"}],7:[function(t,e){function n(t){i.inPlace(t,["addEventListener","removeEventListener"],"-",r)}function r(t){return t[1]}var o=(t(1),t("ee").create()),i=t(2)(o),a=t("gos");if(e.exports=o,n(window),"getPrototypeOf"in Object){for(var s=document;s&&!s.hasOwnProperty("addEventListener");)s=Object.getPrototypeOf(s);s&&n(s);for(var c=XMLHttpRequest.prototype;c&&!c.hasOwnProperty("addEventListener");)c=Object.getPrototypeOf(c);c&&n(c)}else XMLHttpRequest.prototype.hasOwnProperty("addEventListener")&&n(XMLHttpRequest.prototype);o.on("addEventListener-start",function(t){if(t[1]){var e=t[1];"function"==typeof e?this.wrapped=t[1]=a(e,"nr@wrapped",function(){return i(e,"fn-",null,e.name||"anonymous")}):"function"==typeof e.handleEvent&&i.inPlace(e,["handleEvent"],"fn-")}}),o.on("removeEventListener-start",function(t){var e=this.wrapped;e&&(t[1]=e)})},{1:24,2:25,ee:"QJf3ax",gos:"7eSDFh"}],8:[function(t,e){var n=(t(2),t("ee").create()),r=t(1)(n);e.exports=n,r.inPlace(window.history,["pushState"],"-")},{1:25,2:24,ee:"QJf3ax"}],9:[function(t,e){var n=(t(2),t("ee").create()),r=t(1)(n);e.exports=n,r.inPlace(window,["requestAnimationFrame","mozRequestAnimationFrame","webkitRequestAnimationFrame","msRequestAnimationFrame"],"raf-"),n.on("raf-start",function(t){t[0]=r(t[0],"fn-")})},{1:25,2:24,ee:"QJf3ax"}],10:[function(t,e){function n(t,e,n){t[0]=o(t[0],"fn-",null,n)}var r=(t(2),t("ee").create()),o=t(1)(r);e.exports=r,o.inPlace(window,["setTimeout","setInterval","setImmediate"],"setTimer-"),r.on("setTimer-start",n)},{1:25,2:24,ee:"QJf3ax"}],11:[function(t,e){function n(){f.inPlace(this,p,"fn-")}function r(t,e){f.inPlace(e,["onreadystatechange"],"fn-")}function o(t,e){return e}function i(t,e){for(var n in t)e[n]=t[n];return e}var a=t("ee").create(),s=t(1),c=t(2),f=c(a),u=c(s),d=window.XMLHttpRequest,p=["onload","onerror","onabort","onloadstart","onloadend","onprogress","ontimeout"];e.exports=a,window.XMLHttpRequest=function(t){var e=new d(t);try{a.emit("new-xhr",[],e),u.inPlace(e,["addEventListener","removeEventListener"],"-",o),e.addEventListener("readystatechange",n,!1)}catch(r){try{a.emit("internal-error",[r])}catch(i){}}return e},i(d,XMLHttpRequest),XMLHttpRequest.prototype=d.prototype,f.inPlace(XMLHttpRequest.prototype,["open","send"],"-xhr-",o),a.on("send-xhr-start",r),a.on("open-xhr-start",r)},{1:7,2:25,ee:"QJf3ax"}],12:[function(t){function e(t){var e=this.params,r=this.metrics;if(!this.ended){this.ended=!0;for(var i=0;c>i;i++)t.removeEventListener(s[i],this.listener,!1);if(!e.aborted){if(r.duration=(new Date).getTime()-this.startTime,4===t.readyState){e.status=t.status;var a=t.responseType,f="arraybuffer"===a||"blob"===a||"json"===a?t.response:t.responseText,u=n(f);if(u&&(r.rxSize=u),this.sameOrigin){var d=t.getResponseHeader("X-NewRelic-App-Data");d&&(e.cat=d.split(", ").pop())}}else e.status=0;r.cbTime=this.cbTime,o("xhr",[e,r,this.startTime])}}}function n(t){if("string"==typeof t&&t.length)return t.length;if("object"!=typeof t)return void 0;if("undefined"!=typeof ArrayBuffer&&t instanceof ArrayBuffer&&t.byteLength)return t.byteLength;if("undefined"!=typeof Blob&&t instanceof Blob&&t.size)return t.size;if("undefined"!=typeof FormData&&t instanceof FormData)return void 0;try{return JSON.stringify(t).length}catch(e){return void 0}}function r(t,e){var n=i(e),r=t.params;r.host=n.hostname+":"+n.port,r.pathname=n.pathname,t.sameOrigin=n.sameOrigin}if(window.XMLHttpRequest&&XMLHttpRequest.prototype&&XMLHttpRequest.prototype.addEventListener&&!/CriOS/.test(navigator.userAgent)){t("loader").features.xhr=!0;var o=t("handle"),i=t(2),a=t("ee"),s=["load","error","abort","timeout"],c=s.length,f=t(1);t(4),t(3),a.on("new-xhr",function(){this.totalCbs=0,this.called=0,this.cbTime=0,this.end=e,this.ended=!1,this.xhrGuids={}}),a.on("open-xhr-start",function(t){this.params={method:t[0]},r(this,t[1]),this.metrics={}}),a.on("open-xhr-end",function(t,e){"loader_config"in NREUM&&"xpid"in NREUM.loader_config&&this.sameOrigin&&e.setRequestHeader("X-NewRelic-ID",NREUM.loader_config.xpid)}),a.on("send-xhr-start",function(t,e){var r=this.metrics,o=t[0],i=this;if(r&&o){var f=n(o);f&&(r.txSize=f)}this.startTime=(new Date).getTime(),this.listener=function(t){try{"abort"===t.type&&(i.params.aborted=!0),("load"!==t.type||i.called===i.totalCbs&&(i.onloadCalled||"function"!=typeof e.onload))&&i.end(e)}catch(n){try{a.emit("internal-error",[n])}catch(r){}}};for(var u=0;c>u;u++)e.addEventListener(s[u],this.listener,!1)}),a.on("xhr-cb-time",function(t,e,n){this.cbTime+=t,e?this.onloadCalled=!0:this.called+=1,this.called!==this.totalCbs||!this.onloadCalled&&"function"==typeof n.onload||this.end(n)}),a.on("xhr-load-added",function(t,e){var n=""+f(t)+!!e;this.xhrGuids&&!this.xhrGuids[n]&&(this.xhrGuids[n]=!0,this.totalCbs+=1)}),a.on("xhr-load-removed",function(t,e){var n=""+f(t)+!!e;this.xhrGuids&&this.xhrGuids[n]&&(delete this.xhrGuids[n],this.totalCbs-=1)}),a.on("addEventListener-end",function(t,e){e instanceof XMLHttpRequest&&"load"===t[0]&&a.emit("xhr-load-added",[t[1],t[2]],e)}),a.on("removeEventListener-end",function(t,e){e instanceof XMLHttpRequest&&"load"===t[0]&&a.emit("xhr-load-removed",[t[1],t[2]],e)}),a.on("fn-start",function(t,e,n){e instanceof XMLHttpRequest&&("onload"===n&&(this.onload=!0),("load"===(t[0]&&t[0].type)||this.onload)&&(this.xhrCbStart=(new Date).getTime()))}),a.on("fn-end",function(t,e){this.xhrCbStart&&a.emit("xhr-cb-time",[(new Date).getTime()-this.xhrCbStart,this.onload,e],e)})}},{1:"XL7HBI",2:13,3:11,4:7,ee:"QJf3ax",handle:"D5DuLP",loader:"G9z0Bl"}],13:[function(t,e){e.exports=function(t){var e=document.createElement("a"),n=window.location,r={};e.href=t,r.port=e.port;var o=e.href.split("://");return!r.port&&o[1]&&(r.port=o[1].split("/")[0].split("@").pop().split(":")[1]),r.port&&"0"!==r.port||(r.port="https"===o[0]?"443":"80"),r.hostname=e.hostname||n.hostname,r.pathname=e.pathname,r.protocol=o[0],"/"!==r.pathname.charAt(0)&&(r.pathname="/"+r.pathname),r.sameOrigin=!e.hostname||e.hostname===document.domain&&e.port===n.port&&e.protocol===n.protocol,r}},{}],14:[function(t,e){function n(t){return function(){r(t,[(new Date).getTime()].concat(i(arguments)))}}var r=t("handle"),o=t(1),i=t(2);"undefined"==typeof window.newrelic&&(newrelic=window.NREUM);var a=["setPageViewName","addPageAction","setCustomAttribute","finished","addToTrace","inlineHit","noticeError"];o(a,function(t,e){window.NREUM[e]=n("api-"+e)}),e.exports=window.NREUM},{1:23,2:24,handle:"D5DuLP"}],"7eSDFh":[function(t,e){function n(t,e,n){if(r.call(t,e))return t[e];var o=n();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(t,e,{value:o,writable:!0,enumerable:!1}),o}catch(i){}return t[e]=o,o}var r=Object.prototype.hasOwnProperty;e.exports=n},{}],gos:[function(t,e){e.exports=t("7eSDFh")},{}],handle:[function(t,e){e.exports=t("D5DuLP")},{}],D5DuLP:[function(t,e){function n(t,e,n){return r.listeners(t).length?r.emit(t,e,n):(o[t]||(o[t]=[]),void o[t].push(e))}var r=t("ee").create(),o={};e.exports=n,n.ee=r,r.q=o},{ee:"QJf3ax"}],id:[function(t,e){e.exports=t("XL7HBI")},{}],XL7HBI:[function(t,e){function n(t){var e=typeof t;return!t||"object"!==e&&"function"!==e?-1:t===window?0:i(t,o,function(){return r++})}var r=1,o="nr@id",i=t("gos");e.exports=n},{gos:"7eSDFh"}],G9z0Bl:[function(t,e){function n(){var t=p.info=NREUM.info,e=f.getElementsByTagName("script")[0];if(t&&t.licenseKey&&t.applicationID&&e){s(d,function(e,n){e in t||(t[e]=n)});var n="https"===u.split(":")[0]||t.sslForHttp;p.proto=n?"https://":"http://",a("mark",["onload",i()]);var r=f.createElement("script");r.src=p.proto+t.agent,e.parentNode.insertBefore(r,e)}}function r(){"complete"===f.readyState&&o()}function o(){a("mark",["domContent",i()])}function i(){return(new Date).getTime()}var a=t("handle"),s=t(1),c=(t(2),window),f=c.document,u=(""+location).split("?")[0],d={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-632.min.js"},p=e.exports={offset:i(),origin:u,features:{}};f.addEventListener?(f.addEventListener("DOMContentLoaded",o,!1),c.addEventListener("load",n,!1)):(f.attachEvent("onreadystatechange",r),c.attachEvent("onload",n)),a("mark",["firstbyte",i()])},{1:23,2:14,handle:"D5DuLP"}],loader:[function(t,e){e.exports=t("G9z0Bl")},{}],23:[function(t,e){function n(t,e){var n=[],o="",i=0;for(o in t)r.call(t,o)&&(n[i]=e(o,t[o]),i+=1);return n}var r=Object.prototype.hasOwnProperty;e.exports=n},{}],24:[function(t,e){function n(t,e,n){e||(e=0),"undefined"==typeof n&&(n=t?t.length:0);for(var r=-1,o=n-e||0,i=Array(0>o?0:o);++r<o;)i[r]=t[e+r];return i}e.exports=n},{}],25:[function(t,e){function n(t){return!(t&&"function"==typeof t&&t.apply&&!t[i])}var r=t("ee"),o=t(1),i="nr@wrapper",a=Object.prototype.hasOwnProperty;e.exports=function(t){function e(t,e,r,a){function nrWrapper(){var n,i,s,f;try{i=this,n=o(arguments),s=r&&r(n,i)||{}}catch(d){u([d,"",[n,i,a],s])}c(e+"start",[n,i,a],s);try{return f=t.apply(i,n)}catch(p){throw c(e+"err",[n,i,p],s),p}finally{c(e+"end",[n,i,f],s)}}return n(t)?t:(e||(e=""),nrWrapper[i]=!0,f(t,nrWrapper),nrWrapper)}function s(t,r,o,i){o||(o="");var a,s,c,f="-"===o.charAt(0);for(c=0;c<r.length;c++)s=r[c],a=t[s],n(a)||(t[s]=e(a,f?s+o:o,i,s))}function c(e,n,r){try{t.emit(e,n,r)}catch(o){u([o,e,n,r])}}function f(t,e){if(Object.defineProperty&&Object.keys)try{var n=Object.keys(t);return n.forEach(function(n){Object.defineProperty(e,n,{get:function(){return t[n]},set:function(e){return t[n]=e,e}})}),e}catch(r){u([r])}for(var o in t)a.call(t,o)&&(e[o]=t[o]);return e}function u(e){try{t.emit("internal-error",e)}catch(n){}}return t||(t=r),e.inPlace=s,e.flag=i,e}},{1:24,ee:"QJf3ax"}]},{},["G9z0Bl",4,12,6,5]);</script><script type="text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","queueTime":0,"licenseKey":"a2cef8c3d3","agent":"js-agent.newrelic.com/nr-632.min.js","transactionName":"Z11RZxdWW0cEVkYLDV4XdUYLVEFdClsdAAtEWkZQDlJBGgRFQhFMQl1DXFcZQ10AQkFYBFlUVlEXWEJHAA==","userAttributes":"SxpaQDpWQEANUFwWC1NZR1YBFQ9AF0BXTkBZS2xSFV4XDgNUXhEHHBpGQABFaloEWFdAWBJ8XEEXXlsWGA==","applicationID":"1841284","errorBeacon":"bam.nr-data.net","applicationTime":280}</script>
  <title>
  Dorrin / IMN_libs 
  / source  / README.md
 &mdash; Bitbucket
</title>
  


<meta id="bb-canon-url" name="bb-canon-url" content="https://bitbucket.org">

<meta name="description" content=""/>
<meta name="bb-view-name" content="bitbucket.apps.repo2.views.filebrowse">
<meta name="ignore-whitespace" content="False">
<meta name="tab-size" content="None">

<meta name="application-name" content="Bitbucket">
<meta name="apple-mobile-web-app-title" content="Bitbucket">
<meta name="theme-color" content="#205081">
<meta name="msapplication-TileColor" content="#205081">
<meta name="msapplication-TileImage" content="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/img/logos/bitbucket/white-256.png">
<link rel="apple-touch-icon" sizes="192x192" type="image/png" href="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540//img/bitbucket_avatar/192/bitbucket.png">
<link rel="icon" sizes="192x192" type="image/png" href="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540//img/bitbucket_avatar/192/bitbucket.png">
<link rel="icon" sizes="16x16 32x32" type="image/x-icon" href="/favicon.ico">
<link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="Bitbucket">

  
    
  
<link rel="stylesheet" href="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/compressed/css/6ad287f23850.css" type="text/css" />


  <link rel="stylesheet" href="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/compressed/css/520d6c7393f2.css" type="text/css" />


<link rel="stylesheet" href="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/compressed/css/b519230a6cdd.css" type="text/css" />


  
  <!--[if lte IE 9]><link rel="stylesheet" href="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/bower_components/fd-slider/css/fd-slider.css" media="all"><![endif]-->
  <!--[if IE 9]><link rel="stylesheet" href="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/bower_components/aui-stable/aui-next/css/aui-ie9.css" media="all"><![endif]-->
  <!--[if IE]><link rel="stylesheet" href="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/css/aui-overrides-ie.css" media="all"><![endif]-->
  
  
    <link href="/Dorrin/imn_libs/rss?token=687bc4d51ec90c59a8de9b198adcdba9" rel="alternate nofollow" type="application/rss+xml" title="RSS feed for IMN_libs" />
  

</head>
<body class="production aui-page-sidebar aui-sidebar-collapsed"
      data-base-url="https://bitbucket.org"
      data-no-avatar-image="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/img/default_avatar/16/user_blue.png"
      data-current-user="{&quot;username&quot;: &quot;Dorrin&quot;, &quot;displayName&quot;: &quot;Dorrin&quot;, &quot;firstName&quot;: &quot;&quot;, &quot;avatarUrl&quot;: &quot;https://bitbucket.org/account/Dorrin/avatar/32/&quot;, &quot;lastName&quot;: &quot;&quot;, &quot;isTeam&quot;: false, &quot;isSshEnabled&quot;: true, &quot;isKbdShortcutsEnabled&quot;: true, &quot;id&quot;: 2592829, &quot;isAuthenticated&quot;: true}"
      data-atlassian-id="{&quot;loginStatusUrl&quot;: &quot;https://id.atlassian.com/profile/rest/profile&quot;}"
      data-settings="{&quot;MENTIONS_MIN_QUERY_LENGTH&quot;: 3}"
      data-flag-super-touch-point="true"
       data-current-repo="{&quot;scm&quot;: &quot;git&quot;, &quot;readOnly&quot;: false, &quot;mainbranch&quot;: {&quot;name&quot;: &quot;master&quot;}, &quot;language&quot;: &quot;c++&quot;, &quot;creator&quot;: {&quot;username&quot;: &quot;Dorrin&quot;}, &quot;owner&quot;: {&quot;username&quot;: &quot;Dorrin&quot;, &quot;isTeam&quot;: false}, &quot;fullslug&quot;: &quot;Dorrin/imn_libs&quot;, &quot;slug&quot;: &quot;imn_libs&quot;, &quot;id&quot;: 12003352, &quot;pygmentsLanguage&quot;: &quot;c++&quot;}"
       data-current-cset="8df20040bc1a49c1c33c16f7269537f1e214f496"
      
      
      
      
      >

  
    <script type="text/javascript" src="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/compressed/js/9f0feb819aab.js"></script>
  


<div id="page">
  <div id="wrapper">
    
  


    <header id="header" role="banner" data-modules="header/tracking">
      
  
  


      <nav class="aui-header aui-dropdown2-trigger-group" role="navigation">
        <div class="aui-header-inner">
          <div class="aui-header-primary">
            
  
  <div class="aui-header-before">
    <a class="aui-dropdown2-trigger app-switcher-trigger" href="#app-switcher" aria-owns="app-switcher" aria-haspopup="true" tabindex="0">
      <span class="aui-icon aui-icon-small aui-iconfont-appswitcher">Linked applications</span>
    </a>
    
      <nav id="app-switcher" class="aui-dropdown2 aui-style-default">
        <div class="aui-dropdown2-section blank-slate">
          <h2>Connect Bitbucket with other great Atlassian products:</h2>
          <dl>
            <dt class="jira">JIRA</dt>
            <dd>Project and issue tracking</dd>
            <dt class="confluence">Confluence</dt>
            <dd>Collaboration and content sharing</dd>
            <dt class="bamboo">Bamboo</dt>
            <dd>Continuous integration</dd>
          </dl>
          <ul>
            <li>
              <a href="https://www.atlassian.com/ondemand/signup/?product=jira.ondemand,com.atlassian.bitbucket&utm_source=bitbucket&utm_medium=button&utm_campaign=app_switcher&utm_content=trial_button"
                 class="aui-button aui-button-primary" target="_blank" id="ondemand-trial">Free trial</a>
            </li>
            <li>
              <a href="https://www.atlassian.com/software?utm_source=bitbucket&utm_medium=button&utm_campaign=app_switcher&utm_content=learn_more_button#cloud-products"
                 class="aui-button" target="_blank" id="ondemand-learn-more">Learn more</a>
            </li>
          </ul>
        </div>
      </nav>
    
  </div>


            
              <h1 class="aui-header-logo aui-header-logo-bitbucket " id="logo">
                <a href="/">
                  <span class="aui-header-logo-device">Bitbucket</span>
                </a>
              </h1>
            
            
  
<script id="repo-dropdown-template" type="text/html">
    

[[#hasViewed]]
  <div class="aui-dropdown2-section">
    <strong class="viewed">Recently viewed</strong>
    <ul class="aui-list-truncate">
      [[#viewed]]
        <li class="[[#is_private]]private[[/is_private]][[^is_private]]public[[/is_private]] repository">
          <a href="[[url]]" title="[[owner]]/[[name]]" class="aui-icon-container recently-viewed repo-link">
            <img class="repo-avatar size16" src="[[{avatar}]]" alt="[[owner]]/[[name]] avatar"/>
            [[owner]] / [[name]]
          </a>
        </li>
      [[/viewed]]
    </ul>
  </div>
[[/hasViewed]]
[[#hasUpdated]]
<div class="aui-dropdown2-section">
  <strong class="updated">Recently updated</strong>
  <ul class="aui-list-truncate">
    [[#updated]]
    <li class="[[#is_private]]private[[/is_private]][[^is_private]]public[[/is_private]] repository">
      <a href="[[url]]" title="[[owner]]/[[name]]" class="aui-icon-container recently-updated repo-link">
        <img class="repo-avatar size16" src="[[{avatar}]]" alt="[[owner]]/[[name]] avatar"/>
        [[owner]] / [[name]]
      </a>
    </li>
    [[/updated]]
  </ul>
</div>
[[/hasUpdated]]

  </script>
<script id="snippet-dropdown-template" type="text/html">
    <div class="aui-dropdown2-section">
  <strong>[[sectionTitle]]</strong>
  <ul class="aui-list-truncate">
    [[#snippets]]
      <li>
        <a href="[[links.html.href]]">[[owner.display_name]] / [[name]]</a>
      </li>
    [[/snippets]]
  </ul>
</div>

  </script>
<ul class="aui-nav">
  
    <li>
      <a class="aui-dropdown2-trigger"
         aria-owns="dashboard-dropdown" aria-haspopup="true" href="/dashboard/overview" id="dashboard-dropdown-trigger">
        Dashboard
        <span class="aui-icon-dropdown"></span>
      </a>
      <nav id="dashboard-dropdown" class="aui-dropdown2 aui-style-default">
        <div class="aui-dropdown2-section">
          <ul>
            
              <li>
                <a href="/dashboard/overview">Overview</a>
              </li>
            
              <li>
                <a href="/dashboard/pullrequests">Pull requests</a>
              </li>
            
              <li>
                <a href="/dashboard/issues">Issues</a>
              </li>
            
              <li>
                <a href="/snippets">Snippets</a>
              </li>
            
          </ul>
        </div>
      </nav>
    </li>
    
      <script id="team-dropdown-template" type="text/html">
    

<div class="aui-dropdown2-section primary">
  <ul class="aui-list-truncate">
    [[#teams]]
      <li>
        <a href="/[[username]]" class="aui-icon-container team-link">
          <img class="avatar avatar16" src="[[avatar]]" alt="" width="16" height="16" />[[display_name]]
        </a>
      </li>
    [[/teams]]
  </ul>
</div>

<div class="aui-dropdown2-section">
  <ul>
    <li>
      <a href="/account/create-team/?team_source=header"
          data-modules="registration/create-team-link"
          id="create-team-link">Create team</a>
    </li>
  </ul>
</div>

  </script>
      <li>
        <a class="aui-dropdown2-trigger" href="#teams-dropdown" id="teams-dropdown-trigger"
          data-modules="header/teams-dropdown"
          aria-owns="teams-dropdown" aria-haspopup="true">
          Teams
          <span class="aui-icon-dropdown"></span>
        </a>
        <div id="teams-dropdown" class="aui-dropdown2 aui-style-default">
          <div class="aui-dropdown2-section blank-slate">
            <p>Organize your team's work and supercharge repository administration.</p>
            <ul>
              <li>
                <a class="aui-button aui-button-primary" id="create-team-blank-slate"
                   href="/account/create-team/?team_source=menu_blank"
                   >Create team</a>
              </li>
            </ul>
          </div>
        </div>
      </li>
    
    <li>
      <a class="aui-dropdown2-trigger" id="repositories-dropdown-trigger"
         aria-owns="repo-dropdown" aria-haspopup="true" href="/repo/mine">
        Repositories
        <span class="aui-icon-dropdown"></span>
      </a>
      <nav id="repo-dropdown" class="aui-dropdown2 aui-style-default">
        <div id="repo-dropdown-recent" data-modules="header/recent-repos"></div>
        <div class="aui-dropdown2-section">
          <ul>
            <li>
              <a href="/repo/create" class="new-repository" id="create-repo-link">
                Create repository
              </a>
            </li>
            <li>
              <a href="/repo/import" class="import-repository" id="import-repo-link">
                Import repository
              </a>
            </li>
          </ul>
        </div>
      </nav>
    </li>
    <li>
      <a class="aui-dropdown2-trigger" id="snippets-dropdown-trigger"
        aria-owns="nav-recent-snippets" aria-haspopup="true" href="/snippets">
        Snippets
        <span class="aui-icon-dropdown"></span>
      </a>
      <nav id="nav-recent-snippets" class="aui-dropdown2 aui-style-default">
        <div id="snippet-dropdown-recent" class="aui-dropdown2-section"
            data-modules="snippets/recent-list"></div>
        <div class="aui-dropdown2-section">
          <ul>
            <li>
              <a href="/snippets/new">
                Create snippet
              </a>
            </li>
          </ul>
        </div>
      </nav>
    </li>
    <li>
      <div class="aui-buttons ">
        <button class="aui-button aui-button-primary aui-dropdown2-trigger" aria-owns="create-cta-dropdown" aria-haspopup="true" aria-controls="create-cta-dropdown">
          Create<span class="aui-icon-dropdown"></span>
        </button>
      </div>
      <nav id="create-cta-dropdown" class="aui-dropdown2 aui-style-default aui-dropdown2-in-header" aria-hidden="true">
        <div class="aui-dropdown2-section">
          <ul>
            <li>
              <a href="/repo/create" id="repo-create-cta">
                Create repository
              </a>
            </li>
            <li>
              <a href="/snippets/new" id="snippet-create-cta">
                Create snippet
              </a>
            </li>
          </ul>
        </div>
      </nav>
    </li>
  
</ul>

          </div>
          <div class="aui-header-secondary">
            
  

<ul role="menu" class="aui-nav">
  
  <li>
    <form action="/repo/all" method="get" class="aui-quicksearch">
      <label for="search-query" class="assistive">owner/repository</label>
      <input id="search-query" class="bb-repo-typeahead" type="text"
             placeholder="Find a repository&hellip;" name="name" autocomplete="off"
             data-bb-typeahead-focus="false">
    </form>
  </li>
  <li id="ace-stp-menu">
    <a id="ace-stp-menu-link" class="aui-nav-link" href="#"
    aria-controls="super-touch-point-dialog"
    data-modules="aui/inline-dialog2"
    data-aui-trigger>
  <span id="ace-stp-menu-icon"
      class="aui-icon aui-icon-small ace-stp-icon-help"></span>
  <span class="aui-icon-dropdown"></span>
</a>
  </li>
  
    
  
  
    <li>
      <a class="aui-dropdown2-trigger"
         aria-owns="user-dropdown" aria-haspopup="true" data-container="#header .aui-header-inner"
         href="/Dorrin" title="Dorrin" id="user-dropdown-trigger">
        <div class="aui-avatar aui-avatar-small">
            <div class="aui-avatar-inner">
                <img src="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/img/default_avatar/32/user_blue.png" class="deferred-image" data-src-url="https://bitbucket.org/account/Dorrin/avatar/32/" data-src-url-2x="https://bitbucket.org/account/Dorrin/avatar/64/" alt="Logged in as Dorrin" height="24" width="24">
            </div>
        </div>
      </a>
      <nav id="user-dropdown" class="aui-dropdown2 aui-style-default" aria-hidden="true">
        <div class="aui-dropdown2-section">
          <ul>
            <li>
              <a href="/Dorrin" id="profile-link">View profile</a>
            </li>
            <li>
              <a href="/account/user/Dorrin/" id="account-link">Manage account</a>
            </li>
            <li>
                <a href="/account/notifications/" id="inbox-link">Inbox <span id="inbox-unread-count"></span></a>
            </li>
            <li>
              <a href="#general-invite" class="general-invite-link" id="general-invite-dropdown" data-modules="header/general-invite">Invite a friend</a>
              <script id="general-invite-template" type="text/html">
    
<div id="general-invite">
  <form class="aui invitation-form" id="general-invite-form" method="post" novalidate>
    <div class="error aui-message hidden">
      <span class="aui-icon icon-error"></span>
      <div class="message"></div>
    </div>
    <div class="field-group">
      <label for="id_general_email_address">Email address</label>
      <input type="email" id="id_general_email_address" name="email-address" class="text long-field">
    </div>
  </form>
</div>

  </script>
            </li>
          </ul>
        </div>
        <div class="aui-dropdown2-section">
          <ul>
            <li>
              
                <a href="/account/signout/" id="log-out-link">Log out</a>
              
            </li>
          </ul>
        </div>
      </nav>
    </li>
  
</ul>

          </div>
        </div>
      </nav>
    </header>

    
  
  <header id="account-warning" role="banner" data-modules="header/account-warning"
          class="aui-message-banner warning
          ">
    <div class="aui-message-banner-inner">
      <span class="aui-icon aui-icon-warning"></span>
      <span class="message">
      
      </span>
    </div>
  </header>


    
  
<header id="aui-message-bar">
  
</header>


    <div id="content" role="main">
      
  

<div class="aui-sidebar repo-sidebar" data-modules="components/repo-sidebar,experiment/grow1279-guide"
   aria-expanded="false">
  <div class="aui-sidebar-wrapper">
    <div class="aui-sidebar-body">
      <header class="aui-page-header">
        <div class="aui-page-header-inner">
          <div class="aui-page-header-image">
            <a href="/Dorrin/imn_libs" id="repo-avatar-link" class="repo-link">
              <span class="aui-avatar aui-avatar-large aui-avatar-project">
                <span class="aui-avatar-inner">
                  <img  src="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/img/language-avatars/default_64.png" class="deferred-image" data-src-url="https://bitbucket.org/Dorrin/imn_libs/avatar/64/?ts=2015-06-14T00:52:15.532349" data-src-url-2x="https://bitbucket.org/Dorrin/imn_libs/avatar/128/?ts=2015-06-14T00:52:15.532349" alt="">
                </span>
              </span>
            </a>
          </div>
          <div class="aui-page-header-main">
            <ol class="aui-nav aui-nav-breadcrumbs">
              <li>
                <a href="/Dorrin" id="repo-owner-link">Dorrin</a>
              </li>
            </ol>
            <h1>
              
              <a href="/Dorrin/imn_libs" title="IMN_libs" class="entity-name">IMN_libs</a>
            </h1>
          </div>
        </div>
      </header>
      <nav class="aui-navgroup aui-navgroup-vertical">
        <div class="aui-navgroup-inner">
          
            
              <div class="aui-sidebar-group aui-sidebar-group-actions repository-actions forks-enabled can-create">
                <div class="aui-nav-heading">
                  <strong>Actions</strong>
                </div>
                <ul id="repo-actions" class="aui-nav">
                  
                  
                    <li>
                      <a id="repo-clone-button" class="aui-nav-item "
                        href="#clone"
                        data-modules="components/clone/clone-dialog"
                        target="_self">
                        <span class="aui-icon aui-icon-large icon-clone"></span>
                        <span class="aui-nav-item-label">Clone</span>
                      </a>
                    </li>
                  
                    <li>
                      <a id="repo-create-branch-link" class="aui-nav-item create-branch-button"
                        href="/Dorrin/imn_libs/branch"
                        data-modules="repo/create-branch"
                        target="_self">
                        <span class="aui-icon aui-icon-large icon-create-branch"></span>
                        <span class="aui-nav-item-label">Create branch</span>
                      </a>
                    </li>
                  
                    <li>
                      <a id="repo-create-pull-request-link" class="aui-nav-item "
                        href="/Dorrin/imn_libs/pull-request/new"
                        
                        target="_self">
                        <span class="aui-icon aui-icon-large icon-create-pull-request"></span>
                        <span class="aui-nav-item-label">Create pull request</span>
                      </a>
                    </li>
                  
                    <li>
                      <a id="repo-compare-link" class="aui-nav-item "
                        href="/Dorrin/imn_libs/branches/compare"
                        
                        target="_self">
                        <span class="aui-icon aui-icon-large aui-icon-small aui-iconfont-devtools-compare"></span>
                        <span class="aui-nav-item-label">Compare</span>
                      </a>
                    </li>
                  
                    <li>
                      <a id="repo-fork-link" class="aui-nav-item "
                        href="/Dorrin/imn_libs/fork"
                        
                        target="_self">
                        <span class="aui-icon aui-icon-large icon-fork"></span>
                        <span class="aui-nav-item-label">Fork</span>
                      </a>
                    </li>
                  
                </ul>
              </div>
          
          <div class="aui-sidebar-group aui-sidebar-group-tier-one repository-sections">
            <div class="aui-nav-heading">
              <strong>Navigation</strong>
            </div>
            <ul class="aui-nav">
              
              
                <li>
                  <a id="repo-overview-link" class="aui-nav-item "
                    href="/Dorrin/imn_libs/overview"
                    
                    target="_self"
                    >
                    
                    <span class="aui-icon aui-icon-large icon-overview"></span>
                    <span class="aui-nav-item-label">Overview</span>
                  </a>
                </li>
              
                <li class="aui-nav-selected">
                  <a id="repo-source-link" class="aui-nav-item "
                    href="/Dorrin/imn_libs/src"
                    
                    target="_self"
                    >
                    
                    <span class="aui-icon aui-icon-large icon-source"></span>
                    <span class="aui-nav-item-label">Source</span>
                  </a>
                </li>
              
                <li>
                  <a id="repo-commits-link" class="aui-nav-item "
                    href="/Dorrin/imn_libs/commits"
                    
                    target="_self"
                    >
                    
                    <span class="aui-icon aui-icon-large icon-commits"></span>
                    <span class="aui-nav-item-label">Commits</span>
                  </a>
                </li>
              
                <li>
                  <a id="repo-branches-link" class="aui-nav-item "
                    href="/Dorrin/imn_libs/branches"
                    
                    target="_self"
                    >
                    
                    <span class="aui-icon aui-icon-large icon-branches"></span>
                    <span class="aui-nav-item-label">Branches</span>
                  </a>
                </li>
              
                <li>
                  <a id="repo-pullrequests-link" class="aui-nav-item "
                    href="/Dorrin/imn_libs/pull-requests"
                    
                    target="_self"
                    >
                    
                    <span class="aui-icon aui-icon-large icon-pull-requests"></span>
                    <span class="aui-nav-item-label">Pull requests</span>
                  </a>
                </li>
              
                <li>
                  <a id="repo-issues-link" class="aui-nav-item "
                    href="/Dorrin/imn_libs/issues?status=new&amp;status=open"
                    
                    target="_self"
                    title="( type &#39;r&#39; then &#39;i&#39; )">
                    
                    <span class="aui-icon aui-icon-large icon-issues"></span>
                    <span class="aui-nav-item-label">Issues</span>
                  </a>
                </li>
              
                <li>
                  <a id="repo-downloads-link" class="aui-nav-item "
                    href="/Dorrin/imn_libs/downloads"
                    
                    target="_self"
                    >
                    
                    <span class="aui-icon aui-icon-large icon-downloads"></span>
                    <span class="aui-nav-item-label">Downloads</span>
                  </a>
                </li>
              
            </ul>
          </div>
          <div class="aui-sidebar-group aui-sidebar-group-tier-one repository-settings">
            <div class="aui-nav-heading">
              <strong class="assistive">Settings</strong>
            </div>
            <ul class="aui-nav">
              
              
                <li>
                  <a id="repo-settings-link" class="aui-nav-item "
                    href="/Dorrin/imn_libs/admin"
                    
                    target="_self"
                    >
                    
                    <span class="aui-icon aui-icon-large icon-settings"></span>
                    <span class="aui-nav-item-label">Settings</span>
                  </a>
                </li>
              
            </ul>
          </div>
          
            
              <div class="hidden kb-shortcut-actions">
                <a id="repo-create-issue" href="/Dorrin/imn_libs/issues/new"></a>
              </div>
            
          
        </div>
      </nav>
    </div>
    <div class="aui-sidebar-footer">
      <a class="aui-sidebar-toggle aui-sidebar-footer-tipsy aui-button aui-button-subtle"><span class="aui-icon"></span></a>
    </div>
  </div>
  
    <script id="share-repo-template" type="text/html">
    

<div class="clearfix">
   <span class="repo-avatar-container size32" title="Dorrin/IMN_libs">
  <img alt="Dorrin/IMN_libs" src="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/img/language-avatars/default_32.png" class="deferred-image" data-src-url="https://bitbucket.org/Dorrin/imn_libs/avatar/32/?ts=2015-06-14T00:52:15.532349" data-src-url-2x="https://bitbucket.org/Dorrin/imn_libs/avatar/64/?ts=2015-06-14T00:52:15.532349">
</span>

  <span class="repo-name-container">
    Dorrin / IMN_libs
  </span>
</div>
<p class="helptext">
  
    Existing users are granted access to this repository immediately.
    New users will be sent an invitation.
  
</p>
<div class="manage-repo-link"
  data-manage-link="/Dorrin/imn_libs/admin/access"></div>
<div class="share-form"></div>

  </script>
    <script id="share-dialog-template" type="text/html">
    <div class="aui-tabs horizontal-tabs">
  <ul class="tabs-menu">
    [[#panels]]
      <li class="menu-item">
        <a href="#[[tabId]]"><strong>[[display]]</strong></a>
      </li>
    [[/panels]]
  </ul>
  [[#panels]]
    <div class="tabs-pane" id="[[tabId]]"></div>
  [[/panels]]
</div>

  </script>
  
  <div id="repo-clone-dialog" class="clone-dialog hidden">
  
  
  <div class="clone-url" data-modules="components/clone/url-dropdown">
  <div class="aui-buttons">
    <a href="https://Dorrin@bitbucket.org/Dorrin/imn_libs.git"
      class="aui-button aui-dropdown2-trigger" aria-haspopup="true"
      aria-owns="clone-url-dropdown-header">
      <span class="dropdown-text">HTTPS</span>
    </a>
    <div id="clone-url-dropdown-header"
      class="clone-url-dropdown aui-dropdown2 aui-style-default">
      <ul class="aui-list-truncate">
        <li>
          <a href="https://Dorrin@bitbucket.org/Dorrin/imn_libs.git"
            
              data-command="git clone https://Dorrin@bitbucket.org/Dorrin/imn_libs.git"
            
            class="item-link https">HTTPS
          </a>
        </li>
        <li>
          <a href="ssh://git@bitbucket.org/Dorrin/imn_libs.git"
            
              data-command="git clone git@bitbucket.org:Dorrin/imn_libs.git"
            
            class="item-link ssh">SSH
          </a>
        </li>
      </ul>
    </div>
    <input type="text" readonly="readonly" class="clone-url-input"
      value="git clone https://Dorrin@bitbucket.org/Dorrin/imn_libs.git">
  </div>
  
  <p>Need help cloning? Visit
    <a href="https://confluence.atlassian.com/x/cgozDQ" target="_blank">Bitbucket 101</a>.</p>
  
</div>
  
  <div class="sourcetree-callout clone-in-sourcetree"
  data-modules="components/clone/clone-in-sourcetree"
  data-https-url="https://Dorrin@bitbucket.org/Dorrin/imn_libs.git"
  data-ssh-url="ssh://git@bitbucket.org/Dorrin/imn_libs.git">

  <div>
    <button class="aui-button aui-button-primary">
      
        Clone in SourceTree
      
    </button>
  </div>

  <p class="windows-text">
    
      <a href="http://www.sourcetreeapp.com/?utm_source=internal&amp;utm_medium=link&amp;utm_campaign=clone_repo_win" target="_blank">Atlassian SourceTree</a>
      is a free Git and Mercurial client for Windows.
    
  </p>
  <p class="mac-text">
    
      <a href="http://www.sourcetreeapp.com/?utm_source=internal&amp;utm_medium=link&amp;utm_campaign=clone_repo_mac" target="_blank">Atlassian SourceTree</a>
      is a free Git and Mercurial client for Mac.
    
  </p>
</div>
</div>
</div>

      
  <div class="aui-page-panel ">
    



    <div class="aui-page-panel-inner">
      <div id="repo-content" class="aui-page-panel-content" data-modules="repo/index">
        <div class="aui-group repo-page-header">
          <div class="aui-item section-title">
            <h1>Source</h1>
          </div>
          <div class="aui-item page-actions">
            
          </div>
        </div>
        
  <div id="source-container" class="maskable" data-modules="repo/source/index">
    



<header id="source-path">
  <div class="labels labels-csv">
    
      <div class="aui-buttons">
        <button data-branches-tags-url="/api/1.0/repositories/Dorrin/imn_libs/branches-tags"
                data-modules="components/branch-dialog"
                class="aui-button branch-dialog-trigger" title="master">
          
            
              <span class="aui-icon aui-icon-small aui-iconfont-devtools-branch">Branch</span>
            
            <span class="name">master</span>
          
          <span class="aui-icon-dropdown"></span>
        </button>
        <button class="aui-button" id="checkout-branch-button"
                title="Check out this branch">
          <span class="aui-icon aui-icon-small aui-iconfont-devtools-clone">Check out branch</span>
          <span class="aui-icon-dropdown"></span>
        </button>
      </div>
      <script id="branch-checkout-template" type="text/html">
  

<div id="checkout-branch-contents">
  <div class="command-line">
    <p>
      Check out this branch on your local machine to begin working on it.
    </p>
    <input type="text" class="checkout-command" readonly="readonly"
        
           value="git fetch && git checkout [[branchName]]"
        
        >
  </div>
  
    <div class="sourcetree-callout clone-in-sourcetree"
  data-modules="components/clone/clone-in-sourcetree"
  data-https-url="https://Dorrin@bitbucket.org/Dorrin/imn_libs.git"
  data-ssh-url="ssh://git@bitbucket.org/Dorrin/imn_libs.git">

  <div>
    <button class="aui-button aui-button-primary">
      
        Check out in SourceTree
      
    </button>
  </div>

  <p class="windows-text">
    
      <a href="http://www.sourcetreeapp.com/?utm_source=internal&amp;utm_medium=link&amp;utm_campaign=clone_repo_win" target="_blank">Atlassian SourceTree</a>
      is a free Git and Mercurial client for Windows.
    
  </p>
  <p class="mac-text">
    
      <a href="http://www.sourcetreeapp.com/?utm_source=internal&amp;utm_medium=link&amp;utm_campaign=clone_repo_mac" target="_blank">Atlassian SourceTree</a>
      is a free Git and Mercurial client for Mac.
    
  </p>
</div>
  
</div>

</script>
    
  </div>
  <div class="secondary-actions">
    <div class="aui-buttons">
      
        <a href="/Dorrin/imn_libs/src/8df20040bc1a/README.md?at=master"
           class="aui-button pjax-trigger" aria-pressed="true">
          Source
        </a>
        <a href="/Dorrin/imn_libs/diff/README.md?diff2=8df20040bc1a&at=master"
           class="aui-button pjax-trigger"
           title="Diff to previous change">
          Diff
        </a>
        <a href="/Dorrin/imn_libs/history-node/8df20040bc1a/README.md?at=master"
           class="aui-button pjax-trigger">
          History
        </a>
      
    </div>
  </div>
  <h1>
    
      
        <a href="/Dorrin/imn_libs/src/8df20040bc1a?at=master"
          class="pjax-trigger root" title="Dorrin/imn_libs at 8df20040bc1a">IMN_libs</a> /
      
      
        
          
            
              <span class="file-name">README.md</span>
            
          
        
      
    
  </h1>
  
    
    
  
  <div class="clearfix"></div>
</header>


    
      
    

    <div id="editor-container" class="maskable"
         data-modules="repo/source/editor"
         data-owner="Dorrin"
         data-slug="imn_libs"
         data-is-writer="true"
         data-has-push-access="true"
         data-hash="8df20040bc1a49c1c33c16f7269537f1e214f496"
         data-branch="master"
         data-path="README.md"
         data-source-url="/api/1.0/repositories/Dorrin/imn_libs/src/8df20040bc1a49c1c33c16f7269537f1e214f496/README.md">
      <div id="source-view" class="file-source-container" data-modules="repo/source/view-file">
        <div class="toolbar">
          <div class="primary">
            <div class="aui-buttons">
              
                <button id="file-history-trigger" class="aui-button aui-button-light changeset-info"
                        data-changeset="8df20040bc1a49c1c33c16f7269537f1e214f496"
                        data-path="README.md"
                        data-current="8df20040bc1a49c1c33c16f7269537f1e214f496">
                  
                     

  <div class="aui-avatar aui-avatar-xsmall">
    <div class="aui-avatar-inner">
      <img src="https://bitbucket.org/account/Dorrin/avatar/16/">
    </div>
  </div>
  <span class="changeset-hash">8df2004</span>
  <time datetime="2015-06-14T00:52:10+00:00" class="timestamp"></time>
  <span class="aui-icon-dropdown"></span>

                  
                </button>
              
            </div>
          <a href="/Dorrin/imn_libs/full-commit/8df20040bc1a/README.md" id="full-commit-link"
              title="View full commit 8df2004">Full commit</a>
          </div>
            <div class="secondary">
              <div class="aui-buttons">
                
                  <a href="/Dorrin/imn_libs/annotate/8df20040bc1a49c1c33c16f7269537f1e214f496/README.md?at=master"
                  class="aui-button aui-button-light pjax-trigger">Blame</a>
                
                
                  
                  <a id="embed-link" href="https://bitbucket.org/Dorrin/imn_libs/src/8df20040bc1a49c1c33c16f7269537f1e214f496/README.md?embed=t"
                    class="aui-button aui-button-light" data-modules="repo/source/embed">Embed</a>
                
                <a href="/Dorrin/imn_libs/raw/8df20040bc1a49c1c33c16f7269537f1e214f496/README.md"
                  class="aui-button aui-button-light">Raw</a>
              </div>
              
                <div class="aui-buttons">
                  <button class="edit-button aui-button aui-button-light aui-button-split-main">
                    Edit
                    
                  </button>
                  <button class="aui-button aui-button-light aui-dropdown2-trigger aui-button-split-more" aria-owns="split-container-dropdown" aria-haspopup="true" data-container="#editor-container">More file actions</button>
                </div>
                <div id="split-container-dropdown" class="aui-dropdown2 aui-style-default" data-container="split-button-demo">
                  <ul class="aui-list-truncate">
                    <li><a href="#" data-modules="repo/source/rename-file" class="rename-link">Rename</a></li>
                    <li><a href="#" data-modules="repo/source/delete-file" class="delete-link">Delete</a></li>
                  </ul>
                </div>
              
            </div>
          <div class="clearfix"></div>
        </div>
        


  <div class="readme file file-markup wiki-content"
      >
    <h1 id="markdown-header-imn-libs">IMN Libs</h1>
<p>C++ libraries with numerical methods, based on lecture "Inżynierskie Metody Numeryczne" (Engineering Numerical Methods).<br />
AGH University of Science and Technology, Faculty of Physics and Applied Computer Science, 2014/2015.<br />
Lecture taught by prof. Bartłomiej Szafran.</p>
<p>More info in pdf files in each directory.<br />
Materials are not mine, I have only implemented methods.<br />
All pdfs downloaded from <a href="http://galaxy.agh.edu.pl/~dzebrow/">here</a>.</p>
  </div>


      </div>
    </div>
    <div data-modules="js/source/set-changeset" data-hash="8df20040bc1a49c1c33c16f7269537f1e214f496"></div>




  
  
    <script id="branch-dialog-template" type="text/html">
  

<div class="tabbed-filter-widget branch-dialog">
  <div class="tabbed-filter">
    <input placeholder="Filter branches" class="filter-box" autosave="branch-dropdown-12003352" type="text">
    [[^ignoreTags]]
      <div class="aui-tabs horizontal-tabs aui-tabs-disabled filter-tabs">
        <ul class="tabs-menu">
          <li class="menu-item active-tab"><a href="#branches">Branches</a></li>
          <li class="menu-item"><a href="#tags">Tags</a></li>
        </ul>
      </div>
    [[/ignoreTags]]
  </div>
  
    <div class="tab-pane active-pane" id="branches" data-filter-placeholder="Filter branches">
      <ol class="filter-list">
        <li class="empty-msg">No matching branches</li>
        [[#branches]]
          
            [[#hasMultipleHeads]]
              [[#heads]]
                <li class="comprev filter-item">
                  <a class="pjax-trigger filter-item-link" href="/Dorrin/imn_libs/src/[[changeset]]/README.md?at=[[safeName]]"
                     title="[[name]]">
                    [[name]] ([[shortChangeset]])
                  </a>
                </li>
              [[/heads]]
            [[/hasMultipleHeads]]
            [[^hasMultipleHeads]]
              <li class="comprev filter-item">
                <a class="pjax-trigger filter-item-link" href="/Dorrin/imn_libs/src/[[changeset]]/README.md?at=[[safeName]]" title="[[name]]">
                  [[name]]
                </a>
              </li>
            [[/hasMultipleHeads]]
          
        [[/branches]]
      </ol>
    </div>
    <div class="tab-pane" id="tags" data-filter-placeholder="Filter tags">
      <ol class="filter-list">
        <li class="empty-msg">No matching tags</li>
        [[#tags]]
          <li class="comprev filter-item">
            <a class="pjax-trigger filter-item-link" href="/Dorrin/imn_libs/src/[[changeset]]/README.md?at=[[safeName]]" title="[[name]]">
              [[name]]
            </a>
          </li>
        [[/tags]]
      </ol>
    </div>
  
</div>

</script>
  



  </div>

        
        
        
          <script id="image-upload-template" type="text/html">
  

<form id="upload-image" method="POST"
    
      action="/xhr/Dorrin/imn_libs/image-upload/"
    >
  <input type='hidden' name='csrfmiddlewaretoken' value='ajgNqFHUOIpzWs5Yt5p00OO9MWVGkVqh' />

  <div class="drop-target">
    <p class="centered">Drag image here</p>
  </div>

  
  <div>
    <button class="aui-button click-target">Select an image</button>
    <input name="file" type="file" class="hidden file-target"
           accept="image/jpeg, image/gif, image/png" />
    <input type="submit" class="hidden">
  </div>
</form>


</script>
        
      </div>
    </div>
  </div>

    </div>
  </div>

  <footer id="footer" role="contentinfo" data-modules="components/footer">
    <section class="footer-body">
      
  <ul>
  <li>
    <a class="support-ga" target="_blank"
       data-support-gaq-page="Blog"
       href="http://blog.bitbucket.org">Blog</a>
  </li>
  <li>
    <a class="support-ga" target="_blank"
       data-support-gaq-page="Home"
       href="/support">Support</a>
  </li>
  <li>
    <a class="support-ga"
       data-support-gaq-page="PlansPricing"
       href="/plans">Plans &amp; pricing</a>
  </li>
  <li>
    <a class="support-ga" target="_blank"
       data-support-gaq-page="DocumentationHome"
       href="//confluence.atlassian.com/display/BITBUCKET">Documentation</a>
  </li>
  <li>
    <a class="support-ga" target="_blank"
       data-support-gaq-page="DocumentationAPI"
       href="//confluence.atlassian.com/x/IYBGDQ">API</a>
  </li>
  <li>
    <a class="support-ga" target="_blank"
       data-support-gaq-page="SiteStatus"
       href="http://status.bitbucket.org/">Site status</a>
  </li>
  <li>
    <a class="support-ga" id="meta-info"
       data-support-gaq-page="MetaInfo"
       href="#">Version info</a>
  </li>
  <li>
    <a class="support-ga" target="_blank"
       data-support-gaq-page="EndUserAgreement"
       href="//www.atlassian.com/end-user-agreement?utm_source=bitbucket&amp;utm_medium=link&amp;utm_campaign=footer">Terms of service</a>
  </li>
  <li>
    <a class="support-ga" target="_blank"
       data-support-gaq-page="PrivacyPolicy"
       href="//www.atlassian.com/company/privacy?utm_source=bitbucket&amp;utm_medium=link&amp;utm_campaign=footer">Privacy policy</a>
  </li>
</ul>
<div id="meta-info-content" style="display: none;">
  <ul>
    
      <li><a href="/account/user/Dorrin/" class="view-language-link">English</a></li>
    
    <li>
      <a class="support-ga" target="_blank"
         data-support-gaq-page="GitDocumentation"
         href="http://git-scm.com/">Git 2.1.1</a>
    </li>
    <li>
      <a class="support-ga" target="_blank"
         data-support-gaq-page="HgDocumentation"
         href="http://mercurial.selenic.com/">Mercurial 2.9</a>
    </li>
    <li>
      <a class="support-ga" target="_blank"
         data-support-gaq-page="DjangoDocumentation"
         href="https://www.djangoproject.com/">Django 1.7.8</a>
    </li>
    <li>
      <a class="support-ga" target="_blank"
         data-support-gaq-page="PythonDocumentation"
         href="http://www.python.org/">Python 2.7.3</a>
    </li>
    <li>
      <a class="support-ga" target="_blank"
         data-support-gaq-page="DeployedVersion"
         href="#">0a2f2974a540 / 0a2f2974a540 @ app15</a>
    </li>
  </ul>
</div>
<ul class="atlassian-links">
  <li>
    <a id="atlassian-jira-link" target="_blank"
       title="Track everything – bugs, tasks, deadlines, code – and pull reports to stay informed."
       href="http://www.atlassian.com/software/jira?utm_source=bitbucket&amp;utm_medium=link&amp;utm_campaign=bitbucket_footer">JIRA</a>
  </li>
  <li>
    <a id="atlassian-confluence-link" target="_blank"
       title="Content Creation, Collaboration & Knowledge Sharing for Teams."
       href="http://www.atlassian.com/software/confluence/overview/team-collaboration-software?utm_source=bitbucket&amp;utm_medium=link&amp;utm_campaign=bitbucket_footer">Confluence</a>
  </li>
  <li>
    <a id="atlassian-bamboo-link" target="_blank"
       title="Continuous integration and deployment, release management."
       href="http://www.atlassian.com/software/bamboo/overview?utm_source=bitbucket&amp;utm_medium=link&amp;utm_campaign=bitbucket_footer">Bamboo</a>
  </li>
  <li>
    <a id="atlassian-stash-link" target="_blank"
       title="Git repo management, behind your firewall and Enterprise-ready."
       href="http://www.atlassian.com/software/stash?utm_source=bitbucket&amp;utm_medium=link&amp;utm_campaign=bitbucket_footer">Stash</a>
  </li>
  <li>
    <a id="atlassian-sourcetree-link" target="_blank"
       title="A free Git and Mercurial desktop client for Mac or Windows."
       href="http://www.sourcetreeapp.com/?utm_source=bitbucket&amp;utm_medium=link&amp;utm_campaign=bitbucket_footer">SourceTree</a>
  </li>
  <li>
    <a id="atlassian-hipchat-link" target="_blank"
       title="Group chat and IM built for teams."
       href="http://www.hipchat.com/?utm_source=bitbucket&amp;utm_medium=link&amp;utm_campaign=bitbucket_footer">HipChat</a>
  </li>
</ul>
<div id="footer-logo">
  <a target="_blank"
     title="Bitbucket is developed by Atlassian in San Francisco and Austin."
     href="http://www.atlassian.com?utm_source=bitbucket&amp;utm_medium=logo&amp;utm_campaign=bitbucket_footer">Atlassian</a>
</div>

    </section>
  </footer>
</div>


  

<script src="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/jsi18n/en/djangojs.js"></script>

  
    <script src="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/dist/main.js" data-main="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/dist/main" defer></script>
  



<script>
  (function () {
    var ga = document.createElement('script');
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    ga.setAttribute('async', 'true');
    var s = document.getElementsByTagName('script')[0];
    s.parentNode.insertBefore(ga, s);
  }());
</script>


  

<div data-modules="components/mentions/index">
  <script id="mention-result" type="text/html">
    
<div class="aui-avatar aui-avatar-small">
  <div class="aui-avatar-inner">
    <img src="[[avatar_url]]">
  </div>
</div>
[[#display_name]]
  <span class="display-name">[[&display_name]]</span> <small class="username">[[&username]]</small>
[[/display_name]]
[[^display_name]]
  <span class="username">[[&username]]</span>
[[/display_name]]
[[#is_teammate]][[^is_team]]
  <span class="aui-lozenge aui-lozenge-complete aui-lozenge-subtle">teammate</span>
[[/is_team]][[/is_teammate]]

  </script>
  <script id="mention-call-to-action" type="text/html">
    
[[^query]]
<li class="bb-typeahead-item">Begin typing to search for a user</li>
[[/query]]
[[#query]]
<li class="bb-typeahead-item">Continue typing to search for a user</li>
[[/query]]

  </script>
  <script id="mention-no-results" type="text/html">
    
[[^searching]]
<li class="bb-typeahead-item">Found no matching users for <em>[[query]]</em>.</li>
[[/searching]]
[[#searching]]
<li class="bb-typeahead-item bb-typeahead-searching">Searching for <em>[[query]]</em>.</li>
[[/searching]]

  </script>
</div>

  <div data-modules="components/typeahead/emoji/index">
    <script id="emoji-result" type="text/html">
    
<div class="aui-avatar aui-avatar-small">
  <div class="aui-avatar-inner">
    <img src="[[src]]">
  </div>
</div>
<span class="name">[[&name]]</span>

  </script>
  </div>


<div data-modules="components/repo-typeahead/index">
  <script id="repo-typeahead-result" type="text/html">
    <span class="aui-avatar aui-avatar-project aui-avatar-xsmall">
  <span class="aui-avatar-inner">
    <img src="[[avatar]]">
  </span>
</span>
<span class="owner">[[&owner]]</span>/<span class="slug">[[&slug]]</span>

  </script>
</div>
<script id="share-form-template" type="text/html">
    

<div class="error aui-message hidden">
  <span class="aui-icon icon-error"></span>
  <div class="message"></div>
</div>
<form class="aui">
  <table class="widget bb-list aui">
    <thead>
    <tr class="assistive">
      <th class="user">User</th>
      <th class="role">Role</th>
      <th class="actions">Actions</th>
    </tr>
    </thead>
    <tbody>
      <tr class="form">
        <td colspan="2">
          <input type="text" class="text bb-user-typeahead user-or-email"
                 placeholder="Username or email address"
                 autocomplete="off"
                 data-bb-typeahead-focus="false"
                 [[#disabled]]disabled[[/disabled]]>
        </td>
        <td class="actions">
          <button type="submit" class="aui-button" disabled>Add</button>
        </td>
      </tr>
    </tbody>
  </table>
</form>

  </script>
<script id="share-detail-template" type="text/html">
    

[[#username]]
<td class="user
           [[#hasCustomGroups]]custom-groups[[/hasCustomGroups]]"
    [[#error]]data-error="[[error]]"[[/error]]>
  <div title="[[displayName]]">
    <a href="/[[username]]" class="user">
      <img class="avatar avatar16" src="[[avatar]]" />
      <span>[[displayName]]</span>
    </a>
  </div>
</td>
[[/username]]
[[^username]]
<td class="email
           [[#hasCustomGroups]]custom-groups[[/hasCustomGroups]]"
    [[#error]]data-error="[[error]]"[[/error]]>
  <div title="[[email]]">
    <span class="aui-icon aui-icon-small aui-iconfont-email"></span>
    [[email]]
  </div>
</td>
[[/username]]
<td class="role
           [[#hasCustomGroups]]custom-groups[[/hasCustomGroups]]">
  <div>
    [[#group]]
      [[#hasCustomGroups]]
        <select class="group [[#noGroupChoices]]hidden[[/noGroupChoices]]">
          [[#groups]]
            <option value="[[slug]]"
                    [[#isSelected]]selected[[/isSelected]]>
              [[name]]
            </option>
          [[/groups]]
        </select>
      [[/hasCustomGroups]]
      [[^hasCustomGroups]]
      <label>
        <input type="checkbox" class="admin"
               [[#isAdmin]]checked[[/isAdmin]]>
        Administrator
      </label>
      [[/hasCustomGroups]]
    [[/group]]
    [[^group]]
      <ul>
        <li class="permission aui-lozenge aui-lozenge-complete
                   [[^read]]aui-lozenge-subtle[[/read]]"
            data-permission="read">
          read
        </li>
        <li class="permission aui-lozenge aui-lozenge-complete
                   [[^write]]aui-lozenge-subtle[[/write]]"
            data-permission="write">
          write
        </li>
        <li class="permission aui-lozenge aui-lozenge-complete
                   [[^admin]]aui-lozenge-subtle[[/admin]]"
            data-permission="admin">
          admin
        </li>
      </ul>
    [[/group]]
  </div>
</td>
<td class="actions
           [[#hasCustomGroups]]custom-groups[[/hasCustomGroups]]">
  <div>
    <a href="#" class="delete">
      <span class="aui-icon aui-icon-small aui-iconfont-remove">Delete</span>
    </a>
  </div>
</td>

  </script>
<script id="share-team-template" type="text/html">
    

<div class="clearfix">
  <span class="team-avatar-container">
    <img src="[[avatar]]" alt="[[display_name]]" title="[[display_name]]" class="avatar avatar32" />
  </span>
  <span class="team-name-container">
    [[display_name]]
  </span>
</div>
<p class="helptext">
  
    Existing users are granted access to this team immediately.
    New users will be sent an invitation.
  
</p>
<div class="share-form"></div>

  </script>


  

<script id="source-changeset" type="text/html">
  

<a href="/Dorrin/imn_libs/src/[[raw_node]]/[[path]]?at=master"
   class="[[#selected]]highlight[[/selected]]"
   data-hash="[[node]]">
  [[#author.username]]
    <img class="avatar avatar16" src="[[author.avatar]]"/>
    <span class="author" title="[[raw_author]]">[[author.display_name]]</span>
  [[/author.username]]
  [[^author.username]]
    <img class="avatar avatar16" src="https://d3oaxc4q5k2d6q.cloudfront.net/m/0a2f2974a540/img/default_avatar/16/user_blue.png"/>
    <span class="author unmapped" title="[[raw_author]]">[[author]]</span>
  [[/author.username]]
  <time datetime="[[utctimestamp]]" data-title="true">[[utctimestamp]]</time>
  <span class="message">[[message]]</span>
</a>

</script>
<script id="embed-template" type="text/html">
  

<form class="aui embed">
  <label for="embed-code">Embed this source in another page:</label>
  <input type="text" readonly="true" value="&lt;script src=&quot;[[url]]&quot;&gt;&lt;/script&gt;" id="embed-code">
</form>

</script>


  <script id="edit-form-template" type="text/html">
  


<form class="bb-content-container online-edit-form aui"
      data-repository="[[owner]]/[[slug]]"
      data-destination-repository="[[destinationOwner]]/[[destinationSlug]]"
      data-local-id="[[localID]]"
      data-is-writer="[[#isWriter]]true[[/isWriter]][[^isWriter]]false[[/isWriter]]"
      data-has-push-access="[[#hasPushAccess]]true[[/hasPushAccess]][[^hasPushAccess]]false[[/hasPushAccess]]"
      data-is-pull-request="[[#isPullRequest]]true[[/isPullRequest]][[^isPullRequest]]false[[/isPullRequest]]"
      data-hash="[[hash]]"
      data-branch="[[branch]]"
      data-path="[[path]]"
      data-is-create="[[isCreate]]"
      data-preview-url="/xhr/[[owner]]/[[slug]]/preview/[[hash]]/[[encodedPath]]"
      data-preview-error="We had trouble generating your preview."
      data-unsaved-changes-error="Your changes will be lost. Are you sure you want to leave?">
  <div class="bb-content-container-header">
    <div class="bb-content-container-header-primary">
      <h2 class="bb-content-container-heading">
        [[#isCreate]]
          
            Creating <span class="edit-path">[[path]]</span> on branch: <strong>[[branch]]</strong>
          
        [[/isCreate]]
        [[^isCreate]]
          
            Editing <span class="edit-path">[[path]]</span> on branch: <strong>[[branch]]</strong>
          
        [[/isCreate]]
      </h2>
    </div>
    <div class="bb-content-container-header-secondary">
      <div class="hunk-nav aui-buttons">
        <button class="prev-hunk-button aui-button aui-button-light"
              disabled="disabled" aria-disabled="true" title="previous change">&#x25B2;</button>
        <button class="next-hunk-button aui-button aui-button-light"
              disabled="disabled" aria-disabled="true" title="next change">&#x25BC;</button>
      </div>
    </div>
  </div>
  <div class="bb-content-container-body has-header has-footer file-editor">
    <textarea id="id_source"></textarea>
  </div>
  <div class="preview-pane"></div>
  <div class="bb-content-container-footer">
    <div class="bb-content-container-footer-primary">
      <div id="syntax-mode" class="bb-content-container-item field">
        <label for="id_syntax-mode">Syntax mode:</label>
        <select id="id_syntax-mode">
          [[#syntaxes]]
            <option value="[[#mime]][[mime]][[/mime]][[^mime]][[mode]][[/mime]]">[[name]]</option>
          [[/syntaxes]]
        </select>
      </div>
      <div id="indent-mode" class="bb-content-container-item field">
        <label for="id_indent-mode">Indent mode:</label>
        <select id="id_indent-mode">
          <option value="tabs">Tabs</option>
          <option value="spaces">Spaces</option>
        </select>
      </div>
      <div id="indent-size" class="bb-content-container-item field">
        <label for="id_indent-size">Indent size:</label>
        <select id="id_indent-size">
          <option value="2">2</option>
          <option value="4">4</option>
          <option value="8">8</option>
        </select>
      </div>
    </div>
    <div class="bb-content-container-footer-secondary">
      [[^isCreate]]
        <button class="preview-button aui-button aui-button-light"
                disabled="disabled" aria-disabled="true"
                data-preview-label="View diff"
                data-edit-label="Edit file">View diff</button>
      [[/isCreate]]
      <button class="save-button aui-button aui-button-primary"
              disabled="disabled" aria-disabled="true">Commit</button>
      [[^isCreate]]
        <a class="aui-button aui-button-link cancel-link" href="#">Cancel</a>
      [[/isCreate]]
    </div>
  </div>
</form>

</script>
  <script id="commit-form-template" type="text/html">
  

<form class="aui commit-form"
      data-title="Commit changes"
      [[#isDelete]]
        data-default-message="[[filename]] deleted online with Bitbucket"
      [[/isDelete]]
      [[#isCreate]]
        data-default-message="[[filename]] created online with Bitbucket"
      [[/isCreate]]
      [[^isDelete]]
        [[^isCreate]]
          data-default-message="[[filename]] edited online with Bitbucket"
        [[/isCreate]]
      [[/isDelete]]
      data-fork-error="We had trouble creating your fork."
      data-commit-error="We had trouble committing your changes."
      data-pull-request-error="We had trouble creating your pull request."
      data-update-error="We had trouble updating your pull request."
      data-branch-conflict-error="A branch with that name already exists."
      data-forking-message="Forking repository"
      data-committing-message="Committing changes"
      data-merging-message="Branching and merging changes"
      data-creating-pr-message="Creating pull request"
      data-updating-pr-message="Updating pull request"
      data-cta-label="Commit"
      data-cancel-label="Cancel">
  [[#isDelete]]
    <div class="aui-message info">
      <span class="aui-icon icon-info"></span>
      <span class="message">
        
          Committing this change will delete [[filename]] from your repository.
        
      </span>
    </div>
  [[/isDelete]]
  <div class="aui-message error hidden">
    <span class="aui-icon icon-error"></span>
    <span class="message"></span>
  </div>
  [[^isWriter]]
    <div class="aui-message info">
      <span class="aui-icon icon-info"></span>
      <p class="title">
        
          You don't have write access to this repository.
        
      </p>
      <span class="message">
        
          We'll create a fork for your changes and submit a
          pull request back to this repository.
        
      </span>
    </div>
  [[/isWriter]]
  [[#isRename]]
    <div class="field-group">
      <label for="id_path">New path</label>
      <input type="text" id="id_path" class="text" value="[[path]]"/>
    </div>
  [[/isRename]]
  <div class="field-group">
    <label for="id_message">Commit message</label>
    <textarea id="id_message" class="long-field textarea"></textarea>
  </div>
  [[^isPullRequest]]
    [[#isWriter]]
      <fieldset class="group">
        <div class="checkbox">
          [[#hasPushAccess]]
            <input id="id_create-pullrequest" class="checkbox" type="checkbox">
            <label for="id_create-pullrequest">Create a pull request for this change</label>
          [[/hasPushAccess]]
          [[^hasPushAccess]]
            <input id="id_create-pullrequest" class="checkbox" type="checkbox" checked="checked" aria-disabled="true" disabled="true">
            <label for="id_create-pullrequest" title="Branch restrictions do not allow you to update this branch.">Create a pull request for this change</label>
          [[/hasPushAccess]]

        </div>
      </fieldset>
      <div id="pr-fields">
        <div id="branch-name-group" class="field-group">
          <label for="id_branch-name">Branch name</label>
          <input type="text" id="id_branch-name" class="text long-field">
        </div>

        

<div class="field-group" id="id_reviewers_group">
  <label for="reviewers">Reviewers</label>

  
  <input id="reviewers" name="reviewers" type="hidden"
          value=""
          data-mention-url="/xhr/mentions/:dest_username/:dest_slug"
          data-reviewers="[]"
          data-suggested="[]"
          data-participants="[]">

  <div class="error"></div>
  <div class="suggested-reviewers"></div>

</div>


      </div>
    [[/isWriter]]
  [[/isPullRequest]]
  <button type="submit" id="id_submit">Commit</button>
</form>

</script>
  <script id="merge-message-template" type="text/html">
  Merged [[hash]] into [[branch]]

[[message]]

</script>
  <script id="commit-merge-error-template" type="text/html">
  



  We had trouble merging your changes. We stored them on the <strong>[[branch]]</strong> branch, so feel free to
  <a href="/[[owner]]/[[slug]]/full-commit/[[hash]]/[[path]]?at=[[encodedBranch]]">view them</a> or
  <a href="#" class="create-pull-request-link">create a pull request</a>.


</script>
  <script id="selected-reviewer-template" type="text/html">
  <div class="aui-avatar aui-avatar-xsmall">
  <div class="aui-avatar-inner">
    <img src="[[avatar_url]]">
  </div>
</div>
[[display_name]]

</script>
  <script id="suggested-reviewer-template" type="text/html">
  <button class="aui-button aui-button-link" type="button" tabindex="-1">[[display_name]]</button>

</script>
  <script id="suggested-reviewers-template" type="text/html">
  

<span class="suggested-reviewer-list-label">Recent:</span>
<ul class="suggested-reviewer-list unstyled-list"></ul>

</script>

  


  <div id="recently-mentioned-2592829"
       data-value="[]"></div>





  
  
  




<aui-inline-dialog2 id="super-touch-point-dialog"
    
      class="aui-layer aui-inline-dialog"
      data-aui-alignment="bottom right"
    

    
    data-aui-alignment-static="true"
    data-aui-responds-to="toggle"
    data-modules="header/help-menu,js/connect/connect-views,js/connect/super-touch-point"
    aria-hidden="true">

  
  <div class="aui-inline-dialog-contents">
  

    <div id="ace-stp-section" >
      <div id="ace-stp-help-section">
        <h1 class="ace-stp-heading">Help</h1>

        <form id="ace-stp-search-form" class="aui" target="_blank" method="get"
            action="https://support.atlassian.com/customer/search">
          <span id="stp-search-icon" class="aui-icon aui-icon-large aui-iconfont-search"></span>
          <input id="ace-stp-search-form-input" name="q" class="text" type="text" placeholder="Ask a question">
        </form>

        <ul id="ace-stp-help-links">
          <li>
            <a class="support-ga" data-support-gaq-page="DocumentationHome"
                href="https://confluence.atlassian.com/x/bgozDQ" target="_blank">
              Online help
            </a>
          </li>
          <li>
            <a class="support-ga" data-support-gaq-page="GitTutorials"
                href="https://www.atlassian.com/git?utm_source=bitbucket&amp;utm_medium=link&amp;utm_campaign=help_dropdown&amp;utm_content=learn_git"
                target="_blank">
              Learn Git
            </a>
          </li>
          <li>
            <a id="keyboard-shortcuts-link"
               href="#">Keyboard shortcuts</a>
          </li>
          <li>
            <a href="/whats-new" id="features-link">
              Latest features
            </a>
          </li>
          <li>
            <a class="support-ga" data-support-gaq-page="Documentation101"
                href="https://confluence.atlassian.com/x/cgozDQ" target="_blank">
              Bitbucket 101
            </a>
          </li>
          <li>
            <a class="support-ga" data-support-gaq-page="SiteStatus"
                href="http://status.bitbucket.org/" target="_blank">
              Site status
            </a>
          </li>
          <li>
            <a class="support-ga" data-support-gaq-page="Home" href="/support">
              Support
            </a>
          </li>

        </ul>
      </div>

      
        <div id="ace-stp-message-section">
          
<div class="ap-container-onload"
     id="ap-namespace"
     data-source="https://ace-cdn.atlassian.com/stp/current/dialog/ace-stp-dialog-bitbucket.html?username=Dorrin&amp;uuid=%7Ba935453a-fb20-4d32-b84b-b21cf2401f71%7D&amp;xdm_e=https%3A%2F%2Fbitbucket.org&amp;xdm_c=channel-e11ecd30-fe0b-4f21-8cb4-f2a42719cb6a&amp;jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJjb25uZWN0aW9uOjM4Nzc4IiwiaWF0IjoxNDM0NTM5MDI2LCJxc2giOiI1NjdmNjdiM2Q4N2M1NTVkNDE4MTRmNzZhYTZhZGNlNzg5MTcwNTExMzc4MTNjNDNlMjg5ODYwNjBkM2I4OGVkIiwiYXVkIjoiY29ubmVjdGlvbjozODc3OCIsImV4cCI6MTQzODEzOTAyNn0.O1wEnB7PsX_cX2vjX0-NVAuT1ylJZoHh-XiiYUalLeU" data-key="help-panel"
     data-name="help panel"
     data-width="649" data-height="370"
     data-dlg="false" data-general="true"
     data-enc-context=""
     
     >
  <div class="ap-content" id="embedded-namespace"></div>
  <div class="ap-stats hidden">
    <div class="ap-loading ap-status hidden">
      <small>
        <div class="small-spinner"></div>
        <div class="description">
          
            Loading add-on <a href="https://ace-cdn.atlassian.com" class="ap-doc-url" target="_blank">help panel</a>.
          
        </div>
      </small>
    </div>
    <div class="ap-load-timeout ap-status hidden">
      <small>
        <div class="small-spinner"></div>
        <div class="description">
          
            Add-on <a href="https://ace-cdn.atlassian.com" class="ap-doc-url" target="_blank">help panel</a> is not responding.
            Wait or <a href="#" class="ap-btn-cancel">cancel</a>?
          
        </div>
      </small>
    </div>
    <div class="ap-load-error ap-status hidden">
      <small>
        <div class="description">
          
            Add-on <a href="https://ace-cdn.atlassian.com" class="ap-doc-url" target="_blank">help panel</a> failed to load.
          
        </div>
      </small>
    </div>
  </div>
</div>

        </div>
      
    </div>

  
  </div>
  

</aui-inline-dialog2>
  


  <div class="omnibar" data-modules="js/components/omnibar/index">
    <form class="omnibar-form aui"></form>
  </div>
  <script id="omnibar-form-template" type="text/html">
    <div class="omnibar-input-container">
  <input class="omnibar-input" type="text">
</div>
<ul class="omnibar-result-group-list"></ul>

  </script>
  <script id="omnibar-blank-slate-template" type="text/html">
    

<div class="omnibar-blank-slate">No results found</div>

  </script>
  <script id="omnibar-result-group-list-item-template" type="text/html">
    <div class="omnibar-result-group-header clearfix">
  <h2 class="omnibar-result-group-label" title="[[label]]">[[label]]</h2>
  <span class="omnibar-result-group-context" title="[[context]]">[[context]]</span>
</div>
<ul class="omnibar-result-list unstyled-list"></ul>

  </script>
  <script id="omnibar-result-list-item-template" type="text/html">
    <span class="omnibar-result-label">[[&label]]</span>
[[#context]]
  <span class="omnibar-result-context">[[context]]</span>
[[/context]]

  </script>




</body>
</html>
