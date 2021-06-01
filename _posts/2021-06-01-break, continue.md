---
layout: single
title: "break, continue"
---

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
