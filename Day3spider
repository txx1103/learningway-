import urllib
from urllib import request
import time
import random

 
agent1= "Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10_6_8; en-us) AppleWebKit/534.50 (KHTML, like Gecko) Version/5.1 Safari/534.50"
agent2="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:7.0a1) Gecko/20110623 Firefox/7.0a1 Fennec/7.0a1  "
agent3=" Mozilla/5.0 (Linux; U; Android 3.0; en-us; Xoom Build/HRI39) AppleWebKit/534.1(KHTML, like Gecko) Version/4.0 Safari/534.13  "
agent4="Mozilla/5.0 (iPhone; U; CPU iPhone OS 4_0 like Mac OS X; en-us) AppleWebKit/532.9 (KHTML, like Gecko) Version/4.0.5 Mobile/8A293 Safari/6531.22.7"
agent5 = "Mozilla/5.0 (compatible; MSIE 9.0; Windows NT 6.1; Trident/5.0"
list1=[agent1,agent2, agent3, agent4,agent5]
agent =random.choice(list1)
print(agent)
header ={ 
 "user-agent": agent
}
for i in range(1,8):
    print("https://www.sogou.com/sie?hdq=AQxRG-4493&query=sublime自动补全&page=" +str(i ))

def loadpage(fullurl,filename):
    print("正在下崽",filename)
    req = request.Request(fullurl,headers = header)
    resp = request.request.urlopen(req).read()
    return (resp)

def  baocun(html,filename):
	print("正在保存",filename)

	with open(filename,"wb")as f:
		f.write(html)
	
	print("+++++++++++")//仅是为了区分


def tiebaospider(url,begain,end):
	for page in range(begin,end+1):
		pn = (page+1)
		fullurl = url+"&page="+str(pn)
		filename ="D:/第"+str(page)+"页.html"

		html = loadpage(fullurl,filename)
		writepage(html,filename)
	 

if __name__ == '__main__':
	kw = input("请输入贴吧名")
	begin = int(input("请输入起思明"))
	end  = int(input("请输入结束页"))
	url = "http://tieba.baidu.com/f?"
	key = urllib.parse.urlencode({"kw":kw})
	url = url +key
	time(10)
	tiebaospider(url,begain,end)

#remarking
！！！The url of the crawling page entered here is the one I find at will.
Please find the agent and the url of the crawling page when you use it for reference



  
