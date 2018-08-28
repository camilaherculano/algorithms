#include <bits/stdc++.h>

using namespace std;

class Node {
    public:
        int data;
        Node * left;
        Node * right;
        Node(int d) {
            data = d;
            left = NULL;
            right = NULL;
        }
};

class Solution {
    public:
  		Node * insert(Node * root, int data) {
            if(root == NULL) {
                return new Node(data);
            } else {
                Node * cur;
                if(data <= root->data) {
                    cur = insert(root->left, data);
                    root->left = cur;
                } else {
                    cur = insert(root->right, data);
                    root->right = cur;
               }

               return root;
           }
        }

    void bfs(Node * current) {
        queue<Node *> q; q.push(current);
        Node * it;
        while(!q.empty()) {
            it = q.front();
            cout << it->data << " ";
            q.pop();
            
            if(it->left != NULL) q.push(it->left);
            if(it->right != NULL) q.push(it->right);
        }
    }
};

int main() {
  
    Solution tree;
    Node * root = NULL;
    
    int t;
    int data;

    std::cin >> t;

    while(t-- > 0) {
        std::cin >> data;
        root = tree.insert(root, data);
    }

    tree.bfs(root);
    
    return 0;
}
