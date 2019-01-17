#Python 기초 

##### 특징

- 인터프리터 기반 객체지향 언어
- 플랫폼에 구애받지 않음
- 확장성이 뛰어남



##### Number

```python
print(5 + 5)

print(5 - 2)

print(3 ** 2)	#제곱

print(8 / 2)	#float 형

print(8 // 2)	#int 형
```

#####String

```python
test = "Hello World!"
print(test)  # Hello World!

test = 'Hello!'
print(test)  # Hello!

test = 'I don\'t need Coke!'
print(test)  # I don't need Coke!

test = "I don't need Coke!"
print(test)  # I don't need Coke!
```

#####'r'은 raw라는 의미로 아무 의미없는 문자열을 뜻함

```python
test = r'C:\Users'
print(test)  # C:\Users
```

##### 조건문

```python
name = 'python'

if name is 'python':
    print('Hello python')
elif name is 'moonch':
    print('Hello moonch!')
else:
    print('Hello Everyone!')
```

**List 내장 함수들!**

```
test = [1, 2]
test.append(3)  # 맨 뒤에 값 추가
print(test)  # [1, 2, 3]
```

append(x) 함수는 인자를 1개밖에 받지 않기 때문에 여러개의 인자를 넘겨줄 경우 에러가 납니다.

```
test = [3, 1, 2, 5, 4]
test.sort()
print(test)  # [1, 2, 3, 4, 5]

test.sort(reverse=True)
print(test)  # [5, 4, 3, 2, 1]
```

sort() 함수는 List를 자동으로 정렬해줍니다. 역순으로 정렬하기 위해서는 sort 함수에 reverse 옵션을 True로 설정해주면 됩니다.

```
test = [3, 1, 2]
test.reverse()
print(test)  # [2, 1, 3]
```

reverse() 함수는 현재의 List를 역순으로 뒤집어 줍니다. 정렬은 하지 않고 현재의 List를 역순으로 뒤집어 줍니다.

```
test = [1, 2, 3, 4, 5]
print(test.index(3))  # 2
print(test.index(5))  # 4
```

index(x) 함수는 x 라는 값이 있는 경우 , x 의 인덱스를 반환해주는 함수입니다.

```
test = [1, 2, 3, 4, 5]
test.insert(0, 6)
print(test)  # [6, 1, 2, 3, 4, 5]
```



##### Dictionaty 자료형

Dictionary는 키=값 형태로 이루어진 자료형입니다. 이렇게 대응 관계를 나타내는 자료형을 연관 배열 혹은 Hash라고 합니다. 대표적인 예로는 루비의 Hash와 C#의 Dictionary가 있습니다.

이제 Dictionary라는 것은 어떻게 생겼는지 알아보도록 하겠습니다.

```
dic1 = dict()
dic2 = {'k1': 'v1', 'k2': 'v2', 'k3': 'v3'}
dic3 = dict([('name', 'L3opold7'), ('phone', '010-1234-5678')])
dic4 = dict(firstname='Myungseo', lastname='Kang')
dic5 = {'ls': ['a', 'b', 'c']}

print(dic2)               # {'k1': 'v1', 'k3': 'v3', 'k2': 'v2'}
print(dic2['k2'])         # v2
print(dic3)               # {'phone': '010-1234-5678', 'name': 'L3opold7'}
print(dic3['name'])       # L3opold7
print(dic4)               # {'firstname': 'Myungseo', 'lastname': 'Kang'}
print(dic4['firstname'])  # Myungseo
print(dic5['ls'])         # ['a', 'b', 'c']
```

빈 Dictionary를 만들땐 dict() 함수를 사용하면 됩니다. 물론 내용이 있는 Dictionary를 만들 때 사용해도 됩니다! 그리고 value 값을 호출할 때는 Dictionary이름[‘키값’] 으로 호출하게 되면 값을 얻을 수 있습니다. 또한 Dictionary의 값으로 List도 넣을 수 있다.

```
test = {1: 'first'}
test[2] = 'second'

print(test)  # {2: 'second', 1: 'first'}
```

Dictionary는 간단하게 키값을 지정해주고 추가해주면 됩니다.

```
test = {1: 'first', 2: 'second', 3: 'third'}

del test[2]
print(test)  # {1: 'first', 3: 'third'}
```