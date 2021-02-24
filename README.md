# Free Food(음식 추천 앱)
## 제작 인원, 기간
* 1인
* 20.05 ~ 20.07

## 앱 제작 배경
>평소 가족들이나, 친구들과 무엇을 먹을 지 고민할 때가 많다. 
그럴 때 마다, 모두 공통으로 ‘아무거나’ 또는 ‘너가 정해’라고 말을 하는 경우가 많다. 
메뉴 선택권을 맡게 된 사람은 부담감과 책임감을 느끼게 된다. 
나는 이러한 상황으로부터 유연해질 수 있는 앱을 개발하기로 했다.
이는 혼자 밥을 먹을 때도 쓸 수 있고, 메뉴를 정해야 되는 상황이라면 어디서든 간편하고 재미있게 쓸 수 있다.

## 실행 동영상
[유튜브 영상](https://www.youtube.com/watch?v=t7PjBRBnIOU)


## 시스템 동작
### 1. 메인 화면
 <img width="320" height = "500" alt="PK 메인화면" src="https://user-images.githubusercontent.com/78644129/108962960-d5555280-76bc-11eb-9009-91d330cb83a3.jpg"><br/>
### 2. 항목 선택 페이지
<img width="320" height = "500" alt="PK 메인화면" src="https://user-images.githubusercontent.com/78644129/108964379-bf489180-76be-11eb-892c-7ebda328c4c8.jpg"><br/>
### 2-1. 종류에 따라 선택
<img width="320" height = "500" alt="PK 메인화면" src="https://user-images.githubusercontent.com/78644129/108963259-39781680-76bd-11eb-81a3-5f4d5c6f942f.jpg"><br/>
#### 2-1-1. 음식 추천 기본 페이지
<img width="320" height = "500" alt="PK 메인화면" src="https://user-images.githubusercontent.com/78644129/108964483-dd15f680-76be-11eb-9f21-1d44a4a9a475.jpg"><br/>
#### 2-1-2. 랜덤 음식 추천 페이지
<img width="320" height = "500" alt="PK 메인화면" src="https://user-images.githubusercontent.com/78644129/108964595-00d93c80-76bf-11eb-974e-f8481bb157c2.jpg"><br/>
### 2-2. 상황에 따라 선택
<img width="320" height = "500" alt="PK 메인화면" src="https://user-images.githubusercontent.com/78644129/108964677-20706500-76bf-11eb-993a-2d0aa73371e0.jpg"><br/>
#### 2-2-1.'다이어트' 페이지는 음식 추천과 레시피 제공
<img width="320" height = "500" alt="PK 메인화면" src="https://user-images.githubusercontent.com/78644129/108964727-32ea9e80-76bf-11eb-8397-969ebcc4274d.jpg">
<img width="320" height = "500" alt="PK 메인화면" src="https://user-images.githubusercontent.com/78644129/108964793-4bf34f80-76bf-11eb-897d-423e5934e7ea.jpg"><br/>
* 나머지 항목 기능은 2-1-2과 동일


## 주요 기능
1. intent를 이용한 페이지 전환
```
Intent intent = new Intent(MainActivity.this, Menus.class);
startActivity(intent);
```
2. ImageView에 음식 이미지 출력
```
<ImageView
        android:id="@+id/imageView"
        android:layout_width="match_parent 
        android:layout_height="168dp"
        app:srcCompat="@drawable/btn_random" />
```
3. Random() 메소드를 이용한 음식 랜덤 추첨
```
  int count = random.nextInt(4)+1;
```  
4. Switch를 이용하여 반복적으로 음식 랜덤 추첨
```
switch(count){
                    case 1 :
                        imageView.setImageResource(R.drawable.k_pic1);
                        txtResult.setText("김치찌개");
                        break;
                    case 2 :
                        imageView.setImageResource(R.drawable.k_pic2);
                        txtResult.setText("된장찌개");
                        break;
                    case 3 :
                        imageView.setImageResource(R.drawable.k_pic3);
                        txtResult.setText("부대찌개");
                        break;
                    case 4 :
                        imageView.setImageResource(R.drawable.k_pic4);
                        txtResult.setText("감자탕");
                        break;
                }
```                

## 개선점
* 음식 종류가 더 다양했으면 선택의 폭이 넓어져 좋았을 것..!
* 디자인이 너무 심플해 보이는 문제... 디자인에도 신경쓰기!
