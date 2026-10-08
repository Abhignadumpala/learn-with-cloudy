# Learn with Cloudy ☁️

Animated DevOps & cloud explainers, presented by **Cloudy**, a cloud & DevOps guide.
Each topic has voice and captions in **English · తెలుగు · हिन्दी · Español · Português**.

🔗 **Live:** https://abhignadumpala.github.io/learn-with-cloudy/

## Topics

| # | Topic | Live link |
|---|---|---|
| 01 | DNS, step by step | https://abhignadumpala.github.io/learn-with-cloudy/dns/ |

## DNS, step by step
1. What DNS does: a name becomes an IP address
2. A DNS lookup, nearest first: browser cache → OS cache → ISP resolver → root → .store registry → Route 53
3. My domain, managed by Route 53: bought on Namecheap, public hosted zone, 4 AWS nameservers as Custom DNS
4. Records for my 3-tier app: A records + a CNAME, so every server finds the next one by name
5. TTL: why returning visitors can still hit an old IP, and how to avoid it

Plus short notes on what DNS is, why it exists, nslookup, and Route 53 hosted zones.

**Controls:** play bar · ±5 s · step · speed 0.75×–1.5× · mute ·
keys ← / → step, Shift + ← / → 5 s, Space play/pause, M voice, L language, F fullscreen

## Layout
```
index.html      home page with all topics
dns/            DNS explainer (index.html + audio/)
```

Built from my hands-on notes: https://github.com/Abhignadumpala/devops-notes
