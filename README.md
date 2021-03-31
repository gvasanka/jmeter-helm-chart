# jmeter-helm-chart

Developer: Asanka Vithanage

Helm repository for JMeter related Helm charts



---
This Helm chart is capable of deploying JMeter slave machines. Chart provides several
deployment customizations. 

Following customization possible with the current implementation, Please refer and change
values.yaml file values as per your requirements

1. User can deploy JMeter slave machines with custom CPU and memory allocations.
2. Chart can be used to deploy different JMeter versions
3. JMeter JVM memory allocation can be customizable

--
Helm chart can be build and published following below steps
1. helm lint charts/*
2. helm package charts/*
3. helm repo index --url https://gvasanka.github.io/jmeter-helm-chart/ .
4. git commit
5. git push

Add helm chart and pull chart with below steps
1. helm repo add gvasanka https://gvasanka.github.io/jmeter-helm-chart
2. helm repo update
3. helm search jmeter-slave
4. helm install --wait gvasanka/jmeter-slave --name jmeter-slave-machines
5. helm list
6. helm delete --purge jmeter-slave-machines
