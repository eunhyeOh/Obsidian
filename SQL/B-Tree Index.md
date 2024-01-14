### DB 인덱스로 B tree계열을 사용하는 이유

DB는 Secondary storage(SSD/HDD)에 저장된다.
서컨더리 스토리지는 block단위로 

- B Tree 
	- Binary Search Tree
- 시간 복잡도(O(logN))
	- 평균 케이스, 최악 케이스의 조회,삽입, 삭제시의 시