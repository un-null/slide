---
marp: true
theme: ts_challenge
color: #ededed;
---

### 2025/01/30

# TS Challenge - 3

### Keita Kawabata

<!--
_class: title
 -->

---

# Problem 1

### [Push](https://github.com/type-challenges/type-challenges/blob/main/questions/03057-easy-push/README.md)

<!--
_class: lead
 -->

---

## Problem 1

### Implement the generic version of `Array.push`

![](./images/image.png)

---

## Solution

![](./images/image-1.png)

---

# Prerequisites

1. Generics
2. `any` / `unknown` type
3. Spread syntax

<!--
_class: prereq
 -->

---

# Prerequisites

1. Generics
2. `any` / `unknown` type
3. Spread syntax

<!--
_class: prereq
 -->

<style scoped>
  li:nth-child(1) {
    color: #d23d8d;
    font-weight: 600;
  }
</style>

---

## Generics - Basic

#### A way to create reusable code that works with multiple types

![](./images/image-12.png)

---

## Generics - Extends

#### Extends allows you to limit a generic type to a specific type

![](./images/image-13.png)

---

# Prerequisites

1. Generics
2. `any` / `unknown` type
3. Spread syntax

<!--
_class: prereq
 -->

<style scoped>
  li:nth-child(2) {
    color: #d23d8d;
    font-weight: 600;
  }
</style>

---

## `any`

### Allow all types, any operation

![](./images/image-10.png)

---

## `unknown`

### "Type-safe counterpart of any"

![](./images/image-11.png)

---

# Prerequisites

1. Generics
2. `any` / `unknown` type
3. Spread syntax

<!--
_class: prereq
 -->

<style scoped>
  li:nth-child(3) {
    color: #d23d8d;
    font-weight: 600;
  }
</style>

---

## Spread syntax - Basic

#### A syntax that expands elements of arrays and objects

![](./images/image-8.png)

---

## Spread syntax - Type

![](./images/image-9.png)

---

## Problem 1

### Implement the generic version of `Array.push`

![](./images/image.png)

---

## Solution

![](./images/image-1.png)

---

# Problem 2

### [Unshift](https://github.com/type-challenges/type-challenges/blob/main/questions/03060-easy-unshift/README.md)

<!--
_class: lead
 -->

---

## Problem 2

### Implement the type version of Array.unshift

![](./images/image-2.png)

---

## Solution

![](./images/image-3.png)

---

# Problem 3

### [Concat](https://github.com/type-challenges/type-challenges/blob/main/questions/00533-easy-concat/README.md)

<!--
_class: lead
 -->

---

## Problem 3

### Implement the JavaScript `Array.concat` function in the type system.

![](./images/image-4.png)

---

## Solution

![](./images/image-5.png)

---

# Related Problem

### [Last of Array](https://github.com/type-challenges/type-challenges/blob/main/questions/00015-medium-last/README.md)

<!--
_class: lead
 -->

---

## Related Problem

### Implement a generic `Last<T>` that takes an Array T and returns its last element.

![](./images/image-6.png)

---

## Solution

- `[unknown, ...T]`
  - `T = [3, 2, 1]` becomes `[unknown, 3, 2, 1]`
- Without `[unknown, ...T]`
  - `[...T][T["length"]]` = `T[3]` is `undefined` (out of bounds.)

![w:1000](./images/image-7.png)
