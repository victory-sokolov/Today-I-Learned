# Common Errors

```bash
failed to solve with frontend dockerfile.v0: failed to build LLB: failed to load cache key: rpc error: code = Unknown desc = error getting credentials - err: exec: "docker-credential-desktop.exe": executable file not found in $PATH, out: ``
```

**Solution:** 
```
rm docker/config.json
docker login
```

---

