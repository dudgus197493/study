# 트리(tree)
> ### 노드로 이루어진 자료 구조

## 트리의 개념
- 트리는 **하나의 루트 노드**를 갖는다.
- 루트 노드는 **0개 이상의 자식 노드**를 갖는다.
- 그 자식 노드 또한 0개 이상의 자식 노드를 갖고 있고, 이는 반복적으로 정의된다.
- **노드**들과 노드들을 연겨하는 **간선**들로 구성되어 있다.
    - 트리에는 사이클(cycle)이 존재할 수 없다.
    - 노드들은 특정 순서로 나열될 수도 있고 그럴 수 없을 수도 있다.
    - 각 노드는 부모 노드로의 연결이 있을 수도 있고 없을 수도 있다.
    - 각 노드는 어떤 자료형으로도 표현 가능하다.

## 기본적인 트리(tree)의 구조
![트리구조](https://blog.kakaocdn.net/dn/bbNRYk/btqV36qaJux/cklbzws6M82XkJkJaqPA51/img.png)
- `부모노드(parent node)` : 자기 자신과 연결 된 노드 중 **자신보다 높은 노드**를 의미 *(F의 부모노드 B)*
- `자식 노드(child node)` : 자기 자신(노드)과 연결 된 노드 중 **자신보다 낮은 노드**를 의미 *(C의 자식노드 : G, H)*

- `루트 노드 (root node)` : 일명 뿌리 노드라고 하며 루트 노드는 **하나의 트리에선 하나밖에 존재하지 않고, 부모노드가 없다.** 위 이미지에선 녹색이 뿌리노드다.

- `단말 노드(leaf node)` : 리프 노드라고도 불리며 **자식 노드가 없는 노드**를 의미한다. 위 이미지에서 주황색 노드가 단말노드다.

- `내부 노드(internal node)` : 단말 노드가 아닌 노드

- `형제 노드(sibling node)` : 부모가 같은 노드를 말한다. *(D, E, F는 모두 부모노드가 B이므로 D, E, F는 형제노드다.)*

- `깊이(depth)` : 특정 노드에 도달하기 위해 거쳐가야 하는 **'간선의 개수'**를 의미 *(F의 깊이 : A→B→F 이므로 깊이는 2가 됨)*

- `레벨(level)` : **특정 깊이에 있는 노드들의 집합**을 말하며, 구현하는 사람에 따라 0 또는 1부터 시작한다. *(D, E, F, G, H)*

- `차수(degree)` : **특정 노드가 하위(자식) 노드와 연결 된 개수** *(B의 차수 = 3 {D, E, F} )*

<br>

## 이진 트리(Binary Tree)
> ### 기본적인 트리 구조에서 모든 노드의 최대 차수를 2로 제한한 것
> *쉽게 말하면 각 노드는 자식노드를 최대 2개밖에 가질 수 없는 것*

![이진 트리 구조](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FtMysu%2FbtqV0DJgeJf%2FUfsVUDLaMWGFFt7tMpumkk%2Fimg.png)

<br>

## 완전 이진 트리(Complete binary tree)
> ### **마지막 레벨**을 제외한 모든 노드가 채워져있으면서 모든 노드가 왼쪽부터 채워져있는 트리구조

### 완전 이진 트리의 조건
- 마지막 레벨을 제외한 모든 노드가 채워져있어야함
- 모든 노드들은 왼쪽부터 채워져있어야함

![완전 이진 트리](https://cdn.codingworldnews.com/news/photo/202105/3554_4950_509.jpg)

<br>

## 포화 이진 트리(Perfect binary tree)
> ### 완전 이진 트리 에서 **마지막 레벨을 제외한 모든 노드가 두 개의 자식 노드를 갖는** 트리 구조 

![포화 이진 트리](https://sites.google.com/site/2019algorithm3/_/rsrc/1574958571729/gwaje-gong-yu/gwaje3binarytree/%ED%8F%AC%ED%99%94%EC%9D%B4%EC%A7%84%ED%8A%B8%EB%A6%AC.PNG?height=267&width=400)