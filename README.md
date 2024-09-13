## DevOps

Scripts for managing the Magistrala IoT platform. For installation instructions, refer to [Magistrala Kubernetes Documentation](https://docs.magistrala.abstractmachines.fr/kubernetes/).

### Autogenerating Helm Chart Documentation

The documentation for Magistrala Helm charts in `charts/magistrala/README.md` is generated using `helm-docs`, which extracts metadata from `Chart.yaml` and `values.yaml`. To update the documentation after changes, follow these steps:

### Prerequisites

Before starting, ensure the following tools are installed:

1. **Helm**  
   Make sure [Helm](https://helm.sh) is installed on your system. If not, follow the [Helm installation guide](https://helm.sh/docs) to get started.

2. **Helm Docs Tool**  
   The documentation for the Magistrala Helm charts is autogenerated using the `helm-docs` tool. To install `helm-docs`, use the following command:

   ```bash
   go install github.com/norwoodj/helm-docs/cmd/helm-docs@latest
   ```

   If Go is not installed, follow the [Go installation guide](https://golang.org/doc/install).

### Step 1: Navigate to Your Project Directory

First, move to the directory where the Helm charts are stored. For this project, the command would be:

```bash
cd devops
```

### Step 2: Run the `helm-docs` Command

Generate or update the documentation for your Helm charts by running:

```bash
helm-docs
```

This command will parse the charts in the `charts` directory and update the `charts/magistrala/README.md` file. A typical successful run looks like this:

```bash
INFO[2024-09-11T11:34:20+03:00] Found Chart directories [charts/magistrala]
INFO[2024-09-11T11:34:20+03:00] Generating README Documentation for chart charts/magistrala
```

### Step 3: Commit and Push the Changes

After `helm-docs` has updated the documentation, review the changes, and then commit and push them to your Git repository:

```bash
git add charts/magistrala/README.md
git commit -m "Update Helm chart documentation"
git push origin <your-branch>
```

Replace `<your-branch>` with the branch you are working on.

## License

This project is licensed under the [Apache-2.0](LICENSE).
