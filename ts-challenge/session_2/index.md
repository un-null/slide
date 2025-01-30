---
marp: true
theme: ts_challenge
color: #ededed;
---

### 2025/01/23

# TS Challenge - 2

### Keita Kawabata

<!--
_class: title
 -->

---

# Problem 1

### - [Length of Tuple](https://github.com/type-challenges/type-challenges/blob/main/questions/00018-easy-tuple-length/README.md) -

<!--
_class: lead
 -->

---

## Problem 1

### Create a generic `Length`, pick the length of the tuple

![](./images/image.png)

---

## Solution

![](./images/image-1.png)

---

## Which is the prefer solution ?

![](./images/image-1.png)

---

## Best solution

![](./images/image-2.png)

---

# Prerequisites

1. `any` / `unknown` type
2. Generics
3. index access types

<!--
_class: prereq
 -->

---

# Prerequisites

1. `any` / `unknown` type
2. Generics
3. index access types

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

## `any`

### Allow all types, any operation

![](./images/image-12.png)

---

## `unknown`

### "Type-safe counterpart of any"

![alt text](./images/image-13.png)

---

# Prerequisites

1. `any` / `unknown`
2. Generics
3. index access types

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

## Generics - Basic

#### A way to create reusable code that works with multiple types

![](././images/image-3.png)

---

## Generics - Extends

#### Extends allows you to limit a generic type to a specific type

![](././images/image-4.png)

---

# Prerequisites

1. `any` / `unknown`
2. Generics
3. index access types

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

## index access types

#### Can get the type of a specific key in object

![w:900](././images/image-5.png)

---

### In Addition, it can access properties in TypeScript type definitions.

![](./images/image-6.png)

---

## Problem 1

### Create a generic `Length`, pick the length of the tuple

![](./images/image.png)

---

## Best solution

![](./images/image-2.png)

---

# Problem 2

### - [Tuple to Object](https://github.com/type-challenges/type-challenges/blob/main/questions/00011-easy-tuple-to-object/README.md) -

<!--
_class: lead
 -->

---

## Problem 2

### transform it into an object type and the key / value must be in the provided array.

![w:850](./images/image-7.png)

---

## Solution

### it works, but we should avoid using `any` type

![](./images/image-8.png)

---

## Solution

![](./images/image-9.png)

---

# Prerequisites

1. `as const` (const assertion)
2. `PropertyKey` type
3. Mapped Types
4. `T[number]` (Tuple)

<!--
_class: prereq
 -->

---

# Prerequisites

1. `as const` (const assertion)
2. `PropertyKey` type
3. Mapped Types
4. `T[number]` (Tuple)

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

## `as const`

### Makes the variable readonly deeply with literal types

![bg right contain](./images/image-15.png)

---

# Prerequisites

1. `as const` (const assertion)
2. `PropertyKey` type
3. Mapped Types
4. `T[number]` (Tuple)

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

## `PropertyKey`

- `PropertyKey` is union type: `string | number | symbol`
  - In TypeScript, object can only have 3 types of values as keys: `string`, `number` and `symbol`

![w:850](./images/image-14.png)

---

# Prerequisites

1. `as const` (const assertion)
2. `PropertyKey` type
3. Mapped Types
4. `T[number]` (Tuple)

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

![bg right contain](././images/image-16.png)

---

# Prerequisites

1. `as const` (const assertion)
2. `PropertyKey` type
3. Mapped Types
4. `T[number]` (Tuple)

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

## What it Tuple

- a special Array type
- Has a fixed length
- Has specific types for each elements

![](./images/image-18.png)

---

## `T[number]`

### allows you to extract the union of the types of all elements of the tuple

![](./images/image-20.png)

---

## `T[number]` with const assertion

![](./images/image-21.png)

---

## Problem 2

### transform it into an object type and the key / value must be in the provided array.

![w:850](./images/image-7.png)

---

## Best solution

![](./images/image-2.png)

---

# Related Problem

### - [Tuple to Union](https://github.com/type-challenges/type-challenges/blob/main/questions/00010-medium-tuple-to-union/README.md) -

<!--
_class: lead
 -->

---

## Related Problem

### Implement a generic TupleToUnion<T> which covers the values of a tuple to its values union.

![](./images/image-10.png)

---

## Solution

- **`unknown` is the best choise in this case**
  - `unknown` permits any element types (e.g., `boolean`)
  - `PropertyKey` permits only `string | number | symbol` types

![](./images/image-11.png)
