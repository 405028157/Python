
(from_sequence.py)[./from_sequence.py] 实现的Node节点， __repr__() 方便调试，也可以仿照写一个 __str__()
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