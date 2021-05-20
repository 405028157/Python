
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