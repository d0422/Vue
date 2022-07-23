# Vue

⇒ 리액트랑 비슷한 SPA(Single Page Application)을 만들수 있게 하는 프레임워크

리액트가 js에 가깝다면 Vue는 html에 가깝다.

# 데이터 바인딩

리액트와 유사하나 조금 다르다.

```jsx
<script>
export default{
	name:'App',
	data(){
		return{
			변수 : "내용",
			메뉴들 : ["Home", "Shop", "About"],
		}
	},
	components: {
	}
}
</script>
```

이렇게 변수를 선언하고 페이지에서는 이렇게 사용한다.

```html
<div>{{변수}}</div>
```

# 반복문

react의 map과 유사하나 html에 가깝게 사용한다.

```html
<div class="menu">
	<a v-for="메뉴목록 in 메뉴들":key ="메뉴목록">{{메뉴목록}}</a>
</div>
```

:key 가없으면 오류가 발생한다. map의 key와 동일한 개념