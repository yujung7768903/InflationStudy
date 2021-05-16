# InflationStudy
> inflation 공부를 위한 쉬운 예제      
> 참고 : https://rina214.tistory.com/22    
> 참고 : https://zion830.tistory.com/16
> 참고 : https://www.crocus.co.kr/1584
> 위 블로그 예제를 따라해보며 공부함

### Inflation
xml 파일과 java 코드를 연결하는 과정을 인플레이션이라고 한다.      
xml은 레이아웃을 정의한 파일인데 정의하고 끝이 아니라, 자바 코드에서 setContentView()와 같은 메소드를 이용하여 xml 파일 내용을 객체화해줘야 참조할 수 있다.

### 부분 화면 - LayoutInflater
setContetnView() 메소드를 사용하면 화면 전체에 레이아웃이 띄워지기 때문에, 부분적으로 다른 xml내용을 추가하고 싶을 때는 LayoutInflater라는 클래스를 이용한다.         
이 클래스는 xml에 정의된 resource를 View 객체로 반환해준다.

### 동작 화면
<img width="474" alt="inflater study 동작 화면" src="https://user-images.githubusercontent.com/68562176/117848435-45d43e80-b2be-11eb-93e2-5cce290c7d9d.png">

### 주요 코드
**main_item.xml**을 activity_main.xml의 **content**라는 아이디를 가진 LinearLayout에 **추가**
```
inflaterBtn = (Button) findViewById(R.id.button);
content = (LinearLayout) findViewById(R.id.content);

inflaterBtn.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        LayoutInflater layoutInflater = (LayoutInflater) getSystemService(getApplicationContext().LAYOUT_INFLATER_SERVICE);
        layoutInflater.inflate(R.layout.main_item, content, true);
    }
});
```
