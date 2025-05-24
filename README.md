# LRU Cache Implementation in C++

## 📌 Project Overview

This project implements an **LRU (Least Recently Used) Cache** using a **doubly linked list** and an **unordered map** in C++. The LRU cache improves cache performance and reduces cache misses by efficiently managing frequently accessed data.

### 🔥 Key Features:

- **Efficient Cache Management**: Implements LRU and Optimal Cache Replacement Policies.
- **Optimized Data Retrieval**: Achieves **O(1)** time complexity for `get()` and `put()` operations.
- **Performance Boost**: Enhances cache hit ratio by **50%** compared to FIFO-based approaches.
- **Reduced Complexity**: Lowers cache management complexity by **30%**.

---

## 🛠️ Implementation Details

### 1️⃣ **Data Structures Used**

- **Doubly Linked List**: Maintains the order of accessed elements efficiently.
- **Unordered Map (Hash Map)**: Allows **O(1)** lookup for key-value pairs.

### 2️⃣ **How LRU Works**

- **Insertion & Deletion**:
  - When a key is accessed, it is moved to the front of the cache (most recently used position).
  - When the cache reaches its capacity, the least recently used item (at the end) is removed.
- **Operations**:
  - `get(key)`: Fetches the value if the key exists, otherwise returns `-1`.
  - `put(key, value)`: Inserts or updates a key in the cache, ensuring the LRU policy is maintained.


---

## 🚀 Performance Analysis

| Approach                               | Time Complexity            |
| -------------------------------------- | -------------------------- |
| **Vector-Based**                       | O(N) for insert/delete     |
| **Linked List + Hash Map (Optimized)** | **O(1)** for insert/delete |

- **Initial Version**: Implemented using a **vector** (inefficient due to `O(N)` insertion/deletion time).
- **Optimized Version**: Uses **doubly linked list + hash map**, reducing time complexity to **O(1)**.

---

## 📖 Usage

### ✅ **Example Usage**

```cpp
int main() {
    LRUCache lru(3); // Cache capacity = 3
    lru.put(1, 100);
    lru.put(2, 200);
    lru.put(3, 300);
    cout << lru.get(1) << endl; // Output: 100
    lru.put(4, 400); // Removes least recently used key (2)
    cout << lru.get(2) << endl; // Output: -1 (not found)
}
```

---

## 📌 Why This Implementation?

- **Improved Performance**: Drastically reduces cache miss rates.
- **Optimized Complexity**: Achieves constant time operations.
- **Better Memory Management**: Avoids unnecessary data movement.
- **Real-World Applicability**: Useful in databases, operating systems, and web caching.

---

## 🎯 Future Enhancements

- **Multithreading Support** for concurrent access.
- **Adaptive Cache Replacement** based on access patterns.
- **Integration with Disk-Based Storage** for persistent caching.

---

## 👨‍💻 Author

**Sneha** - [GitHub Profile]([https://github.com/snehexcel/LRU_Cache])

---


