# NGNIX based web application

<img src="https://github.com/DanilaMartynuk/rebrain-devops-task1-/blob/main/nginx.png" align="right"
     alt="nginx logo" width="150" height="150">

Nginx is a web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache. The software was created by Igor Sysoev and publicly released in 2004. Nginx is free and open-source software, released under the terms of the 2-clause BSD license.

What is NGINX is used for?

* **web serving**
* **reverse proxying**
* **caching**
* **load balancing**
* **media streaming**

## Nginx in comparison to Apache

*Nginx* was written with an explicit goal of outperforming the Apache web server.[42] Out of the box, serving static files, Nginx uses much less memory than Apache, and can handle roughly four times as many requests per second. However, this performance boost comes at a cost of decreased flexibility, such as the ability to override systemwide access settings on a per-file basis (Apache accomplishes this with an .htaccess file, while Nginx has no such feature built in).

Formerly, adding third-party modules to Nginx required recompiling the application from source with the modules statically linked. This was partially overcome in version 1.9.11 in February 2016, with the addition of dynamic module loading. However, the modules still must be compiled at the same time as Nginx, and not all modules are compatible with this system; some require the older static linking process.

Nginx is generally considered to be less stable on Windows Server than it is on Linux, while Apache has equal support for both.

<p align="center">
<img src="https://github.com/DanilaMartynuk/rebrain-devops-task1-/blob/main/nginxvsapache.png"
  alt="Nginx vs apache"
</p>

## **Configuration File’s Structure**

 *Nginx* consists of modules which are controlled by directives specified in the configuration file. Directives are divided into simple directives and block directives. A simple directive consists of the name and parameters separated by spaces and ends with a semicolon (;). A block directive has the same structure as a simple directive, but instead of the semicolon it ends with a set of additional instructions surrounded by braces ({ and }). If a block directive can have other directives inside braces, it is called a context (examples: events, http, server, and location).

Directives placed in the configuration file outside of any contexts are considered to be in the main context. The events and http directives reside in the main context, server in http, and location in server.

<sub> config structure example </sub>
``` 
http{
	server {
	    location / {
	        proxy_pass http://localhost:8080/;
	    }
	
	    location ~ \.(gif|jpg|png)$ {
	        root /data/images;
	    }
	}
}
```


## Who Uses *Nginx*

1. [Netflix](https://www.netflix.com)
2. [Hulu](https://www.hulu.com)
3. [Airbnb](https://www.airbnb.com)
4. [Github](https://github.com) 

