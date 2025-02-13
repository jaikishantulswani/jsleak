**Changes**

In this change the tool look for secrets on the go whenever a new link found.





### Description

I was developing jsleak during most of my free time for my own need.It is easy-to-use command-line tool designed to uncover secrets and links in JavaScript files or source code. The jsleak was inspired by [Linkfinder](https://github.com/GerbenJavado/LinkFinder) and regexes are collected from multiple sources.  

### Features:

- Discover secrets in JS files such as API keys, tokens, and passwords.
- Identify links in the source code.
- Complete Url Function
- Concurrent processing for scanning of multiple Urls
- Check status code if the url is alive or not

### Instllation

```
go install github.com/channyein1337/jsleak/@latest
```

### Usage

To display help message

```
jsleak -h
```

![](https://raw.githubusercontent.com/channyein1337/jsleak/main/images/help.png)

Secret Finder

```
echo http://testphp.vulnweb.com/ | jsleak -s
```

![](https://raw.githubusercontent.com/channyein1337/jsleak/main/images/secret.png)


Link Finder

```
echo http://testphp.vulnweb.com/ | jsleak -l
```

![](https://raw.githubusercontent.com/channyein1337/jsleak/main/images/linkfinder.png)

Complete Url

```
echo http://testphp.vulnweb.com/ | jsleak -e
```

![](https://raw.githubusercontent.com/channyein1337/jsleak/main/images/completeURL.png)

Check Status

```
echo http://testphp.vulnweb.com/ | jsleak -c 20 -k
```

![](https://raw.githubusercontent.com/channyein1337/jsleak/main/images/status_code.png)

You can also use multiple flags 

```
echo http://testphp.vulnweb.com/ | jsleak -c 20 -l -s 
```

![](https://raw.githubusercontent.com/channyein1337/jsleak/main/images/multipleFlags.png)

Running with Urls

```
cat urls.txt | jsleak -l -s -c 30
```

![](https://raw.githubusercontent.com/channyein1337/jsleak/main/images/file.png)

### To Do

- Support scanning local files.
- Support scanning apk files.
- Update Regex.
- Support mulitple user agents.

### Credit and thanks to all the following resources
- https://github.com/GerbenJavado/LinkFinder
- https://github.com/0xsha/GoLinkFinder
