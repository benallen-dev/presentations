---
layout: cover
background: /john-towner-JgOeRuGD_Y4-unsplash.jpg
---

# Chapter 4

## Conclusions

---
layout: image-right
image: /john-towner-JgOeRuGD_Y4-unsplash.jpg
transition: view-transition
---

# HTMX is pretty freakin sweet

<v-clicks>

- No leaky abstractions
- Can be integrated only where needed
- Changing behaviour only implemented once
- No TS/JS build step
- Using HTMX makes you look cool and hip
- Vim is still the one true editor

</v-clicks>

---
layout: cover
image: background
transition: view-transition
---

# Example: Adding login

```go {all|6-11|13-16|18}
func GetCommentForSlug(w http.ResponseWriter, r *http.Request) {
	slug := chi.URLParam(r, "slug")

	log.Println("GetCommentForSlug", slug)

	// Get the comments for the slug
	comments, err := data.GetCommentsForSlug(slug)
	if err != nil {
		log.Panic(err)
		return
	}

	if len(comments) == 0 {
		templ.Handler(views.NoComments()).ServeHTTP(w, r)
		return
	}

	templ.Handler(views.Comments(comments)).ServeHTTP(w, r)
}
```


---
layout: cover
image: background
transition: view-transition
---

# Example: Adding login (2)

```go {all|6-9|all}
func GetCommentForSlug(w http.ResponseWriter, r *http.Request) {
	slug := chi.URLParam(r, "slug")

	log.Println("GetCommentForSlug", slug)

	// Let's just pretend we have some kind of user context 
	if(!ctx.LoggedInUser()) {
		templ.Handler(views.LoginForm()).ServeHTTP(w,r)
		return
	}

	// Get the comments for the slug
	comments, err := data.GetCommentsForSlug(slug)
	if err != nil {
		log.Panic(err)
		return
	}

	if len(comments) == 0 {
		templ.Handler(views.NoComments()).ServeHTTP(w, r)
		return
	}

	templ.Handler(views.Comments(comments)).ServeHTTP(w, r)
}
```

---
layout: cover
background: /john-towner-JgOeRuGD_Y4-unsplash.jpg
---

# HTMX is dope

<v-click>

## The end

</v-click>
