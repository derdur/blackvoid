# Extract Photo URLS



## Target == { Photo | IMG.SRC }


### List / Don't decode                           
```
javascript:(function(){var urls=[];document.querySelectorAll('img').forEach(function(img){var url=img.src;if(url){urls.push(url)}});var html='<html><head><title>All URLs on the Page</title></head><body><h1>All URLs on the Page:</h1><ul>';urls.forEach(function(url){html+='<li><a href="'+url+'" target="_blank">'+url+'</a></li>'});html+='</ul></body></html>';var newWindow=window.open();newWindow.document.write(html)})();                      
```



## Target == { Link | A.HREF }


### List / Re-tag | Show photo
javascript:(function(){var urls=[];document.querySelectorAll('a').forEach(function(a){var url=a.href;if(url){urls.push(url)}});var html='<html><head><title>All URLs on the Page</title></head><body><h1>All URLs on the Page:</h1><ul>';urls.forEach(function(url){html+='0<br><img src="' +url+ '"></img><li><a href="'+url+'" target="_blank">'+url+'</a></li>'});html+='</ul></body></html>';var newWindow=window.open();newWindow.document.write(html)})();                 


`javascript:(function(){var urls=[];document.querySelectorAll('a').forEach(function(a){var url=a.href;if(url){urls.push(url)}});var html='<html><head><title>All URLs on the Page</title></head><body><h1>All URLs on the Page:</h1><ul>';urls.forEach(function(url){html+='0<br><img src="' +url+ '"></img><li><a href="'+url+'" target="_blank">'+url+'</a></li>'});html+='</ul></body></html>';var newWindow=window.open();newWindow.document.write(html)})();`


