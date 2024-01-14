### DB 인덱스로 B tree계열을 사용하는 이유
**B-Tree(Binary Search Tree)의 특징**
1.  B tree는 자녀노드 수를 3~5개까지 가질 수 있어 데이터를 찾을 때 탐색 범위를 빠르게 좁힐 수 있다.
2. 또 노드 데이터 수도 2~4개 까지 가질 수 있어서 block단위로 가져올 때 더 관련된 데이터를 같이 가지고 올 수 있다. (block단위에 대한 저장 공간 활용도가 좋다.

**컴퓨터의 구조**
- cpu - Main memory(RAM) - Secondary storage(SSD/HDD)
- cpu
- RAM : 한시적 데이터 저장공간. 연산코드와 그의 결과값 등이 저장되며, 속도가 빠르다.
- Secondary storage : 연산 속도가 가장 느리고, Block단위로 데이터를 저장한다. 

**DB와 Secondary storage**
- DB는 기본적으로 Secondary storage(SSD/HDD)에 저장된다.
- Secondary storage는 block단위로 데이터를 읽고 쓰기 때문에 연관된 데이터를 모아서 저장하면 더 효율적으로 읽고 쓸 수 있다.
- DB에서 데이터를 조회할 때 Secondary storage에 최대한 적게 접근하는 것이 성능 면에서 좋다.

**B-Tree계열을 DB 인덱스로 사용하는 이유**
1. DB는 기본적으로 secondary  storage에 저장된다.
2. B-Tree index는 self-balancing

**참고로 알아볼 것**
- 시간 복잡도(O(logN))
	- 평균 케이스, 최악 케이스의 조회,삽입, 삭제시의 시간