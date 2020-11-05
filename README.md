# Custom error pages in Razor

Can use either

```csharp
app.UseStatusCodePagesWithRedirects("/errors/_{0}");
```

or

```csharp
app.UseStatusCodePagesWithReExecute("/errors/_{0}");
```

Redirect will redirect to the error page with a 302 HTTP status code.

Re-Execute will re-execute the request pipeline but show the error page thereby preserving the error code which is probably a good thing for SEO.
