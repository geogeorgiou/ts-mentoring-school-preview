---
theme: seriph
background: /intro.png
title: TS Mentoring School Preview

fonts:
  sans: "chalet-new-york-sixty"
  serif: "Montserrat"
  mono: "chalet-new-york-sixty"

class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# TS Mentoring School Preview

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Let's dive in! <carbon:arrow-right />
</div>

<div class="abs-bl m-6 text-xl">
  <a href="https://github.com/agileactors/ts-workshop" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: slide-left
src: ./pages/intro.md
hide: false
---

---
transition: slide-up
level: 2
layout: image-right
image: /repo-anatomy.png
---

# GH Repo Anatomy 🩻

<br/>

- 📚 **Reading** - `<topic>/**`
- 📝 **Exercises** - `<topic>/src/README.md`
- 🤔 **Starter** - `<topic>/src/initial.ts`
- 🤩 **Solutions** - `<topic>/src/final.ts`


---
src: ./pages/ts-intermediate-preview.md
hide: false
---

---
src: ./pages/aknowledgments.md
hide: false
---

---
src: ./pages/qna.md
hide: false
---

---
layout: center
class: text-center
---

# Learn More

<!-- //TODO STACKBLITZ REPO -->
[AA Training Material](https://typescript--aa-trainings.netlify.app/) · [Github Repo](https://github.com/agileactors/ts-workshop)

<PoweredBySlidev mt-10 />
