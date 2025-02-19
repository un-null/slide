---
marp: true
theme: ts_challenge
color: #ededed;
---

### 2025/02/19

# TS Challenge - 6

### Keita Kawabata

<!--
_class: title
 -->

---

# Problem 1

### - [Parameters](https://github.com/type-challenges/type-challenges/blob/main/questions/03312-easy-parameters/README.md) -

<!--
_class: lead
 -->

---

## Problem 1

### Implement the built-in Parameters generic without using it.

![](./images/image-2.png)

---

## Solution

![](./images/image-3.png)

---

# Prerequisites

1. Function Type
2. Conditional Type
3. `infer`
4. `any` & `unknown` type

<!--
_class: prereq
 -->

---

# Prerequisites

1. Function Type
2. Conditional Type
3. `infer`
4. `any` & `unknown` type

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

## Function Type

![](./images/image-7.png)

---

#### with Spread Syntax

![bg contain right:60%](./images/image-8.png)

---

# Prerequisites

1. Function Type
2. Conditional Type
3. `infer`
4. `any` & `unknown` type

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

## `infer`

- `infer` is a type operator used in Conditional Types.
- It means "to infer" and can only be written on the right side of extends

![w:950](./images/image-9.png)

---

# Prerequisites

1. Function Type
2. Conditional Type
3. `infer`
4. `any` & `unknown` type

<!--
_class: prereq
 -->

<style scoped>
  li:nth-child(4) {
    color: #d23d8d;
    font-weight: 600;
  }
</style>

---

## `any` & `unknown`

![bg contain right:60%](./images/image-10.png)

---

## `any` & `unknown`

- `infer U` works with `any[]`
  - elements have no restrictions
- `unknown[]` blocks inference
  - `unknown` is restrictive
  - TS avoids inference sometimes

![bg contain right:50%](./images/image-11.png)

---

## Problem 1

### Implement the built-in Parameters generic without using it.

![](./images/image-2.png)

---

## Solution

![](./images/image-3.png)

---

# Problem 2

### - [Includes](https://github.com/type-challenges/type-challenges/blob/main/questions/00898-easy-includes/README.md) -

<!--
_class: lead
 -->

---

## Problem 2

### Implement the JS `Array.includes` function in the type system. A type takes the two arguments. The output should be a boolean `true` or `false`.

![](./images/image.png)

---

## Solution - minimum

![](./images/image-4.png)

---

## Solution - best

![](./images/image-5.png)

---

# Prerequisites

1. Conditional Type
2. `T[number]`

<!--
_class: prereq
 -->

---

# Prerequisites

1. Conditional Type
2. `T[number]`

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

## `T[number]`

### allows you to extract the union of the types of all elements of the tuple

![](./images/image-6.png)

---

# Dive into Best Solution

<!--
_class: lead
 -->

---

## Dive into Best Solution

- one example where unione one fails;

![](./images/image-12.png)

---

## Dive into Best Solution

![](./images/image-5.png)

---

## `IsEqual<X, Y>`

![](./images/image-13.png)

---

## `IsEqual<X, Y>`

#### this would allow partial matches :(

![](./images/image-15.png)

---

## `IsEqual<X, Y>`

#### this would not allow partial matches (※ No need to learn that much)

![w:900](./images/image-16.png)

---

## `Includes<>`

#### `Includes` recursively until Rest runs out or U is found

![](./images/image-14.png)

---

## Problem 2

### Implement the JS `Array.includes` function in the type system. A type takes the two arguments. The output should be a boolean `true` or `false`.

![](./images/image.png)

---

## Solution - minimum

![](./images/image-4.png)

---

## Outro

- ### Thank you so much for your participation!

- ### Next:
  - #### Scheduled reading group:
    - [Software Engineering at Google](https://www.oreilly.com/library/view/software-engineering-at/9781492082781/)
  - #### Starting within the next month.
  - #### See you soon!

![bg contain right:40%](https://abseil.io/img/swe_at_google.2.cover.jpg)
