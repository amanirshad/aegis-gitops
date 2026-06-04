# Aegis GitOps

This repository contains the declarative GitOps configuration for the Aegis platform.

## Purpose

This repository acts as the source of truth for all Kubernetes resources managed by ArgoCD.

## Structure

* clusters/local/argocd - ArgoCD bootstrap and root applications
* clusters/local/observability - Monitoring, logging and tracing stack
* clusters/local/platform - Shared platform services and operators
* clusters/local/applications - Business applications including Aegis

## Workflow

1. Bootstrap cluster using aegis-bootstrap
2. Install ArgoCD
3. Connect ArgoCD to this repository
4. ArgoCD continuously reconciles desired state from Git

## Principles

* Git is the source of truth
* All changes are made through pull requests
* No manual kubectl apply in production workflows
* Declarative infrastructure and applications
