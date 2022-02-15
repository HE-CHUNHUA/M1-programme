# M1-programme
rappel des informations sur la promotion du site 
 import requests
from bs4 import BeautifulSoup
url='https://www.galerieslafayette.com/s?query=sac%20chloe'
headers={
    'User-Agent':'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/98.0.4758.82 Safari/537.36'
}
for pageNum in range(1,3):
    new_url=format(url%pageNum)
    page_text=requests.get(url=new_url,headers=headers)
    soup=BeautifulSoup(page_text.content,'lxml')
    price_list=soup.select('.selection class=price>span class')
    for p in price_list:
    price=?.string
print(price_list)
