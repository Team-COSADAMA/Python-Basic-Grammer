## for문이란?


해당 파트는 이 [영상](https://www.youtube.com/embed/PNnZ9YXbF14?list=PLGPF8gvWLYypeEoFNTfSHdFL5WRLAfmmm)을 시청 후 교안을 정독해주세요.    


for문은 '지정한 횟수만큼 혹은 리스트, 튜플, 문자열의 개수만큼 반복하는 제어문' 입니다. for문의 기본 구조는 다음과 같습니다. 
```python
for 변수 in 지정횟수or리스트or튜플or문자열:
	반복 실행할 명령문 
```
이때 변수는 for문 내부에서만 선언되는 변수로, for문이 끝나면 다시 사용할 수 없습니다. 또한 if문, while문과 같이 `:`기호를 사용한 뒤에는 **엔터 + 들여쓰기**의 형식을 맞춰줘야 합니다. (가독성을 위해!)

> 변수 이름은 사용자가 임의로 설정해주면 됩니다. 편의를 위해 a, z, i 등과 같은 알파벳을 사용하기도 하고, 쉽게 이해할 수 있도록 데이터의 특징을 살린 변수명을 사용하기도 합니다.

다음은 반복할 횟수를 지정해주는 방법(지정횟수, 리스트, 튜플, 문자열)에 예시를 하나씩 살펴보겠습니다.  
```python
# 지정횟수(range)
for num in range(1,5):
	print(num)
```
`range`는 범위안의 정수를 만들어주는데, 주로 for문에서 반복 횟수를 지정해줄 때 사용합니다. range의 기본 형태는 `range(start, end, step)`입니다. 
* start: 시작 위치. 시작점을 지정하지 않으면 0부터 시작함.
* end: 마지막 위치. **end는 포함하지 않음!**
* step: 몇개씩 끊어서 가져올지. 옵션이기 때문에 생략할 수 있음.

즉, range(1,5) 이라면 1~4까지의 정수를 만들어주는 것입니다. 
아래 예시 코드들을 따라서 쳐보고 출력 결과를 확인해보세요. 
```python
# 리스트
fruits = ['apple', 'banana', 'orange']

for fruit in fruits:
	print(fruit)
```

```python
# 튜플
fruits  = ("apple",  "banana",  "orange")

for fruit in fruits:
	print(fruit)
```

```python
# 문자열
ex = "파이썬 공부는 재밌다!"

for i in ex:
	print(i)
```
