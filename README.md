# K8s-CR

This is custom resource definition for kubernetes

## Steps to install operator-sdk

Link: https://sdk.operatorframework.io/docs/installation/


# Commands to generate Controller and CRDs

## Init project

operator-sdk init --plugins go/v4 --domain "sushilbhile.dev" --owner "Sushil Bhile" --repo "github.com/sushilmax93/K8s-CR"

## Create API

operator-sdk create api --kind Scaler --group api --version v1alpha1

## Create manifests and sample files for CRDs

make manifests

## To Run the controller

make run

## Regenerate CRDs

To regenerate CRDs when we make changes in api/v1alpha1/*types.go run following commands:

make manifests; make run