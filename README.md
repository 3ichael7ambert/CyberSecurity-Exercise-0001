# CyberSecurity-Exercise-0001
My first cyber security exercise; I hacked a bank

I did this exercise through a terminal and a virtual machine via www.tryhackme.com

In this exercise I entered the following command into the unix terminal (make sure dependencies are installed),

```bash
gobuster -u http://fakebank.com -w wordlist.txt dir
```

In the command above, -u is used to state the website we're scanning, -w takes a list of words to iterate through to find hidden pages.
this command then returned the following

```bash
ubuntu@tryhackme:~/Desktop$ gobuster -u http://fakebank.com -w wordlist.txt dir
=====================================================
Gobuster v2.0.1
=====================================================
[+] Mode         : dir
[+] Url/Domain   : http://fakebank.com/
[+] Threads      : 10
[+] Wordlist     : wordlist.txt
[+] Status codes : 200,204,301,302,307,403
[+] Timeout      : 10s
=====================================================
2022/04/11 18:23:28 Starting gobuster
=====================================================
/images (Status: 301)
/DIRECTORY_NAME_OUTPUT (Status: 200)
/bank-transfer (Status: 200)
=====================================================
2022/04/11 18:23:38 Finished
=====================================================
```

As you can see there are two directories
images and bank-transfer

as long as we are logged in, we may enter
http://fakebank.com/bank-transfer to access this hidden page


