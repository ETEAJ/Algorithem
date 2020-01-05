## K번째수

#### 설명

array의 i번째 숫자부터 j번째 숫자까지 자르고 정렬했을 때 k번째에 있는 수를 구하려고 합니다.

array가 [1, 5, 2, 6, 3, 7, 4], i = 2, j = 5, k = 3 이면,

1. array의 2번째부터 5번째까지 자르면 [5, 2, 6, 3] 입니다.
2. 1에서 나온 배열을 정렬하면 [2, 3, 5, 6] 입니다.
3. 2에서 나온 배열의 3번째 숫자는 5 입니다.

###### 제한사항

- array의 길이는 1 이상 100 이하입니다.
- array의 각 원소는 1 이상 100 이하입니다.
- commands의 길이는 1 이상 50 이하입니다.
- commands의 각 원소는 길이가 3입니다.

#### 코드

###### javascript

```javascript
function solution(array, commands) {
    let answer = [];
    for(let i=0; i<commands.length; i++) {
        let arr = commands[i];
        answer.push(array.slice(arr[0]-1, arr[1]).sort((a, b) => {return a-b})[arr[2]-1]);
    }
    return answer;
}
```

* JavaScript는 sort 함수를 이용해서 했습니다.

###### java

```java
a
```

* JavaScript와 다르게 Java는 for문으로 정렬을 했습니다.