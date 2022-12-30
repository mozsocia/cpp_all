```cpp

// Online C++ compiler to run C++ program online
#include <iostream>


class Node {
    public:
  int val;
  Node* left;
  Node* right;
  Node(int val) : val(val), left(nullptr), right(nullptr) {}
};


void print(const Node* node, int level)
{
  if (node == nullptr)
  {
    std::cout << "null";
    return;
  }

  std::cout << "Node { ";
//   for (int i = 0; i < level+1; ++i)
//   {
//     std::cout << "    ";
//   }
  std::cout << "val: " << node->val << "\n";
  for (int i = 0; i < level+1; ++i)
  {
    std::cout << "      ";
  }
  std::cout << "left: ";
  print(node->left, level + 1);
  std::cout << "\n";
  for (int i = 0; i < level+1; ++i)
  {
    std::cout << "      ";
  }
  std::cout << "right: ";
  print(node->right, level + 1);
  std::cout << " }";
}

int main() {
    Node* root = new Node(1);
    root->left = new Node(2);
    root->right = new Node(3);
    root->right->left = new Node(4);
    root->right->right = new Node(5);
    
    print(root, 0);

    return 0;
}

```

### output

![image](https://user-images.githubusercontent.com/12442613/210036068-ed71e27e-f50c-4747-be1b-2fa5fb8039f1.png)


