Kubernetes has been widely adopted in the enterprise for its ability to manage and orchestrate containerized applications at scale. As a result, Kubernetes has become a prime target for malicious actors. In order to ensure the security of your Kubernetes environment, it is important to be aware of the various security risks and take the necessary precautions.

The NSA has released a great guide on how to harden Kubernetes.

The key recommendations from each section are:
- Use containers built to run applications as non-root users
- Where possible, run containers with immutable file systems
- Scan container images for possible vulnerabilities or misconfigurations
- Use a Pod Security Policy to enforce a minimum level of security, including:
- Preventing privileged containers
- Denying container features frequently exploited to breakout, such as hostPID, hostIPC, hostNetwork, allowedHostPath
- Rejecting containers that execute as the root user or allow elevation to root
- Hardening applications against exploitation using security services such as SELinux®, AppArmor®, and seccomp
- Lock down access to control plane nodes using a firewall and role-based access control (RBAC)
- Further limit access to the Kubernetes etcd server
- Configure control plane components to use authenticated, encrypted communications using Transport Layer Security (TLS) certificates
- Set up network policies to isolate resources. Pods and services in different namespaces can still communicate with each other unless additional separation is enforced, such as network policies
- Place all credentials and sensitive information in Kubernetes Secrets rather than in configuration files. Encrypt Secrets using a strong encryption method
- Disable anonymous login (enabled by default)
- Use strong user authentication
- Create RBAC policies to limit administrator, user, and service account activity
- Enable audit logging (disabled by default)
- Log all API requests and responses
- Store logs for at least 90 days

![image](https://user-images.githubusercontent.com/99908467/154585522-d9d8c1ac-7fed-4abb-b684-608468b42a6c.png)

One of the biggest security risks with Kubernetes is that it provides a single point of failure for all of your containerized applications. If an attacker is able to gain access to your Kubernetes environment, they could potentially wreak havoc on your organization. To mitigate this risk, it is important to ensure that your Kubernetes environment is well protected with strong authentication and authorization mechanisms.

Another risk with Kubernetes is that it provides a wealth of information about the applications running in your environment. This information can be valuable to attackers who are looking to exploit vulnerabilities in your applications. To protect against this, it is important to use encryption for all traffic between your applications and Kubernetes, and to ensure that your applications are properly patched and secured.

In addition to securing your Kubernetes environment, it is also important to secure the data that is stored in your Kubernetes clusters. To do this, you should use encryption to protect your data at rest, and ensure that your clusters are properly secured with firewalls and other security measures.
By taking the necessary precautions, you can help to ensure the security of your Kubernetes environment and protect your organization from malicious actors.
For more, see this great talk “Kubernetes Security Best Practices” by Ian Lewis at Google: https://www.youtube.com/watch?v=wqsUfvRyYpw