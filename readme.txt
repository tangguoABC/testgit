#对excel表格的操作用到的模块：  xlwt（写入表格） xlrd（读取表格）

import  xlwt
f = xlwt.Workbook(encoding='utf-8')   #打开一个文件。
sheet =f.add_sheet('123')             #添加一个标签页123。
g=open(r'C:\Users\Tangguo\PycharmProjects\untitled\venv\Include\a.text','r',encoding='utf-8')  #打开文件
s=g.readlines() #读取所有内容 并放在一个列表中
print(s)
for j,i in enumerate(s):
    b=i.split(',')            #以括号中的内容为分隔符；#将字符串变为列表
    print(b)
    for p,w in enumerate(b):
        sheet.write(j,p,w)
f.save('text.xls')

