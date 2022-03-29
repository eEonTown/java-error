>java.lang.StackOverflowError

재귀 횟수가 너무 많아서 발생하는 경우

```
//에러를 발생시킨 코드
public static int factorial(int number) {
    return number * factorial(number-1);
}

public static void main(String[] args) {
    System.out.println(factorial(3));
}
```

```
//수정
/*
number-1로 인해 음수까지 내려가 재귀 횟수가 많아져 오류가 발생한 것 같아서
if문으로 number가 1이 되었을 때 1을 return하면서 메소드를 종료 시켜 해결 했습니다.
*/
public static int factorial(int number) {
    if(number == 1) {
        return 1; //
    } else {
        return number * factorial(number-1);
    }
}

public static void main(String[] args) {
    System.out.println(factorial(3));
}
```
