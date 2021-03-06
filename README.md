# webkit
### Center:
	body {
	    text-align: center;
	}
	.center {
	    text-align: left;
	}
	@media (min-width: 1300px) {
	    .center {
		display: inline-block;
		width: 1300px;
	    }
	}

### Web Apps For iOS:
#### 1. Make it standalone:
    <meta name="apple-mobile-web-app-capable" content="yes">

#### 2. Add a custom icon:
    <link rel="apple-touch-icon" href="single-page-icon.png">
    <link rel="apple-touch-icon" href="touch-icon-iphone.png">
	<link rel="apple-touch-icon" sizes="152x152" href="touch-icon-ipad.png">
	<link rel="apple-touch-icon" sizes="180x180" href="touch-icon-iphone-retina.png">
	<link rel="apple-touch-icon" sizes="167x167" href="touch-icon-ipad-retina.png">

#### 3. Add a custom splash screen:
    <link rel="apple-touch-startup-image" href="launch.png">

#### 5. Give it a short name:
    <meta name="apple-mobile-web-app-title" content="Appscope">

#### 6. Disable selection, highlighting, and callouts:
##### 6.1 Disable text selection:
    body {
	   -webkit-user-select: none;
	}
##### 6.2 Disable highlighting:
    body {
	   -webkit-tap-highlight-color: transparent;
	}
##### 6.3 Disable callouts:
    body {
	   -webkit-touch-callout: none;
	}


#### 7. JS-FIX (Disable new tab on link)
	<script>(function(a,b,c){if(c in b&&b[c]){var d,e=a.location,f=/^(a|html)$/i;a.addEventListener("click",function(a){d=a.target;while(!f.test(d.nodeName))d=d.parentNode;"href"in d&&(d.href.indexOf("http")||~d.href.indexOf(e.host))&&(a.preventDefault(),e.href=d.href)},!1)}})(document,window.navigator,"standalone")</script>
	
#### 8. No zoom
	<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
