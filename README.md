# OpenMatch Match Function

# Installation

```
helm install open-match open-match/open-match \
  --create-namespace \
  --namespace open-match \
  --set open-match-customize.enabled=true \
  --set open-match-customize.evaluator.enabled=true \
  --set open-match-override.enabled=true \
  --set query.replicas=1 \
  --set frontend.replicas=1 \
  --set backend.replicas=1 \
  --set open-match-telemetry.enabled=true
```

# Utilities

```
redis-cli -p 7000 -n 0 flushall && \
redis-cli -p 7001 -n 0 flushall && \
redis-cli -p 7002 -n 0 flushall