environments/
└── k3s-dev/
    ├── Chart.yaml
    ├── values.yaml                  # Which applications are enabled
    ├── templates/                   # Argo CD Application templates
    │   ├── house-price-api.yaml
    │   └── loki.yaml
    │
    ├── values/                      # Dev-specific overrides
    │   ├── house-price-api.yaml
    │   ├── loki.yaml
    │   └── kube-prom-stack.yaml
    │
    └── charts/                      # Dev's independent chart copies
        ├── applications/
        │   └── house-price-api/
        │       ├── Chart.yaml
        │       ├── values.yaml      # Chart defaults
        │       └── templates/
        └── platform/
            └── loki/
                ├── Chart.yaml
                ├── values.yaml      # Chart defaults
                └── templates/