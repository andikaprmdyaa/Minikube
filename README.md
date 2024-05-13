# 📝 Tutorial & Exercise 11 📝

**Student Details:**

| Attribute | Information                |
|-----------|----------------------------|
| Name      | Andika Pramudya Wardana   |
| Student ID| 2206046645                 |
| Class     | Advanced Programming KKI   |

---

<details>
<summary>Module 11: Deployment on Kubernetes</summary>

## Questions and Answers

### -> Reflection

#### Reflection on Hello Minikube
1. In the application logs before exposing it as a Service, we see entries indicating the startup of the HTTP and UDP servers, as well as some HTTP GET requests being made to the server. After exposing the application as a Service and opening the app multiple times while the proxy into the Service is running, we observe additional HTTP GET requests in the logs. Yes, the number of logs increases each time the app is opened, reflecting the increased traffic to the application due to it being exposed as a Service.

2. The -n option in kubectl get is used to specify the namespace in which to list the resources. When not provided, kubectl get lists resources from the default namespace. In the given scenario, the first invocation of kubectl get did not specify a namespace, so it listed resources from the default namespace. The second invocation included the -n kube-system option, which instructed kubectl to list resources from the kube-system namespace. The output did not list the pods/services explicitly created because they were likely created in the default namespace, not in kube-system.