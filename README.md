This is a sample helm chart meant to test publishing MG helm charts

Add repository

``bash
helm repo add magistrala-devops https://jeffmboya.github.io/MG-helm-example/

````

Install chart

```bash
helm install my-magistrala magistrala-devops/magistrala --version 1.0.6
````

my-magistrala corresponds to the release name, feel free to change it to suit your needs. You can also add additional flags to the helm install command if you need to.
