# Debugging Techniques

**What it is:**
- Debugging is the process of identifying, isolating, and fixing issues in software systems.
- It requires a combination of tooling, methodology, and domain knowledge.

---

## General Debugging Process

1. **Reproduce the issue**
2. **Check logs / output / error messages**
3. **Isolate the problem (reduce surface area)**
4. **Form and test hypotheses**
5. **Verify the fix and monitor**

---

## Language-Specific Tips

### Python
- Use `print()` or logging (`logging.debug/info/warning/error`)
- Use `pdb` (Python debugger): `import pdb; pdb.set_trace()`
- Inspect stack traces for `NameError`, `KeyError`, etc.
- Use `pytest -s -x` to stop on first failure with output

### Java
- Use IDE breakpoints (IntelliJ, Eclipse)
- Log exceptions and inspect stack traces (`e.printStackTrace()`)
- Enable debug logging via `log4j.properties` or `slf4j`
- Use `jconsole` or `jvisualvm` for memory/thread debugging

### Bash
- Add `set -x` to see script execution
- Use `trap 'commands' ERR` to catch error points
- Check `$?` exit codes after commands
- Redirect stdout/stderr to logs

---

## Distributed Systems

- **Check logs across components**
  - Include request IDs for correlation
- **Understand retries and timeouts**
- **Use health checks and metrics**
- Use observability tools (Grafana, Prometheus, OpenTelemetry)

---

## Debugging in Kubernetes
- `kubectl logs <pod>` — see container logs
- `kubectl exec -it <pod> -- /bin/sh` — shell into a pod
- `kubectl describe pod <pod>` — see pod lifecycle events and resource issues
- Check readiness and liveness probe status

---

## Data Engineering Debugging

- Check nulls, type mismatches, schema drift
- Look for partitions with missing/extra columns
- Validate row counts across sources
- Compare hashes/checksums to validate migration or load

---

## Debugging SQL

- Add `LIMIT` early to reduce scan time
- Use `EXPLAIN` to inspect query plans
- Log slow queries and tune indexes
- Validate assumptions: filter conditions, joins, NULL handling

---

## Debugging Tips for Interviews
- Walk through your process out loud
- Be hypothesis-driven: “I checked the logs and saw…”
- Prioritize reproducibility and metrics over guesswork
- Emphasize **how you validated** a fix and monitored impact
