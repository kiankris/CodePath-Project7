# Project 7 - WordPress Pentesting

Time spent: 9 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) CVE-2015-5622
  - [X] Summary: Anyone with posting permissions can insert formatted HTML wiht JS on a page/post
    - Vulnerability types: XSS
    - Tested in version: 4.2.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: 
  - [X] Steps to recreate: Create new post, select text mode option on the right of the text box, insert malicious html code
  - [ ] Affected source code:
    - [Link 1] - 

2. (Required) OVE-20160717-0003
  - [X] Summary: WordPress audio playfist functionality is affected by Cross-Site Scripting
    - Vulnerability types: XSS
    - Tested in version: 4.5.3
    - Fixed in version: 4.7.3
  - [ ] GIF Walkthrough: 
  - [X] Steps to recreate: A specific mp3 audio file for the attack is available at
	https://www.securify.nl/advisory/SFY20160742/xss.mp3. Once downloaded upload to the Media Library, then insert an Audio Playist in a post containing the MP3
  - [X] Affected source code:
    - [Link 1] /wp-includes/js/mediaelement/wp-playlist.js
		- [Link 2] /wp-includes/media.php 

3. (Required) CVE-2015-5 4.2.2
  - [X] Summary: HTML and form validation are performed separetely, allowing specific payloads to bypass the whitelist check of the individual portions and be rendered. Inserting into a post a shortcode will cause the rendering of the post to construct an XSS attack.
    - Vulnerability types: XSS
    - Tested in version:
    - Fixed in version: 4.2.5
  - [ ] GIF Walkthrough: 
  - [X] Steps to recreate:
		Insert into a post [caption width="1" caption='<a href="' ">]</a><a href="http://onMouseOver='alert(1)'">Click me</a> 
  - [X] Affected source code:
    - [Link 1] wp-includes / shortcodes.php

## Assets

List any additional assets, such as scripts or files
 - https://www.securify.nl/advisory/SFY20160742/xss.mp3.

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)


## Notes

Setup for this lab was very difficult errors would occur with no real indication as to what happened. Otherwise learning and setting up the environment was fun. 

## License

    Copyright 2017 Kiankris VIllagonzalo

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
