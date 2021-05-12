# InflationStudy
> inflation 공부를 위한 쉬운 예제      
> 참고 : https://rina214.tistory.com/22       
> 위 블로그 예제를 따라해보며 공부함

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
