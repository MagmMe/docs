---
Title: "animation-fill-mode"
Subjects:
  - "Web Development"
  - "Web Design"
Tags:
  - "Animation"
Catalog Content:
  - "https://www.codecademy.com/learn/learn-css"
  - "https://www.codecademy.com/learn/paths/front-end-engineer-career-path"
  - "https://www.codecademy.com/learn/paths/full-stack-engineer-career-path"
---

## Definition

Defines what values are applied by an animation outside of its execution time.

## Syntax

```css
animation-fill-mode: <value>;
```

where `<value>` can be one of the following:

- `none`: Default, no animation styles will be applied outside of the animation's execution time.
- `forwards`: The last keyframe values computed will be retained outside of the animation's execution time.
- `backwards`: The initial keyframe values computed will be retained outside of the animation's execution time.
- `both`: Provides both `forwards` and `backwards` values to `animation-fill-mode` property.

**Note:**  The first and last keyframe computed values depend on the value of `animation-direction` and `animation-iteration-count`.

## Example 1

Use `forwards` to persist the last keyframe values computed outside of the animation's execution time:

```css
div {
  height: 200px;
  width: 200px;
  background-color: blue;
  animation-name: disappear;
  animation-duration: 2s;
  animation-fill-mode: forwards;
}

@keyframes disappear {
  from {
    background-color: blue;
  }
  to {
    background-color: white;
  }
}
```

## Example 2

Use `backwards` to persist the initial keyframe values computed outside of the animation's execution time:

```css
div {
  height: 200px;
  width: 200px;
  background-color: blue;
  animation-name: disappear;
  animation-duration: 2s;
  animation-fill-mode: backwards;
}

@keyframes disappear {
  from {
    background-color: blue;
  }
  to {
    background-color: white;
  }
}
```