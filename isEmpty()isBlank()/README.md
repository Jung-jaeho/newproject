# 6. StringUtils.isBlank와 StringUtils.isEmpty  

isBlank와 isEmpty의 차이점은 아래 예제와 같이 공백(whitespace) 처리입니다. isBlank의 경우 공백을 blank 즉, 비어있는 값으로 처리하며 isEmpty의 경우 공백을 비어있지 않다고(isEmpty가 false) 리턴합니다.

`String.Utils.isBlank` 공백을 빈값으로 처리

~~~~
StringUtils.isBlank(null)      = true
 StringUtils.isBlank("")        = true
 StringUtils.isBlank(" ")       = true
 StringUtils.isBlank("bob")     = false
 StringUtils.isBlank("  bob  ") = false
~~~~


`StringUtils.isEmpty` 공백을 비어있지 않다고 처리
~~~
 StringUtils.isEmpty(null)      = true
 StringUtils.isEmpty("")        = true
 StringUtils.isEmpty(" ")       = false
 StringUtils.isEmpty("bob")     = false
 StringUtils.isEmpty("  bob  ") = false
~~~

문자열이  빈 값("") 일 경우 true를 반환합니다.
하지만 whitespace("  ")의 처리에서는 다릅니다.
isEmpty()는 false를, isBlank()는 true를 반환합니다.

<br>
<br>
<br>
<br>