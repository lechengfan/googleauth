##### GitHub OAuth HTTP handler

See <https://godoc.org/github.com/kr/githubauth> for documentation.

###### Example

```go
h := &githubauth.Handler{
	PermittedEmails: map[string]bool{"tommy@interstellar.com":true},
	Keys:         keys(),
	ClientID:     os.Getenv("OAUTH_CLIENT_ID"),
	ClientSecret: os.Getenv("OAUTH_CLIENT_SECRET"),
}
http.ListenAndServe(":8080", h)
```
