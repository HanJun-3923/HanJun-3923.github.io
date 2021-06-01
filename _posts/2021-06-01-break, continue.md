---
layout: single
title: "break, continue"
---
문제 1
-
[문제 상황]  
DAUM에서는 주기적으로 비밀번호를 변경하여 개인정 보를 안전하게 보호하고 있습니다. ID는 ‘알파벳+숫자’ 의 조합으로, ‘kyunghee8323’과 같이 만들 수 있습니 다. 새로 변경하려는 비밀번호에서 연속된 3글자가 
ID에 들어 있다면 그것은 사용이 허락되지 않습니다. 위에서 설명한 것과 같이 비밀번호 변경 가능 여부를 체크한 후에 비밀번호를 변경하는 프로그램을 작성하시오.  

~~~python
id = 'gkswns0326'
password = input("변경하시려는 비밀번호를 입력해주세요: ")
bo = True

for i in range(len(password) - 2):
    if password[i : i + 3] in id:
        bo = False
        break
    
if bo:
    print("비밀번호를 사용할 수 있습니다.")
else:
    print("비밀번호를 사용할 수 없습니다.")
~~~

[출력 결과]  
(비밀번호가 koriangk028 이면)  
비밀번호를 사용할 수 있습니다.    

(비밀번호가 wiosd032wj 이면)  
비밀번호를 사용할 수 없습니다.  

문제 2
-
[문제 상황]
365 자원봉사포털에서는 4월 3주 도서관에서의 주말 봉사활동지원을 받고 있습니다. 지원자의 이름과 전화번호를 저장하여 조건에 따라 처리한 후 결과를 출력하는 프로그램을 작성하시오.  
>>> 처리조건  
1 신청기한은 정해져 있다.  
2 신청순서대로 3순위까지만 봉사활동이 확정되며 나머지는 대기자가 된다.  
3 확정자 중에 취소가 발생하면 대기자 명단의 1순위를 확정자로 대체한다.  
4 취소는 확정자에서만 발생한다고 가정한다.  

~~~python
comfirm=[]
wait=[]
while True:
  val=input('(신청:1, 취소:2, 종료:3) ==> ')
  if val=='3': break

  phone=input('phone: ')
  if val=='1':
      name=input('name: ')
      if len(comfirm)<3: confirm.append([name, phone])
      else: wait.append([name, phone])
  else:
   for i in range(len(confirm)):
      if confirm[i][1]==phone:
         print('{}님의 신청을 취소하였습니다.'.format(confirm[i][0]))
         del confirm[i]
      confirm.append(wait[0])
      del wait[0]
      print('{}님이 신청되었습니다.'.format(conform[-1][0]))

  print('신청자: ', confirm)
  print('대기자: ', wait)
~~~
