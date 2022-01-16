# Patika-Python-Proje
## Modül bitirme soruları

#### 1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]

'''
    n=[]
    q=[]
    a=[[1,'a',['cat'],2],[[[3]],'dog'],4,5]
    
    for i in a:
        if type(i)==type(q):
            for y in i:
                if type(y)==type(q):
                    for j in y:
                        if type(j)==type(q):
                            for k in j:
                                n.append(k)
                else:
                    n.append(y)
        else:
            n.append(i)
    print(n)
'''

#### 2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:

    b = [[1, 2], [3, 4], [5, 6, 7]]
    n=[]
    
    for i in b:
        n.append(i[::-1])
    n=n[::-1]
    print(n)
