                     FLUX Kustomize
┌─────────────────────────────────────────────┐
│                                             │
│  sourceRef ──────► Where are the files?     │
│                                             │
│  path ───────────► Which files?             │
│                                             │
│  interval ───────► When to reconcile?       │
│                                             │
│  timeout ────────► How long to wait?        │
│                                             │
│  prune ──────────► Delete obsolete objects? │
│                                             │
│  ┌───────────────────────────────────────┐  │
│  │             KUSTOMIZE                 │  │
│  │                                       │  │
│  │  resources                            │  │
│  │  patches                              │  │
│  │  replacements                         │  │
│  │  generators                           │  │
│  └───────────────────────────────────────┘  │
│                     │                       │
│                     ▼                       │
│              rendered YAML                  │
│                     │                       │
│  postBuild ─────────► substitutions         │
│                     │                       │
│                     ▼                       │
│              Kubernetes API                 │
└─────────────────────────────────────────────┘