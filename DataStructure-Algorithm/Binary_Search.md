# Binary Search(이진 탐색)

***

> 1 ~ n 개의 원소를 가진 리스트에서 특정 원소를 찾는것을 **Search** 라고 하며,
**Simple Search** (단순 탐색. 일일이 순서대로 모두 추측..)의 경우 운이 좋다면 빠른 시간 안에 검색이 끝날 수 도 있지만 그 반대. 최악의 경우 최대 n번의...모든 원소를 살펴봐야하므로 비효율적이다.
원소가 많아질수록 반복이 많아져 시간이 더욱 오래걸린다.

* 더 좋은 탐색 방법은 n의 중간, 예를 들면 1 ~ 1000일 경우 500 부터 시작하는 것이다.
500이 너무 "작다" 또는 "크다" 이 대답 하나로 다른 절반은 답이 아니라는 것을 알 수 있다.
그 다음으로 나머지 반 숫자들 중 중간에 속하는 숫자로 추측을 한다.
최대 $log_2$ $n$ 번 만에 답을 찾을 수 있다.
<br>
* 하지만 리스트의 원소들이 정렬되어있을 경우에만 사용할 수 있다.
**ex)** 전화번호부에 있는 이름
<br>
* 하지만 만약 이름이 순서대로 정렬되어있지 않다면?
이럴 때 어떻게 해야할지 파이썬을 이용해 알아본다.
다음 예제 코드에서는 **Array**(배열)를 사용한다.

```
# Python3

def binary_search(list, item):

    # 배열 전체길이 설정

    low = 0
    high = len(list) - 1

    # 가운데 있는 원소를 확인

    while low <= high:
        mid = (low + high) // 2
        guess = list[mid]

        # 아이템을 찾음

        if guess == item:
            return mid

        # 추측한 숫자가 너무큼

        if guess > item:
            high = mid - 1

        # 추측한 숫자가 너무작음

        else:
            low = mid + 1

    # 아이템이 리스트에 없음
    return None

# 확인할 리스트

my_list = [1, 3, 5, 7, 9]

print (binary_search(my_list, 3)) # => 1
print (binary_search(my_list, -1)) # => None

```

* 실행결과
```
1
None
```

***

* 위 코드를 자바로 컨버팅해보자.(사실은 컨버팅이 큰 목적이다!!)

```
public class BinarySearch {
    private static Integer binarySearch(int[] list, int item) {
        int low = 0;
        int high = list.length - 1;

        while (low <= high) {
            int mid = (low + high) / 2;
            int guess = list[mid];
            if (guess == item) {
                return mid;
            }
            if (guess > item) {
                high = mid - 1;
            } else {
                low = mid + 1;
            }
        }

        return null;
    }

    public static void main(String[] args) {
        int[] myList = {1, 3, 5, 7, 9};
        System.out.println(binarySearch(myList, 3));
        System.out.println(binarySearch(myList, -1));
    }
}
```

* 미리 일러둔 대로 코틀린으로도 컨버팅 해본다.(IDE가 다 했다.)
Java 코드를 https://try.kotlinlang.org 에서 Kotlin으로 컨버팅 한 코드와도 비슷하고
무엇보다 둘 다 코드가 이상하다. ㅋㅋ그래서 약간 고쳐 실행되게 만들었다.

```
private fun binarySearch(list: IntArray, item: Int): Int? {
    var low = 0
    var high = list.size - 1

    while (low <= high) {
        val mid = (low + high) / 2
        val guess = list[mid]
        if (guess == item) {
            return mid
        }
        if (guess > item) {
            high = mid - 1
        } else {
            low = mid + 1
        }
    }

    return null
}

fun main(args: Array<String>) {
    val myList = intArrayOf(1, 3, 5, 7, 9)
    println(binarySearch(myList, 3))
    println(binarySearch(myList, -1))
}
```

* Dart로도 컨버팅해보자

```

```
