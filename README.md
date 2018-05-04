# Ch.5(2018.04.30)
## Index
1. Thymeleaf
2. etc
3. 시험회고
## 1.Thymeleaf

Thymeleaf: java 라이브러리로 xml, xhtml, html5 문서를 생성하는 템플릿 엔진(광파는 애)
1. Spring Starter Project 생성
* 프로잭트 생성
![프로젝트](/image/1.png){: width="150" height="150"}

* 라이브러리 추가

![라이브러리](/image/2.png){: width="150" height="150"}

* 컨트롤러 생성 및 작성

![컨트롤러](/image/3.png){: width="150" height="150"}

* 코드 작성
~~~
package com.youngjin.controller;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class SampleController {
	@GetMapping("/sample1")
	public void sample1(Model model) {
		
		model.addAttribute("greeting","Hello world");
	}

}

~~~

* templates 내에 sample1.html 생성

![html](/image/4.png){: width="150" height="150"}

* sample1.html 작성
~~~
<html xmlns:th="http:..www.thymeleaf.org">
<head>
<title>Thymeleaf3</title>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
</head>
<body>
	<h1>Thymeleaf Test Page</h1>
</body>
</html>
~~~

* 프로젝트 실행확인

~~~
boot5 -> Run as ->localhost:8080/sample1
~~~

![html](/image/5.png){: width="150" height="150"}




#### 2.etc
~~~
Java script가 왜 맨밑에 내려가나?
1. 상향 호이스팅을 한다.
2. 속도가 30%정도 빨라진다.
3. 표준은 아니다.
~~~
##### 3.시험회고
~~~
-거의 모든 시험이 2차 면접 손코딩
-대소문자/들여쓰기 등의 Convention을 지켜라
-C클래스 구간 친구들 걸러내기
-배점위주로 풀어야한다
-Logic위주로 푼다
~~~