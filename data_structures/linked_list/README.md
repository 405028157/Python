## 算法总结
1、单向链表
2、双向链表
3、从列表生成链表
4、判断链表是否有循环
5、判断链表是否回文
6、合并俩个链表
7、找链表中间的元素
8、交换链表中俩个值对应的节点（把值互换就可）
## 知识点
1、实现Node节点， \__repr__() 方便调试，也可以仿照写一个 \__str__() [from_sequence.py](./from_sequence.py) 
```python
class Node:
    def __init__(self, data=None):
        self.data = data
        self.next = None

    def __repr__(self):
        """Returns a visual representation of the node and all its following nodes."""
        string_rep = ""
        temp = self
        while temp:
            string_rep += f"<{temp.data}> ---> "
            temp = temp.next
        string_rep += "<END>"
        return string_rep
```

2、@property, \__iter__() [has_loop](./has_loop.py) 
3、fast节点往前遍历的时候，while循环的条件写法 [is_palindrome](./is_palindrome.py)
```python
while fast and fast.next:
        fast = fast.next.next
```
4、@dataclass https://docs.python.org/3/library/dataclasses.html
[merge_two_lists](./merge_two_lists.py)
5、self.head = Node(item, self.head) 链表头添加节点，简洁！[__init__.py](./__init__.py)
根据数组生成链表，也可以用这个方法，不过要先把数组逆转, reversed(list)就可以
6、从终端处理IO [middle_element_of_linked_list](./middle_element_of_linked_list.py)