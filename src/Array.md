# 배열 (Array)

## 배열이란?
- "동일한 타입의 데이터"가 여러 개 저장되어 있는 데이터 저장 집합소
- 배열 안에 들어있는 각각의 데이터들은 integer로 되어 있는 index에 의해 접근
- 배열을 사용하면 여러 개의 값을 하나의 이름으로 처리할 수 있음

## 1. 배열의 필요성
- 배열을 사용하면 한번에 여러 개의 값을 저장할 수 있는 공간을 할당 받을 수 있음
- 같은 타입의 데이터를 보다 효율적으로 관리할 수 있음
- 여러 개의 값을 하나의 이름을 공유하여 자료의 조작이 쉬움

### 장점
- 데이터에 접근이 빠름 (인덱스로 접근하므로 상대적인 위치로 용이하게 접근 가능)

### 단점
- 데이터 추가 및 삭제가 어려움
- 미리 최대 길이를 지정해야 하며, 데이터 삭제 시 데이터의 이동을 요구함

---

## 2. JAVA에서의 배열

### 기본 문법
```java
Integer[] intArr = new Integer[5]; // new 키워드를 통해 배열 선언
intArr[0] = 2;
```

### 선언과 동시에 데이터 초기화
```java
Integer int_Arr_1[] = {1, 2, 3, 4, 5};
Integer[] int_Arr_2 = {5, 4, 3, 2, 1};

System.out.println(int_Arr_1[1]);
System.out.println(int_Arr_2[0]);

int_Arr_1[2]; // 자동으로 해당 인덱스의 값에 접근 가능
```

### Arrays 클래스를 활용한 배열 출력
```java
import java.util.Arrays;

System.out.println(Arrays.toString(int_Arr_2)); // 배열 출력
```

---

## ArrayList 사용

```java
ArrayList<Integer> list_1 = new ArrayList<Integer>();
```
- `ArrayList`는 클래스이며, 가변 크기의 배열을 다룰 수 있음

---

## List 사용

```java
List<Integer> list1 = new ArrayList<Integer>();
```
- `List`는 인터페이스이며, 이를 상속받는 클래스는 추상 메서드를 구현해야 함

---

## package import

- 일반적인 패키지는 import를 사용하지 않아도 Jupyter 노트북에서 사용 가능
- import 관련 에러가 발생 시, import 명령 한 번만 실행하면 해결 가능

```java
import java.util.ArrayList;

ArrayList<Integer> listArr = new ArrayList<Integer>();

listArr.add(1); 
listArr.add(2);

// 값 읽기
listArr.get(1);

// 값 변경
listArr.set(0, 8);

// 값 삭제
listArr.remove(0);

// 배열 길이 확인
listArr.size();
```

---

## 2차원 배열 출력

```java
Integer data_Arr[][] = { {1, 2, 3}, {4, 5, 6} };

System.out.println(data_Arr[0][2]); // 3 출력
System.out.println(data_Arr[1][2]); // 6 출력
```

---

## 3차원 배열 출력

```java
Integer[][][] data_Arr = {
    {
        {1, 2, 3},
        {4, 5, 6}
    },
    {
        {7, 8, 9},
        {10, 11, 12}
    }
};

System.out.println(data_Arr[0][1][2]); // 6 출력
System.out.println(data_Arr[1][1][2]); // 12 출력
```

---

## 연습해보기: 배열 초기화 및 출력

```java
int[] a = {1, 2, 3, 4, 5}; // 배열 초기화

for (int i = 0; i < a.length; i++) {
    System.out.println("a[" + i + "] = " + a[i]);
}
```