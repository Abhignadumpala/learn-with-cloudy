# Learn with Cloudy ☁️

Animated DevOps & cloud explainers, presented by **Cloudy**, a cloud & DevOps guide.
Each topic has voice and captions in **English · తెలుగు · हिन्दी · Español · Português**.

🔗 **Live:** https://abhignadumpala.github.io/learn-with-cloudy/

## Topics

| # | Topic | Live link |
|---|---|---|
| 01 | DNS, step by step | https://abhignadumpala.github.io/learn-with-cloudy/dns/ |
| 02 | From SDLC to DevOps | https://abhignadumpala.github.io/learn-with-cloudy/sdlc/ |
| 03 | Traditional IT vs Cloud vs Terraform | https://abhignadumpala.github.io/learn-with-cloudy/why-terraform/ |
| 04 | Deployment strategies | https://abhignadumpala.github.io/learn-with-cloudy/deployment-strategies/ |
| 05 | Kubernetes scheduling | https://abhignadumpala.github.io/learn-with-cloudy/k8s-scheduling/ |
| 06 | Pod affinity, anti-affinity and topology spread | https://abhignadumpala.github.io/learn-with-cloudy/pod-affinity-spread/ |

## DNS, step by step
1. What DNS does: a name becomes an IP address
2. A DNS lookup, nearest first: browser cache → OS cache → ISP resolver → root → .store registry → Route 53
3. My domain, managed by Route 53: bought on Namecheap, public hosted zone, 4 AWS nameservers as Custom DNS
4. Records for my 3-tier app: A records + a CNAME, so every server finds the next one by name
5. TTL: why returning visitors can still hit an old IP, and how to avoid it

Plus short notes on what DNS is, why it exists, nslookup, and Route 53 hosted zones.

## From SDLC to DevOps
1. SDLC: the 7 steps, with a restaurant food-ordering app as the example
2. Traditional SDLC: a Waterfall project over 12 months (testing in months 8–9, client first sees the app in month 12)
3. Agile: a working feature every month, client feedback each sprint
4. Agile + DevOps: git push → build → test → deploy, through DEV → SIT → UAT → PROD (CI/CD)
5. What DevOps solves: faster releases, fewer defects, automated deploys, high availability, auto scaling, security and cost

Plus short notes on why DevOps exists, stakeholders, SDLC phases, Waterfall vs Agile, environments, and what DevOps adds.

## Traditional IT vs Cloud vs Terraform
1. Traditional IT: one server passes through business, analyst, architect, procurement, network, storage, backup and app teams (weeks to months)
2. Cloud console: rent servers on AWS, Azure or Google Cloud and launch in minutes, but by hand for dev, staging and prod, so servers can differ
3. Terraform: main.tf written once, tfvars per environment, terraform plan → apply, code in Git, many providers
4. Why Terraform: automation, repeatable, version control, fewer mistakes, multi-cloud, cost control
5. Traditional IT vs Cloud vs Terraform side by side: each step removes more manual work

Plus short notes on what Terraform is, why use it, same code for every environment, and the init → plan → apply → destroy workflow.

## Deployment strategies
1. What a deployment strategy is: the plan for how v2 replaces v1, and the 3 things it controls (downtime, blast radius, rollback speed)
2. The 4 types: Recreate, Rolling update, Canary, Blue-green
3. Rolling update live: `kubectl set image` adds one v2 Pod at a time (maxSurge 1, maxUnavailable 0), a bug in v2, then `kubectl rollout undo`
4. Canary live: 10% of users to v2, errors on the canary, rollback by weight 0, then 10% → 50% → 100% after the fix
5. Blue-green live: green next to blue, test on a preview URL, switch the Service selector, then switch back instantly
6. Which one to pick: downtime, who a bug hits, rollback and extra cost side by side

Plus short notes on each strategy and the rollout commands.

## Kubernetes scheduling
1. What scheduling is: the kube-scheduler filters nodes, scores the rest and binds the Pod; no node left → Pending
2. Types of scheduling constraints: nodeSelector and node affinity attract, taints repel, tolerations allow
3. Taints and tolerations live: NoSchedule, a toleration is a permission not a ticket, NoExecute evicts
4. nodeSelector vs node affinity live: exact match and Pending, In [ai, agent], required vs preferred
5. Dedicated node: taint + toleration + nodeSelector together
6. Other Pod placement rules: Pod affinity, anti-affinity, topology spread, nodeName

## Pod affinity, anti-affinity and topology spread
1. topologyKey: hostname = one node, zone = one Availability Zone
2. Pod affinity live: cart Pods next to redis, same node vs same zone, required vs preferred
3. Pod anti-affinity live: frontend replicas on different nodes, node failure, required by zone → Pending
4. Topology spread live: maxSkew 1 across 3 zones (2-2-2, then 3-2-2), a zone goes down, DoNotSchedule vs ScheduleAnyway
5. Which rule to use

**Controls:** play bar · ±5 s · step · speed 0.75×–1.5× · mute ·
keys ← / → step, Shift + ← / → 5 s, Space play/pause, M voice, L language, F fullscreen

## Layout
```
index.html      home page with all topics
dns/            DNS explainer (index.html + audio/)
sdlc/           SDLC to DevOps explainer (index.html + audio/)
why-terraform/  Traditional IT vs Cloud vs Terraform explainer (index.html + audio/)
deployment-strategies/  Deployment strategies explainer (index.html + audio/)
k8s-scheduling/  Kubernetes scheduling explainer (index.html + audio/)
pod-affinity-spread/  Pod affinity, anti-affinity and topology spread explainer (index.html + audio/)
```

Built from my hands-on notes: https://github.com/Abhignadumpala/devops-notes
