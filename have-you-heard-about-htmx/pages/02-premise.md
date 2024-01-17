---
layout: cover
background: /john-towner-JgOeRuGD_Y4-unsplash.jpg
---

# Chapter 2

## What is HTMX

<span class="text-md" v-click>
And why won't I shut up about it?
</span>

---
layout: statement
---

# HTMX gives you access to AJAX, CSS Transitions, Websockets and Server Sent Events directly in HTML

---
layout: cover
background: /john-towner-JgOeRuGD_Y4-unsplash.jpg
---

# HTMX adds attributes to existing HTML elements

<v-clicks>

- These attributes do things like call APIs
- API endpoints return HTML 
- Returned HTML is used to replace the calling element

</v-clicks>

---
layout: cover
background: /john-towner-JgOeRuGD_Y4-unsplash.jpg
---

# Example

```html {all|2}
  <script src="https://unpkg.com/htmx.org@1.9.10"></script>
  <button hx-post="/clicked" hx-swap="outerHTML">
    Click Me
  </button>
```
<v-click>

When the button is clicked, it is replaced with whatever the API returns from the `/clicked` route

</v-click>

<v-click>

```html
  <script src="https://unpkg.com/htmx.org@1.9.10"></script>
  <p>Hi! I'm the response from the server!</p>
```

</v-click>

---
layout: cover
background: /john-towner-JgOeRuGD_Y4-unsplash.jpg
transition: view-transition
---


# Confused?

<v-click>

## Let's just use it

</v-click>

<img class="position-absolute top-50 right-20" src="/confused.jpeg" width="300" alt="Confused Nick Young"/>
