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

**Controls:** play bar · ±5 s · step · speed 0.75×–1.5× · mute ·
keys ← / → step, Shift + ← / → 5 s, Space play/pause, M voice, L language, F fullscreen

## Layout
```
index.html      home page with all topics
dns/            DNS explainer (index.html + audio/)
sdlc/           SDLC to DevOps explainer (index.html + audio/)
why-terraform/  Traditional IT vs Cloud vs Terraform explainer (index.html + audio/)
```

Built from my hands-on notes: https://github.com/Abhignadumpala/devops-notes
