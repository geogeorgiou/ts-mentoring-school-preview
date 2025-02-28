---
transition: slide-up
---

# TS Intermediate Section Sneak Peek 🫣

<div grid="~ cols-2 gap-4" class="flex justify-center items-center mt-15">
<div class="flex flex-col items-center">

Have you heard about these concepts before?

- **As const**
- **Indexed Access Types**
- **Satisfies Operator**
- **Type Predicate Inference**
- **Infer**

</div>
<div class="flex flex-col items-center">

<img src="/slido-qna.png" alt="slido QnA" class="w-1/3 rounded shadow bg-white" />
</div>
</div>

---

# As const 

As const as in just stay immutable on my watch ✋! 

```ts twoslash
const obj = {
  name: "John",
  age: 30,
} as const;
```

We'll cover how to use it, unique use cases and more!


---

# Satisfies Operator Why ?

We'll see if this operator "satisfies" your needs!

```ts twoslash
type PersonName = "John" | "Jack" | "Justin";
type OtherDetails = {
  id: number;
  age: number;
};

type PersonInfo = PersonName | OtherDetails;

type Person = {
  myInfo: PersonInfo;
  myOtherInfo: PersonInfo;
};
const applicant: Person = {
  myInfo: "John",
  myOtherInfo: { id: 123, age: 22 },
};

applicant.myInfo.toUpperCase();
```

---

# Satisfies Operator

dynamic type inference...

```ts twoslash
type PersonName = "John" | "Jack" | "Justin";
type OtherDetails = {
  id: number;
  age: number;
};

type PersonInfo = PersonName | OtherDetails;

type Person = {
  myInfo: PersonInfo;
  myOtherInfo: PersonInfo;
};

const applicantWithSatisfies = {
  myInfo: "John",
  myOtherInfo: { id: 123, age: 22 },
} satisfies Person;

applicantWithSatisfies.myInfo.toUpperCase();
```

---

# Indexed Access Types

Did you know you can access type properties like you do with values? 🤯

```ts twoslash
type User = {
  id: number;
  name: string;
  isActive: boolean;
};

type UserName = User["name"];
```

More on this in the course! + tips and tricks!

---
transition: slide-up
level: 2
---


<div class="flex justify-center items-center h-[50vh]">
<div class="flex flex-col items-center">
<img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExM2UweXZxcngycXBhcnlrOXh3dXZoeDF6ZXVxdTFmbnJpbXUzZ3FmMCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/3o7P4F86TAI9Kz7XYk/giphy.gif" alt="operators-salt-bae" class="rounded shadow w-[300px]" />
</div>
</div>

---

# Type predicate inference

Uncovering how TS works under the hood depending on version 🕵️

```markdown
//some code

function isString(value: unknown) {
  return typeof value === "string";
}
```

- Delve into why that's important and exploiting it to our advantage!

---

# Infer

Demystifying the infer keyword and it's allure!

```ts twoslash
const func = (x: number): string => x.toString();

//first example with Custom Implementation of ReturnType
type GetReturnType<T> = T extends (...args: any[]) => infer R ? R : never;
```
