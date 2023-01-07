# BaitapPython
#a) (1,5 điểm) Cho định nghĩa hàm Combination(k,n) như sau:
#-  Combination(k,n) =1 nếu k==0 hoặc k==n
#-  Combination(k,n) = Combination(k-1,n-1) + Combination(k,n-1) nếu 1<k<n
#=> Định nghĩa hàm Combination(k,n) theo định nghĩa trên.
def Combination(k,n):
    if ((k==0) or (k==n)):
        return 1
    else:
        return Combination(k-1,n-1)+Combination(k,n-1)
#b) (1,5 điểm) Định nghĩa hàm ChenThuTu(x,L) để chèn giá trị x vào danh sách L đã được sắp xếp theo thứ tự tăng dần sao cho vẫn đảm bảo thứ tự sau khi chèn.
def ChenThuTu(x,L):
    dung=0
    i=0
    while ((dung==0) and (i<len(L))):
        if L[i]>=x:
            dung=1
        else:
            i=i+1
    L.insert(i,x)
    #  nếu dung==1 thì chèn vào đầu hoặc giữa danh sách
    # nếu dừng ==0 thì chèn vào cuối danh sách
#c) (2,0) Định nghĩa hàm DemSoLan(x,L) để đếm số lần xuất hiện của giá trị x trong danh sách L.
def DemSoLan(x,L):
    kq=0
    for i in range (len(L)):
        if (x==L[i]):
            kq=kq+1
    return kq
#d) (2,0 điểm) Định nghĩa hàm RemoveDuplicate(L) để loại bỏ những giá trị trùng nhau trong danh sách L (ví dụ số 2 xuất hiện nhiều lần thì chỉ giữ lại 1 lần).
def RemoveDuplicate(L):
    S=set()
    for i in range (len(L)):
        S.add(L[i])
    L2=[]
    for x in S:
        L2.insert(len(L2),x)
    return L2
#e) (0,5 điểm) Nhập vào 2 số nguyên dương n, k, gọi hàm Combination(k,n) và in ra kết quả.
n=int(input("Nhap so nguyen duong n="))
k=int(input("Nhap so nguyen duong k="))
print("Ket qua Combination(",k,",",n,")=",Combination(k,n))
#f) (1,0 điểm) Nhập vào danh sách số nguyên L và số nguyên x, xuất kết quả nhập ra màn hình.
n=int(input("Danh sach bao nhieu gia tri ?"))
L=[]
for i in range(n):
    print("Nhap gia tri thu ",i+1, end=" ")
    x=int(input())
    L.insert(len(L),x)
x=int(input("Nhap so nguyen x can chen ="))
print("Danh sach vua nhap", L)
#g) (1,5 điểm):
#- Gọi hàm ChenThuTu(x,L) và in ra kết quả sau khi chèn x vào danh sách L;
#- Gọi hàm DemSoLan(x,L) và in ra kết quả;
#- Gọi hàm RemoveDuplicate(L) và in ra kết quả sau khi loại phần tử trùng nhau trong danh sách L;
ChenThuTu(x,L)
print("Danh sach sau khi them ",x," la ", L)
print("Gia tri",x,"xuat hien ",DemSoLan(x,L),"lan")
print("Ket qua khu trung ",RemoveDuplicate(L) )#a) (1,5 điểm) Cho định nghĩa hàm Combination(k,n) như sau:
#-  Combination(k,n) =1 nếu k==0 hoặc k==n
#-  Combination(k,n) = Combination(k-1,n-1) + Combination(k,n-1) nếu 1<k<n
#=> Định nghĩa hàm Combination(k,n) theo định nghĩa trên.
def Combination(k,n):
    if ((k==0) or (k==n)):
        return 1
    else:
        return Combination(k-1,n-1)+Combination(k,n-1)
#b) (1,5 điểm) Định nghĩa hàm ChenThuTu(x,L) để chèn giá trị x vào danh sách L đã được sắp xếp theo thứ tự tăng dần sao cho vẫn đảm bảo thứ tự sau khi chèn.
def ChenThuTu(x,L):
    dung=0
    i=0
    while ((dung==0) and (i<len(L))):
        if L[i]>=x:
            dung=1
        else:
            i=i+1
    L.insert(i,x)
    #  nếu dung==1 thì chèn vào đầu hoặc giữa danh sách
    # nếu dừng ==0 thì chèn vào cuối danh sách
#c) (2,0) Định nghĩa hàm DemSoLan(x,L) để đếm số lần xuất hiện của giá trị x trong danh sách L.
def DemSoLan(x,L):
    kq=0
    for i in range (len(L)):
        if (x==L[i]):
            kq=kq+1
    return kq
#d) (2,0 điểm) Định nghĩa hàm RemoveDuplicate(L) để loại bỏ những giá trị trùng nhau trong danh sách L (ví dụ số 2 xuất hiện nhiều lần thì chỉ giữ lại 1 lần).
def RemoveDuplicate(L):
    S=set()
    for i in range (len(L)):
        S.add(L[i])
    L2=[]
    for x in S:
        L2.insert(len(L2),x)
    return L2
#e) (0,5 điểm) Nhập vào 2 số nguyên dương n, k, gọi hàm Combination(k,n) và in ra kết quả.
n=int(input("Nhap so nguyen duong n="))
k=int(input("Nhap so nguyen duong k="))
print("Ket qua Combination(",k,",",n,")=",Combination(k,n))
#f) (1,0 điểm) Nhập vào danh sách số nguyên L và số nguyên x, xuất kết quả nhập ra màn hình.
n=int(input("Danh sach bao nhieu gia tri ?"))
L=[]
for i in range(n):
    print("Nhap gia tri thu ",i+1, end=" ")
    x=int(input())
    L.insert(len(L),x)
x=int(input("Nhap so nguyen x can chen ="))
print("Danh sach vua nhap", L)
#g) (1,5 điểm):
#- Gọi hàm ChenThuTu(x,L) và in ra kết quả sau khi chèn x vào danh sách L;
#- Gọi hàm DemSoLan(x,L) và in ra kết quả;
#- Gọi hàm RemoveDuplicate(L) và in ra kết quả sau khi loại phần tử trùng nhau trong danh sách L;
ChenThuTu(x,L)
print("Danh sach sau khi them ",x," la ", L)
print("Gia tri",x,"xuat hien ",DemSoLan(x,L),"lan")
print("Ket qua khu trung ",RemoveDuplicate(L) )
