#!/usr/bin/python2
#coding=utf-8
#The Credit For This Code Goes To Tech Qaiser
#If You Wanna Take Credits For This Code, Please Look Yourself Again...
#Reserved2020


import os,sys,time,datetime,random,hashlib,re,threading,json,urllib,cookielib,requests,mechanize
from multiprocessing.pool import ThreadPool
from requests.exceptions import ConnectionError
from mechanize import Browser


reload(sys)
sys.setdefaultencoding('utf8')
br = mechanize.Browser()
br.set_handle_robots(False)
br.set_handle_refresh(mechanize._http.HTTPRefreshProcessor(),max_time=1)
br.addheaders = [('User-Agent', 'Opera/9.80 (Android; Opera Mini/32.0.2254/85. U; id) Presto/2.12.423 Version/12.16')]

def keluar():
	print "\x1b[1;91mExit"
	os.sys.exit()

def acak(b):
    w = 'ahtdzjc'
    d = ''
    for i in x:
        d += '!'+w[random.randint(0,len(w)-1)]+i
    return cetak(d)


def cetak(b):
    w = 'ahtdzjc'
    for i in w:
        j = w.index(i)
        x= x.replace('!%s'%i,'\033[%s;1m'%str(31+j))
    x += '\033[0m'
    x = x.replace('!0','\033[0m')
    sys.stdout.write(x+'\n')


def jalan(z):
	for e in z + '\n':
		sys.stdout.write(e)
		sys.stdout.flush()
		time.sleep(0.001)

#### colours ####
B='\033[1;96m'
R='\033[1;91m'
G='\033[1;92m'
W='\033[1;97m'
S='\033[1;96m'
P='\033[1;95m'
Y='\033[1;93m'
R='\033[1;94m'

#Dev: qaiser
##### LOGO #####
logo = """
\033[1;93m╭━╮╱╭╮
\033[1;93m┃┃╰╮┃┃
\033[1;93m┃╭╮╰╯┣━━┳╮╭┳╮╭┳╮
\033[1;93m┃┃╰╮┃┃╭╮┃┃┃┃╰╯┣┫
\033[1;93m┃┃╱┃┃┃╰╯┃╰╯┃┃┃┃┃
\033[1;93m╰╯╱╰━┻━━┻━━┻┻┻┻╯
\033[1;93m╱╱╱

\033[1;91m--> GITHUB :- https://github.com/TechQaiser

\033[1;92m--> FACEBOOK :- Qaiser Abbas

\033[1;93m--> YOUTUBE :-  Tech Qaiser

\033[1;94m--> DISCLAIMRR :- This Tool Is only for Educational Purposes I am not responsible for any miss use

\033[1;95m--> NOTE  :- Need First Hand GirlFriend :-)

"""
logo2 = """
\033[1;93m╭━╮╱╭╮
\033[1;93m┃┃╰╮┃┃
\033[1;93m┃╭╮╰╯┣━━┳╮╭┳╮╭┳╮
\033[1;93m┃┃╰╮┃┃╭╮┃┃┃┃╰╯┣┫
\033[1;93m┃┃╱┃┃┃╰╯┃╰╯┃┃┃┃┃
\033[1;93m╰╯╱╰━┻━━┻━━┻┻┻┻╯
\033[1;93m╱╱╱

\033[1;91m--> GITHUB :- https://github.com/TechQaiser

\033[1;92m--> FACEBOOK :- Qaiser Abbas

\033[1;93m--> YOUTUBE :-  Tech Qaiser

\033[1;94m--> DISCLAIMRR :- This Tool Is only for Educational Purposes I am not responsible for any miss use

\033[1;95m--> NOTE  :- Need First Hand GirlFriend :-)

"""
logo3 = """
\033[1;93m╭━╮╱╭╮
\033[1;93m┃┃╰╮┃┃
\033[1;93m┃╭╮╰╯┣━━┳╮╭┳╮╭┳╮
\033[1;93m┃┃╰╮┃┃╭╮┃┃┃┃╰╯┣┫
\033[1;93m┃┃╱┃┃┃╰╯┃╰╯┃┃┃┃┃
\033[1;93m╰╯╱╰━┻━━┻━━┻┻┻┻╯
\033[1;93m╱╱╱

\033[1;91m--> GITHUB :- https://github.com/TechQaiser

\033[1;92m--> FACEBOOK :- Qaiser Abbas

\033[1;93m--> YOUTUBE :-  Tech Qaiser

\033[1;94m--> DISCLAIMRR :- This Tool Is only for Educational Purposes I am not responsible for any miss use

\033[1;95m--> NOTE  :- Need First Hand GirlFriend :-)

"""
logo4 = """
\033[1;93m╭━╮╱╭╮
\033[1;93m┃┃╰╮┃┃
\033[1;93m┃╭╮╰╯┣━━┳╮╭┳╮╭┳╮
\033[1;93m┃┃╰╮┃┃╭╮┃┃┃┃╰╯┣┫
\033[1;93m┃┃╱┃┃┃╰╯┃╰╯┃┃┃┃┃
\033[1;93m╰╯╱╰━┻━━┻━━┻┻┻┻╯
\033[1;93m╱╱╱

\033[1;91m--> GITHUB :- https://github.com/TechQaiser

\033[1;92m--> FACEBOOK :- Qaiser Abbas

\033[1;93m--> YOUTUBE :-  Tech Qaiser

\033[1;94m--> DISCLAIMRR :- This Tool Is only for Educational Purposes I am not responsible for any miss use

\033[1;95m--> NOTE  :- Need First Hand GirlFriend :-)

"""
logo5 = """
\033[1;93m╭━╮╱╭╮
\033[1;93m┃┃╰╮┃┃
\033[1;93m┃╭╮╰╯┣━━┳╮╭┳╮╭┳╮
\033[1;93m┃┃╰╮┃┃╭╮┃┃┃┃╰╯┣┫
\033[1;93m┃┃╱┃┃┃╰╯┃╰╯┃┃┃┃┃
\033[1;93m╰╯╱╰━┻━━┻━━┻┻┻┻╯
\033[1;93m╱╱╱

\033[1;91m--> GITHUB :- https://github.com/TechQaiser

\033[1;92m--> FACEBOOK :- Qaiser Abbas

\033[1;93m--> YOUTUBE :-  Tech Qaiser

\033[1;94m--> DISCLAIMRR :- This Tool Is only for Educational Purposes I am not responsible for any miss use

\033[1;95m--> NOTE  :- Need First Hand GirlFriend :-)

"""
logo6 = """
\033[1;93m╭━╮╱╭╮
\033[1;93m┃┃╰╮┃┃
\033[1;93m┃╭╮╰╯┣━━┳╮╭┳╮╭┳╮
\033[1;93m┃┃╰╮┃┃╭╮┃┃┃┃╰╯┣┫
\033[1;93m┃┃╱┃┃┃╰╯┃╰╯┃┃┃┃┃
\033[1;93m╰╯╱╰━┻━━┻━━┻┻┻┻╯
\033[1;93m╱╱╱

\033[1;91m--> GITHUB :- https://github.com/TechQaiser

\033[1;92m--> FACEBOOK :- Qaiser Abbas

\033[1;93m--> YOUTUBE :-  Tech Qaiser

\033[1;94m--> DISCLAIMRR :- This Tool Is only for Educational Purposes I am not responsible for any miss use

\033[1;95m--> NOTE  :- Need First Hand GirlFriend :-)

"""
logo7 = """
\033[1;93m╭━╮╱╭╮
\033[1;93m┃┃╰╮┃┃
\033[1;93m┃╭╮╰╯┣━━┳╮╭┳╮╭┳╮
\033[1;93m┃┃╰╮┃┃╭╮┃┃┃┃╰╯┣┫
\033[1;93m┃┃╱┃┃┃╰╯┃╰╯┃┃┃┃┃
\033[1;93m╰╯╱╰━┻━━┻━━┻┻┻┻╯
\033[1;93m╱╱╱

\033[1;91m--> GITHUB :- https://github.com/TechQaiser

\033[1;92m--> FACEBOOK :- Qaiser Abbas

\033[1;93m--> YOUTUBE :-  Tech Qaiser

\033[1;94m--> DISCLAIMRR :- This Tool Is only for Educational Purposes I am not responsible for any miss use

\033[1;95m--> NOTE  :- Need First Hand GirlFriend :-)

"""
logo8 = """
\033[1;93m╭━╮╱╭╮
\033[1;93m┃┃╰╮┃┃
\033[1;93m┃╭╮╰╯┣━━┳╮╭┳╮╭┳╮
\033[1;93m┃┃╰╮┃┃╭╮┃┃┃┃╰╯┣┫
\033[1;93m┃┃╱┃┃┃╰╯┃╰╯┃┃┃┃┃
\033[1;93m╰╯╱╰━┻━━┻━━┻┻┻┻╯
\033[1;93m╱╱╱

\033[1;91m--> GITHUB :- https://github.com/TechQaiser

\033[1;92m--> FACEBOOK :- Qaiser Abbas

\033[1;93m--> YOUTUBE :-  Tech Qaiser

\033[1;94m--> DISCLAIMRR :- This Tool Is only for Educational Purposes I am not responsible for any miss use

\033[1;95m--> NOTE  :- Need First Hand GirlFriend :-)

"""
logo11 = """
\033[1;93m╭━╮╱╭╮
\033[1;93m┃┃╰╮┃┃
\033[1;93m┃╭╮╰╯┣━━┳╮╭┳╮╭┳╮
\033[1;93m┃┃╰╮┃┃╭╮┃┃┃┃╰╯┣┫
\033[1;93m┃┃╱┃┃┃╰╯┃╰╯┃┃┃┃┃
\033[1;93m╰╯╱╰━┻━━┻━━┻┻┻┻╯
\033[1;93m╱╱╱
