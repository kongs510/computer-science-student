#  `Data Structure` hash and trie

해시(Hash)는 Key-value쌍으로 데이터를 저장하는 자료구조입니다.

해시는 내부적으로 배열을 사용하여 데이터를 저장하기 때문에 빠른 검색 속도를 가진다.

배열에는 여러 키(Key)들이 저장되며, 해쉬 함수를 통해 해당되는 값을 가져옵니다. 

키(Key)는 중복되지 않는 유니크한 값이어야하며, 값(value)은 중복이 가능합니다.

그래서 해시 자료구조의 대표적인 해시 테이블은 O(1)의 시간 복잡도(Big-O)를 가진다. 

하지만 충돌(Collisions)이 일어나서 데이터가 같은 공간에 리스트로 연결이 된다면, 최악의 경우 모든 리스트를 찾아봐야 하기 때문에 O(n)의 시간 복잡도를 가진다.

![image](https://user-images.githubusercontent.com/68903200/177031782-fecc83e9-7c6a-49ab-9429-d294e1650fa5.png)


Hash Table
key-value 에서 key를 테이블에 저장할 때 key값을 Hash Method를 이용해 계산을 수행한 후, 그 결과값을 배열의 인덱스로 사용하여 저장하는 방식이다. 여기서 key값을 계산하는 것이 Hash Method 이다.


Hash Method
Hash는 특별한 알고리즘을 이용하여 데이터의 고유한 숫자값을 만들어 인덱스로 사용한다고 했다. 이 알고리즘을 구현한 메소드를 Hash Method라고 하며 

Hash Method에 의해 반환된 데이터의 고유 숫자값을 Hash Code 라고한다.

자바에서는 Object 클래스의 hashCode() 메소드를 이용하여 모든 객체의 Hash Code를 쉽게 구할 수 있다.

Hash Method를 이용해서 데이터를 Hash Table에 저장하고 검색하는 기법을 Hashing이라 한다.

Hash Method는 데이터가 저장되어 있는 곳을 알려주기 때문에 다량의 데이터 중에서도 원하는 데이터를 빠르게 찾을 수 있다.

<img src="https://user-images.githubusercontent.com/68903200/177036818-edb1fc09-2ad3-4e73-8f23-ceea462abb80.png" width="500" height="500"/>
Hashing

HashMap과 같이 Hashing을 구현한 컬렉션 클래스에서는 Object 클래스에 정의된 hashCode()를 Hash Method로 사용한다. 

Object 클래스에 정의된 hashCode()는 객체의 주소를 이용하는 알고리즘으로 해시 코드를 만들어내기 때문에 모든 객체에 대해 중복되지 않는 값을 제공한다.

String 클래스의 경우 Object로 부터 상속받은 hashCode()를 오버 라이딩하여 문자열의 내용으로 해시 코드를 만들어 낸다. 서로다른 String 인스턴스 일지라도 같은 내용의 

문자열을 가졌다면 hashCode()를 호출했을 때 같은 값을 얻는다.



