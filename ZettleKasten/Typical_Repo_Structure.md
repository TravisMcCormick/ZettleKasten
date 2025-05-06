
---

```bash
/cmd/
    <appname>/
        main.go
/pkg/
    <library code>   # Exported packages for external use
/internal/
    <private app code>  # Non-exported packages, no external usage
/api/
    <proto/ openapi/ api contracts>
/configs/
    <config files and templates>
/deployments/
    <deployment configs: docker-compose, k8s, etc.>
/build/
    <build scripts, ci pipelines>
/scripts/
    <one-off dev tools, migration scripts, setup scripts>
/test/
    <additional test data and helpers>
/docs/
    <markdown docs, architecture diagrams, ADRs>
/web/ 
    <frontend assets if you have a web app>
/vendor/
    <go mod managed, optional>
go.mod
go.sum
README.md
Makefile (optional but strongly recommended)
```

---