##React 에서 자주 보이던 에러 정리

1. react 에러: React.jsx: type is invalid -- expected a string (for built-in components) or a class/function (for composite components) but got: object
-> axios나 fetch등 call요청하는곳에 이동하려는 곳 이름앞에 /를 붙혀야함         


2. Cannot read properties of undefined (reading '무엇')
-> '무엇'에 대해 정보가 들어오는게 없거나 정의되지않음
   
3.react-dom.development.js:86 Warning: validateDOMNesting(...): <tr> cannot appear as a child of <table>. Add a <tbody>, <thead> or <tfoot> to your code to match the DOM tree generated by the browser.
-> tr태그는 thead나 tbody태그로 둘러주어야 한다. 

4.history.ts:494 Uncaught Error: You cannot render a <Router> inside another <Router>. You should never have more than one in your app.
-> Router태그안에 또 다른 Router를 두면 안된다. 

5.Parsing error: JSX attributes must only be assigned a non-empty expression.
-> React안에 return으로 표현한 JSX에서는 빈 표현식을 사용하면 안되서 채워넣거나 없애야함

6. TypeError: destroy is not a function (it is Object)
-> useEffect 안에서 생긴 문제, 사용법 맞게 잘 작성했는지 확인해야함.

7. buildLink is not function
-> 사용하려는 컴포넌트나 기능중이 install 되지않은 항목이 있을 수 있다.

8. Error: Element type is invalid: expected a string (for built-in components) or a class/function (for composite components) but got: undefined.
-> import나 export를 잘못 실행 하고 있는것.
-> 확인해보니 Input과 Button을 따로 만들어준 컴포넌트를 사용해야 하는데
   자동완성으로 'react-native' 쪽에서 임포트를 해놓았다.
