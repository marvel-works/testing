OPTIONAL_TEST_INFRA_GITOPS_DIRS=./GitOps

#***************************************************************************************************

# Generate YAML files for Optional-Test-Infra GitOps
optional-generate:
	make optional-generate-kubeflow-shared-test-infra-poc
	make optional-generate-kubeflow-shared-test-infra-poc-argo
	make optional-generate-kubeflow-shared-test-infra-poc-tekton

# Generate YAML files for Optional-Test-Infra GitOps for kubeflow-shared-test-infra-poc cluster
optional-generate-kubeflow-shared-test-infra-poc:
	echo "Start generating yaml files for kubeflow-shared-test-infra-poc cluster"
	rm -rf ${OPTIONAL_TEST_INFRA_GITOPS_DIRS}/clusters/kubeflow-shared-test-infra-poc/namespaces/prow/*
	kubectl -n prow create configmap config \
	--from-file=config.yaml=./User/clusters/kubeflow-shared-test-infra-poc/namespaces/prow/configmap/config.yaml \
	--dry-run=client -o yaml > \
	${OPTIONAL_TEST_INFRA_GITOPS_DIRS}/clusters/kubeflow-shared-test-infra-poc/namespaces/prow/config.yaml
	kubectl -n prow create configmap plugins \
	--from-file=plugins.yaml=./User/clusters/kubeflow-shared-test-infra-poc/namespaces/prow/configmap/plugins.yaml \
	--dry-run=client -o yaml > \
	${OPTIONAL_TEST_INFRA_GITOPS_DIRS}/clusters/kubeflow-shared-test-infra-poc/namespaces/prow/plugins.yaml
	echo "Finish generating yaml files for kubeflow-shared-test-infra-poc cluster"

# Generate YAML files for Optional-Test-Infra GitOps for kubeflow-shared-test-infra-poc-argo cluster
optional-generate-kubeflow-shared-test-infra-poc-argo:
	echo "Start generating yaml files for kubeflow-shared-test-infra-poc-argo cluster"
	rm -rf ${OPTIONAL_TEST_INFRA_GITOPS_DIRS}/clusters/kubeflow-shared-test-infra-poc-argo/namespaces/argo/*
	####
	# Add Logic to copy yaml files here
	####
	echo "Finish generating yaml files for kubeflow-shared-test-infra-poc-argo cluster"

# Generate YAML files for Optional-Test-Infra GitOps for kubeflow-shared-test-infra-poc-tekton cluster
optional-generate-kubeflow-shared-test-infra-poc-tekton:
	echo "Start generating yaml files for kubeflow-shared-test-infra-poc-tekton cluster"
	rm -rf ${OPTIONAL_TEST_INFRA_GITOPS_DIRS}/clusters/kubeflow-shared-test-infra-poc-tekton/namespaces/tekton-templates/*
	####
	# Add Logic to copy yaml files here
	####
	echo "Finish generating yaml files for kubeflow-shared-test-infra-poc-tekton cluster"



