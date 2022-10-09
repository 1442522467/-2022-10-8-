#### [剑指 Offer II 024. 反转链表](https://leetcode.cn/problems/UHnkqh/)

给定单链表的头节点 `head` ，请反转链表，并返回反转后的链表的头节点。

~~~
/**

* Definition for singly-linked list.

* public class ListNode {

* int val;

* ListNode next;

* ListNode() {}

* ListNode(int val) { this.val = val; }

* ListNode(int val, ListNode next) { this.val = val; this.next = next; }

* }

*/

class  Solution {

public  ListNode  reverseList(ListNode  head) {

if(head==null){return  null;}

if(head.next==null){return head;}

ListNode  root=reverseList(head.next);

head.next.next=head;

head.next=null;

return root;

}

}
~~~
