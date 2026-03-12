# Kubernetes 专用版

这份文档适合 Kubernetes、Helm、Ingress、ConfigMap、Secret、Service、Deployment、StatefulSet、HPA 等相关任务。

延续当前仓库的写法：

- 提示词全部英文
- 说明全部中文
- 可直接复制后再追加你的真实 YAML、日志或需求

---

## 1. 生产级 YAML 审视版
**用途**：让 AI 不把 Kubernetes YAML 当普通文本改，而是按生产环境语义来审。  
**适合**：Deployment、Service、Ingress、Job、CronJob、ConfigMap、Secret 变更。

```text
Treat this as a production Kubernetes change, not as a text-editing task.

Before modifying the manifest, validate whether the requested change is semantically correct, operationally safe, and aligned with common Kubernetes conventions.

Check:
- workload behavior,
- rollout safety,
- service discovery,
- resource requests and limits,
- probes,
- security context,
- config and secret handling,
- backward compatibility.

Do not patch YAML mechanically.
If the current manifest structure is flawed, correct the structure rather than layering more fields onto a broken pattern.
```

## 2. Kubernetes 排障根因版
**用途**：Pod 起不来、CrashLoopBackOff、Pending、探针失败时，让 AI 按 K8s 根因排障。  
**适合**：调度失败、镜像拉取失败、容器崩溃、配置未生效。

```text
Debug this Kubernetes issue systematically.

Do not assume the first visible error is the root cause.
Determine whether the problem comes from scheduling, image pull, runtime crash, probe failure, misconfiguration, missing dependency, networking, or storage.

Explain the likely root cause first.
Then propose the safest corrective action.
Do not add random manifest changes without verifying the real failure mechanism.
```

## 3. Helm values 设计版
**用途**：改 Helm values 时，防止 AI 只会“改值”，不会看 chart 结构和可维护性。  
**适合**：Helm chart、多环境 values、公共 chart。

```text
Treat this as a Helm design and maintainability task, not just a values edit.

Before changing anything, assess whether the chart structure and values model are clean, scalable, and maintainable across environments.

If the current values pattern is messy or inconsistent, propose a better structure instead of forcing more overrides into a bad layout.
Prefer explicit, predictable, environment-safe chart configuration.
```

## 4. 发布与回滚安全版
**用途**：让 AI 在设计上线变更时兼顾 rollout、回滚和中断风险。  
**适合**：生产上线、灰度发布、Deployment 变更。

```text
Design this Kubernetes rollout like an engineer responsible for production safety.

Consider:
- rollout strategy,
- readiness and liveness impact,
- backward compatibility,
- rollback safety,
- config propagation timing,
- dependency readiness,
- traffic cutover risk.

Do not optimize only for getting the manifest accepted by the cluster.
Prefer a rollout plan that is operationally safe, observable, and reversible.
```

## 5. 资源与稳定性优化版
**用途**：让 AI 评估 requests/limits、HPA、JVM/Python/Node 运行时资源关系。  
**适合**：OOMKilled、CPU 飙高、扩缩容不稳。

```text
Review this workload from a Kubernetes resource and stability perspective.

Do not suggest arbitrary CPU and memory values.
Evaluate the relationship between:
- container runtime behavior,
- requests and limits,
- autoscaling signals,
- startup profile,
- steady-state load,
- eviction and throttling risk.

Recommend a resource strategy that is realistic, stable, and production-safe.
```

## 6. 网络与 Ingress 诊断版
**用途**：Service、Ingress、DNS、跨 namespace 通信异常时用。  
**适合**：访问不通、502、503、超时、路径不匹配。

```text
Analyze this Kubernetes networking issue systematically.

Check the full path:
- client to ingress,
- ingress to service,
- service to endpoints,
- endpoint to pod,
- DNS resolution,
- port mapping,
- protocol assumptions,
- timeout and retry behavior.

Do not stop at the first symptom.
Identify the exact break point in the traffic path and fix that layer properly.
```

## 7. 安全与权限版
**用途**：审 serviceAccount、RBAC、securityContext、secret 使用方式。  
**适合**：权限最小化、安全治理、平台规范。

```text
Review this Kubernetes configuration from a security and least-privilege perspective.

Focus on:
- service accounts,
- RBAC permissions,
- secret exposure,
- pod security context,
- container privileges,
- filesystem access,
- host-level escape risks,
- network exposure.

Challenge insecure defaults and recommend the most professional secure-by-default configuration.
```

## 8. Kubernetes Runbook 编写版
**用途**：让 AI 按运维手册方式写集群变更、排障和恢复步骤。  
**适合**：交接文档、故障处置 SOP、值班手册。

```text
Write this as a Kubernetes operational runbook.

Assume the reader may need to execute it during an incident.
Make it explicit, ordered, and safe.

Include:
- scope,
- prerequisites,
- exact kubectl or Helm steps,
- expected observations,
- verification steps,
- rollback or recovery guidance,
- warnings for risky actions.
```
