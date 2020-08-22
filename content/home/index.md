+++
<script src="https://identity.netlify.com/v1/netlify-identity-widget.js"></script>

# Homepage
type = "widget_page"
headless = true  # Homepage is headless, other widget pages are not.
<script>
  if (window.netlifyIdentity) {
    window.netlifyIdentity.on("init", user => {
      if (!user) {
        window.netlifyIdentity.on("login", () => {
          document.location.href = "/admin/";
        });
      }
    });
  }
</script>
+++
