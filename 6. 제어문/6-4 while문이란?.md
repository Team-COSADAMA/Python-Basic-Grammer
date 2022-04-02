while문이란?

> 해당 파트는 아래 영상들을 시청 후 교안을 정독해주세요. 

1. [while 문](https://www.youtube.com/embed/B2cGQW_Hyik?list=PLGPF8gvWLYypeEoFNTfSHdFL5WRLAfmmm)

2. [continue](https://www.youtube.com/embed/MGBvRQLtpGQ?list=PLGPF8gvWLYypeEoFNTfSHdFL5WRLAfmmm 
3. [break](https://www.youtube.com/embed/uBsd0t_4Pzs?list=PLGPF8gvWLYypeEoFNTfSHdFL5WRLAfmmm)


while문은 '조건이 만족되는 한 계속 반복하여 실행하는 제어문'입니다. 이때의 포인트는 '반복'인데, 아래 예시를 보면서 이해해보겠습니다. 
```python
num = 1
while num <= 10:
	print('The number is %d' % num)
	num += 1
```
위 코드를 한줄씩 해석해보면 다음과 같습니다. 
1. 변수 num은 1이다. 
2. 변수 num 이 10 이하인 동안 반복하여 (참이 끝날 때 까지)
3. 'The number is %d'를 출력해라. (%d에는 변수 num이 들어감)
4. 변수 num에 num+1을 할당해라. 

즉, num에 1씩 더한값을 할당하여 변수를 만들고, `num <= 10`이라는 조건이 참(True)인 동안은 끊임없이 print문을 출력하고, num이 10이 되면 while 반복문을 끝낸다는 의미입니다.
```python
# 실행결과
The number is 1
The number is 2
The number is 3
The number is 4 
The number is 5 
The number is 6 
The number is 7 
The number is 8 
The number is 9 
The number is 10
```

__`continue`__ 는 while문을 빠져나가지 않고 while문의 맨 처음 조건문으로 다시 돌아가게 만듭니다. 혹은 중간에서 건너뛴다고 이해할 수도 있습니다.

```python
num = 0

while num < 10:
	num += 1
	if num % 2 == 1:
		continue
	print(num)
```
위 코드는 1 부터 10까지 숫자 중에서 짝수만 출력하도록 하는 코드입니다. 한 줄씩 의미를 해석해보면 다음과 같습니다. 
1. 변수 num 은 1이다.
2. 변수 num 이 10 미만인 동안 반복하여
3. 변수 num에 1씩 더하여 할당하여 새로운 num을 정의하고
4. 만약 변수 num을 2로 나눴을 때 나머지가 1이라면 (홀수라면)
5. 아래 코드를 실행하지 않고 (건너뛰고) 처음 while 조건문으로 돌아간다.
6. 만약 변수 num을 2로 나눴을 때 나머지가 1이 아니라면(짝수라면) 변수 num을 출력한다. 

`continue`를 사용했기 때문에 if문에서는 else혹은 elif를 사용하여 `num % 2 =! 1`인 조건을 만들어 줄 필요가 없고 while문 안에 있으므로 if문이 참이 아니라도 while문은 멈추지 않습니다. 출력 결과는 `2, 4, 6, 8, 10`입니다. 

하지만 `continue`를 사용한다고 해도 `continue`아래 코드를 건너뛸 뿐, 반복은 계속됩니다. 즉, while문은 조건이 참(True)이 지속된다면 무한으로 반복하여 실행하는 것이죠. 따라서 반드시 중간에 탈출하는 코드, 즉 조건이 거짓(False)가 되도록 만들어주어야 무한으로 반복되는 while문을 멈출 수 있습니다. 위 예시에서도 `num <= 10`, 즉 '10보다 작을 때 까지만'이라는 조건을 주었기 때문에 반복을 멈출 수 있었습니다.

또한 while문은 강제로 멈추게 하는 __`break`__ 를 사용하여 빠져나오는 방법도 있습니다. 다음 예시를 보면서 `break`의 역할을 이해해보세요. 
```python
num = 0

while num < 10:
	num += 1
	if num % 2 == 0:
		print(num)
		break
```
코드를 출력하면 어떤 값이 출력될까요? 네, 바로 `2`만 출력되고 while문은 멈춥니다. '변수를 2로 나눴을 때 나머지가 1이 된다면 변수를 출력하고 break!' 라는 조건에 맞게, 1부터 10까지의 숫자 중 첫 번째 짝수인 2가 출력되자마자 while문은 반복을 멈추는 것이지요. 
