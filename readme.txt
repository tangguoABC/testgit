#��excel���Ĳ����õ���ģ�飺  xlwt��д���� xlrd����ȡ���

import  xlwt
f = xlwt.Workbook(encoding='utf-8')   #��һ���ļ���
sheet =f.add_sheet('123')             #���һ����ǩҳ123��
g=open(r'C:\Users\Tangguo\PycharmProjects\untitled\venv\Include\a.text','r',encoding='utf-8')  #���ļ�
s=g.readlines() #��ȡ�������� ������һ���б���
print(s)
for j,i in enumerate(s):
    b=i.split(',')            #�������е�����Ϊ�ָ�����#���ַ�����Ϊ�б�
    print(b)
    for p,w in enumerate(b):
        sheet.write(j,p,w)
f.save('text.xls')

