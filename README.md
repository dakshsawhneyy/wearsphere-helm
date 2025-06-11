
# wearsphere-helm

Helm chart for deploying the **WearSphere** e-commerce application on Kubernetes.

##  Components

This Helm chart includes deployments and services for the following components:

- `frontend`: React-based client UI
- `backend`: Node.js Express server
- `admin`: Vite-powered React admin panel
- `MongoDB`: Installed via Bitnami Helm chart (external dependency)

##  Features

- Modular Helm templates for frontend, backend, and admin services
- Environment-ready values via `values.yaml`
- Support for production-grade deployment using probes
- Easily configurable and reusable
- Compatible with Prometheus, Grafana, Trivy, and SonarQube integrations
- CI/CD ready with GitHub Actions / Jenkins

##  Installation

```bash
# Add the repo (if packaged and hosted externally)
helm repo add wearsphere-helm https://github.com/yourusername/wearsphere-helm

# OR clone and install locally
git clone https://github.com/yourusername/wearsphere-helm.git
cd wearsphere-helm
helm install wearsphere . -n wearsphere --create-namespace
```

##  Customization

You can edit `values.yaml` to configure environment-specific variables like:
- Container image tags
- Replica count
- MongoDB connection strings
- Service ports
- Resource requests and limits

##  Structure

```
.
├── Chart.yaml
├── values.yaml
├── templates/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
├── wearsphere-helm-0.1.0.tgz  # Optional: packaged Helm chart
└── README.md
```

##  Probes

This chart includes **liveness** and **readiness** probes for production stability.


```

##  Contributing

Feel free to open issues or pull requests to improve the chart!
