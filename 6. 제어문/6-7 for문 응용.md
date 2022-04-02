## for문 응용

해당 파트는 이 [영상](https://www.youtube.com/embed/qC4x-nTCZxg?list=PLGPF8gvWLYypeEoFNTfSHdFL5WRLAfmmm)을 시청 후 교안을 정독해주세요.

* 이중 for문
	for문 안에는 또 다른 for문을 넣어 반복시켜줄 수 있습니다. 아래 코드를 실행하면 어떤 결과가 나올지 생각해본 뒤, 코드를 쳐서 출력 결과를 확인해보세요. 
	```python
	for a in  range(1,  10):
		for b in  range(1,  10):
			print('%d * %d = %d'%(a, b, a * b))
		print('===%d단 끝!==='%(a))
	print('구구단 1단 부터 9단까지 끝!')
	```
	결과를 확인해보셨나요? 이 코드는 구구단 1단 부터 9단까지를 출력하는 코드였습니다. 아래 이미지는 어떤 순서로 중첩된 2개의 for문이 실행되는지 설명하고 있습니다. 
  
	![이중for문](/python/5-3/doubled-for.png)
	
* 리스트 안에 for문 포함하기     
	기존에 for문은 ':'기호 뒤에 엔터+들여쓰기 형식을 꼭 지켜야 한다고 했는데요, 사실 가독성은 떨어지지만 한 줄로 for문을 간단하게 작성하는 방법도 있습니다. 이는 	새로운 리스트에 데이터를 채워주는 코드를 작성할 때 자주 사용됩니다.
	```python
	# 기존 방법
	new_list=[] # 빈 리스트 만들어주기
	
	for i in range(1,6):
		new_list.append(i * 10)
	```
	```python
	# 간단한 방법
	new_list=[i*10 for i in range(1,6)]
	```

* for문의 break, continue     
	break와 continue는 앞서 배운 while에서와 동일한 역할을 합니다. (: 뒤에 바로 써 줄 수도 있고 엔터 + 들여쓰기 형식에 맞춰 사용할 수도 있습니다.)
	* break: for문 반복을 강제 종료
	* continue: for문 실행중 처음으로 돌아가기
	```python
	# break 예시
	for i in  range(1,5):
		if i > 3:
			break
		print(i)
	```
	```python
	# continue 예시
	for i in  range(1,5):
		if i > 3: continue
		print(i)
	```
	
*  for문의 else    
	if문에서 사용되는 else가 for문에서 사용되기도 합니다. for와 함께 쓰는 else는, for문이 중간에 break 등으로 끊기지 않고 끝까지 정상적으로 실행 되었을 때 수행됩니다. 
	```python
	a = 100
	for i in range(0,10):
		print(i)
		if i == a: break
	else:
		print('for complete')
	print('done')	
	```
	위 코드를 한 줄씩 해석해보면 다음과 같습니다. 
  
  1. 변수 a는 100이다.    
  2. 0부터9까지 범위에서 변수 i를 출력해라.    
  3. 만약 변수 i가 처음에 선언한 변수 a와 같다면 반복문을 멈춰라.
  4. 반복문이 멈추지 않고 적용한 조건에 맞게 모두 실행했다면 'for complete' 를 출력해라.     
  5. for 반복문이 모두 끝나면 'done'을 출력해라.   

> ✔️동일하게 '반복'이 포인트인 for와 while, 차이가 뭔가요? 
> * for
>   * 지정된 횟수, 지정된 데이터 수 만큼의 반복.
>   * 변수를 지정
>   
> * while
>   * 조건이 만족될 때(거짓이 될때까지)까지 반복. 
>   * 조건이 만족되지 않는다면 무한으로 실행됨.
> 
> 이렇게 봐도 둘의 차이가 잘 이해되지 않으시나요? 괜찮습니다. 파이썬에는 비슷한 역할을 하지만 다르게 표현하는 문법들이 많습니다. 사용자는 상황에 따라서 더 적합한, 더 익숙한 코드를 작성하면 된답니다! 

