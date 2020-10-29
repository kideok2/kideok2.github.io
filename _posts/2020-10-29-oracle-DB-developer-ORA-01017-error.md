---
title: "oracle DB developer - ORA-01017 error clear"
date: 2020-10-29
categories: oracle DB ORA-01017error
---
![error_ora-01017](https://user-images.githubusercontent.com/31603702/97537406-1cc71d00-1a02-11eb-8761-45d7e08d06d9.jpg)

## ORA-01017 에러 원인

- oracle developer에서만 계정 만들기를 하고 있어서 안되는 거였음..
- cmd창에 들어가서 만들어 줘야됨 ㅎㅎ

## ORA-01017 에러 해결방법


![sqlplus](https://user-images.githubusercontent.com/31603702/97536396-6a428a80-1a00-11eb-8fdd-684ce4876aff.jpg)

**sqlplus "/as sysdba"** 입력 후 엔터 -접속하기

![sqlplus2](https://user-images.githubusercontent.com/31603702/97537011-6f540980-1a01-11eb-9804-b3de6d0495b1.jpg)

**create user c##아이디 identified by 비밀번호** 입력 후 엔터 - 아이디와 비밀번호 생성 (_c## 꼭 넣어줘야됨_)

![sqlplus3](https://user-images.githubusercontent.com/31603702/97537222-cce85600-1a01-11eb-8813-48814e1c3462.jpg)

**grant connect, resource, dba to c##아이디** 입력 후 엔터 - 권한을 부여해준다



### 그 외에 아이디 앞에 c## 안붙이고 싶으면

**alter session set "_ORACLE_SCRIPT"=true;** 입력후 엔터<br>세션의 권한을 부여해줌(_c##안 붙이고 싶으면 위에꺼 입력하기 전에 먼저 입력해 줘야한다_)

---

### TMI 메모
계속 헤매다가 c## 붙여서 아이디 만들고 권한도 부여했는데 막상 developer에서 로그인 할 때는 오류...크흠 developer에도 c## 붙여서 로그인해보니 된다.(오류인지 당연히 붙여야 되는건지 모르겠는데) <br> 처음부터 **alter session set "_ORACLE_SCRIPT"=true;** 라는 세션을 입력해주고 아이디 생성하는게 좋을 듯 싶다
