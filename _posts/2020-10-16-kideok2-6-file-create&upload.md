---
title: "파일 생성 및 깃허브에 업로드 하는 방법"
categories: git_
---

# Chapter 1. 실행

1. Typora에서 실행 하고 내가 원하는 내용을 채운다
2. 내용을 다 채웠으면 ctrl + s로 저장을 한다. <sup>[1](#foot_note1)</sup>
3. 저장 되었는지 확인

# Chapter 2. commit 생성

1. 우선 git status로 새로 만들어진 것이 있나 파일을 확인한다. <sup>[2](#foot_note2)</sup>
2. git add 로 파일 경로와 파일 이름을 쓴다.<sup>[3](#foot_note3)</sup>
```
	git add _posts/2020-10-16-git-upload.md
```

4. 파일 전체를 add 하려면  git add . 으로 표현가능
4. git commit -m 수정, 추가 내용<sup>[4](#foot_note4)</sup>

# Chapter 3. 깃허브에 파일 업로드

1. 추가적으로 git push 해주면 끝 
2. 깃허브 들어가서 확인해보기

----
[1](#foot_note1) : 단, 한글 이름으로 저장 시 파일 내용이 깨질 수 있음<br>
[2](#foot_note2) : 중간 중간에도 확인가능<br>
[3](#foot_note3) : 내 파일을 예. git add  _posts/파일 이름<br> 
[4](#foot_note4) : m은 메세지를 뜻함 
