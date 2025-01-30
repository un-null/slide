---
marp: true
theme: ts_challenge
color: #ededed;
---

### 2025/01/16

# TS Challenge - 1

### Keita Kawabata

<!--
_class: title
 -->

---

# Problem 1

<!--
_class: lead
 -->

---

## Let's define a `MyReadonly` type!

![](./images/image.png)

---

![w:900](./images/image-12.png)

---

## Solution

![w:1000](./images/image-1.png)

---

# Prerequisites

1. Generics
2. keyof operator
3. Mapped Types
4. index access types

<!--
_class: prereq
 -->

---

# Prerequisites

1. Generics
2. keyof operator
3. Mapped Types
4. index access types

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

![](./images/image-2.png)

---

## Generics - Extends

#### Extends allows you to limit a generic type to a specific type

![](./images/image-3.png)

---

# Prerequisites

1. Generics
2. keyof operator
3. Mapped Types
4. index access types

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

## keyof

#### A method to get object keys as a union type

![](./images/image-4.png)

---

# Prerequisites

1. Generics
2. keyof operator
3. Mapped Types
4. index access types

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

## Mapped Types

#### Can create a new object type based on a union of keys

![bg right contain](./images/image-5.png)

<!--
_class: split
 -->

---

## Mapped Types

#### with keyof operator

![bg right contain](./images/image-6.png)

---

# Prerequisites

1. Generics
2. keyof operator
3. Mapped Types
4. index access types

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

## index access types

#### Can get the type of a specific key in object

![](./images/image-7.png)

---

## Let's define a `MyReadonly` type!

![](./images/image.png)

---

## Solution

![w:1000](./images/image-1.png)

<!--
_class: lead
 -->

---

# Related Probelms - ①

<!--
_class: lead
 -->

---

### Implement a generic `MyReadonly2<T, K>` which takes two type argument T and K.

![w:900](./images/image-8.png)

---

## Solution

- `Omit<Type, Keys>`
  - Creates a new type by excluding properties K from type T.
- `Pick<Type, Keys>`
  - Creates a new type by selecting only the properties K from type T.

![](./images/image-9.png)

---

# Related Probelms - ②

<!--
_class: lead
 -->

---

Implement a generic `DeepReadonly<T>` which make every parameter of an object and its sub-objects recursively readonly.

<style scoped>
  p {
    font-size: 1rem;
    font-weight: 500;
  }
</style>

![bg right contain](./images/image-10.png)

---

## Solution

- **If T is a primitive type**
  - it directly returns T with readonly
  - because primitive types don't have properties
- **If T is an object type, the type applies recursion**
  - It iterates over all properties of T using keyof T.

![](./images/image-11.png)
