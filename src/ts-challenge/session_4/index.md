---
marp: true
theme: ts_challenge
color: #ededed;
---

### 2025/02/06

# TS Challenge - 4

### Keita Kawabata

<!--
_class: title
 -->

---

# Problem 1

### - [If](https://github.com/type-challenges/type-challenges/blob/main/questions/00268-easy-if/README.md) -

<!--
_class: lead
 -->

---

## Problem 1

### Implement the util type `If<C, T, F>` which accepts condition `C`, a truthy value `T`, and a falsy value `F`.

![](./images/image.png)

---

## Solution

![](./images/image-1.png)

---

# Prerequisites

1. Generics
2. Conditional Type

<!--
_class: prereq
 -->

---

# Prerequisites

1. Generics
2. Conditional Type

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

## Conditional Type - Basic

#### Allow you to define types dynamically based on conditions.

![](./images/image-6.png)

---

## Problem 1

### Implement the util type `If<C, T, F>` which accepts condition `C`, a truthy value `T`, and a falsy value `F`.

![](./images/image.png)

---

## Solution

![](./images/image-1.png)

---

# Problem 2

### - [Exclude](https://github.com/type-challenges/type-challenges/blob/main/questions/00043-easy-exclude/README.md) -

<!--
_class: lead
 -->

---

## Problem 2

### Implement the built-in `Exclude<T, U>`

![](./images/image-2.png)

---

## Solution

![](./images/image-3.png)

---

# Prerequisites

1. Generics
2. `never` type
3. Distributive Conditional Type

<!--
_class: prereq
 -->

---

# Prerequisites

1. Generics
2. `never` type
3. Distributive Conditional Type

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

## `never` type

- `never` is an empty type — it represents nothing.

![bg contain right:60%](./images/image-9.png)

---

# Prerequisites

1. Generics
2. `never` type
3. Distributive Conditional Type

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

## Distributive Conditional Type

#### `T extends U ? X : Y`

- if `T` is a union type, the condition is applied to each member of the union separately.

![w:900](./images/image-7.png)

---

## Distributive Conditional Type

### - with `never` type

![](./images/image-8.png)

---

## Problem 2

### Implement the built-in `Exclude<T, U>`

![](./images/image-2.png)

---

## Solution

![](./images/image-3.png)
