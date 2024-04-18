# Converting Array into Linked List


``` JAVA
public class Solution {
    public static Node constructLL(int []arr) {
        // 'n' be the size of the array 'arr'
        int n = arr.length;

        // 'head' variable stores the head of the
        // linked list
        Node head = new Node(arr[0]);
        Node temp = head;

        for(int i = 1; i < n; ++i) {
            // Attach current node to the "next"
            // of the previous node
            Node curNode = new Node(arr[i]);
            temp.next = curNode;
            temp = temp.next;
        }

        return head;
    }
}
```