# MarkDown 작성법 공부!
## 1.MarkDown이란 무엇인가
MarkDown은 텍스트 기반 웹상에서 글을 쓰는 모든 사람들을 위한 글쓰기 도구(서식, 포맷, 양식) 입니다.   
GitHub를 통해 각광받기 시작했고 MD을 통해 소스설명, 프로젝트단계별 정리 등을 간단하고 빠르게 할 수 있다   
## 2.MarkDown 문법
### 2.1 줄바꿈
문장 끝에 3칸이상 띄어쓰기를 하면 줄이 바뀐다 "   "   
~~~
문장을 마치고.
띄어쓰기 없이 그냥 쓴다면 개행이 되지않고(   )   
뒤에 띄어쓰기를 3칸이상 해주면 개행되는것을 볼수있다.
~~~
문장을 마치고.
띄어쓰기 없이 그냥 쓴다면 개행이 되지않고(   )   
뒤에 띄어쓰기를 3칸이상 해주면 개행되는것을 볼수있다.   
### 2.2 Header(헤더)
~~~
# 헤더 h1
## 헤더 h2
### 헤더 h3
#### 헤더 h4
##### 헤더 h5
###### 헤더 h6
~~~
# 헤더 h1
## 헤더 h2
### 헤더 h3
#### 헤더 h4
##### 헤더 h5
###### 헤더 h6
1~6 까지 지원한다.   
### 2.3 Code Block(코드 블럭)
<code>```</code> 혹은 <code>~~~</code>   
~~~
<code> 쓸내용 <code>
~~~
를 사용해서 나타낼수 있다.   
~~~
처음~~~옆에 타입을 지정해줄수도 있다.
java, c, javascript 등
ex)  ~~~java
        void func(){
            printf("print code");
        }
     ~~~ 
~~~
### 2.4 Link(링크)
- 인라인 링크   
~~~
[Github](github.com,"git")
~~~
[Github](github.com,"git")   
- URL링크   
~~~
<http://google.com/>
~~~
<http://google.com/>   
### 2.5 List(리스트)
<code>*</code>,<code>+</code>,<code>-</code>로 시작.  
~~~
- list1
+ list2
* list3
~~~
- list1
+ list2
* list3
### 2.6 Emphasis(강조)
굵게 쓰기(bold) : <code>**</code> 또는 <code>__</code>로 감싼 텍스트
기울여 쓰기(italic) : <code>*</code> 또는 <code>_</code>로 감싼 텍스트
~~~
**굵게 강조하여 쓰기1** __굵게 강조하여 쓰기2__   
*기울여 쓰기1* _기울여 쓰기2_   
~~~
**굵게 강조하여 쓰기1**     __굵게 강조하여 쓰기2__   
*기울여 쓰기1*   _기울여 쓰기2_    
### 2.7 image(이미지)
~~~
format
![image title](/path/imagename.jpg or png,gif... "Optional title")
ex)
![ZootopiaImage](zootopia.jpg "Zootopia Optonal title")
~~~
![ZootopiaImage](zootopia.jpg "Zootopia Optonal title")   
사이즈 조절은 html태그 <code><img></img></code>를 이용한다.   
~~~
<img src="zootopia.jpg" width="500px" height="300px" title="set width height px" alt="zootopia"></img><br/>
<img src="zootopia.jpg" width="30%" height="30%" title="set width height %" alt="zootopia"></img>
~~~
<img src="zootopia.jpg" width="500px" height="300px" title="set width height px" alt="zootopia"></img><br/>
<img src="zootopia.jpg" width="30%" height="30%" title="set width height %" alt="zootopia"></img>   
testmassage   
