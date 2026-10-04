# Longest Common Prefix - Java 

A fast and memory-efficient Java solution for finding the **Longest Common Prefix** among an array of strings.

---

## 📌 Problem Description

Write a function to find the longest common prefix string amongst an array of strings. If there is no common prefix, return an empty string `""`.

### Examples
- **Example 1:**
  - **Input:** `["flower", "flow", "flight"]`
  - **Output:** `"fl"`
- **Example 2:**
  - **Input:** `["dog", "racecar", "car"]`
  - **Output:** `""`
  - **Explanation:** There is no common prefix among the input strings.

---

## 💡 Solution Overview: Vertical Scanning

This solution uses the **Vertical Scanning** approach. Instead of comparing full strings horizontal-style, it checks characters index-by-index across all strings simultaneously.

```text
Index:    0 1 2 3 4 5
strs[0]:  f l o w e r
strs[1]:  f l o w
strs[2]:  f l i g h t
          | | |
          | | └─ Mismatch at index 2 ('o' != 'i') ➔ Return substring(0, 2) => "fl"
          | └── Match at index 1 ('l')
          └──── Match at index 0 ('f')
Solution: Java
- ** Time complexity**:0(s)
- ** Space complexity**:0(1)
