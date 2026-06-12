# Hey, I'm Patrick

Platform & Infrastructure Engineer · Homelab tinkerer · Avid cook

---

## What I do

I build and run infrastructure and automate whatever I can so I don't have to do it twice. At work
that's AWS and GCP. At home I keep it cloud-sovereign — a short list of stuff I actually trust
(Cloudflare, NextDNS, Proton). Full-stack on paper, but I mostly live on the platform side.

Honestly, put me in front of the AWS or GCP console and I'm lost. I only know these clouds through
OpenTofu. If it's not in state, it doesn't exist.

## Tooling

This is the part I actually care about. My [setup](https://gitlab.com/ptrck-sh/setup) and
[dotfiles](https://gitlab.com/ptrck-sh/dotfiles) repos get me the same environment on every machine —
Ansible sets up the box, dotfiles do the shell, and I end up with the same config on the cluster or a
brand new laptop. The fun part is making the tools work together:

- **1Password + mise** — a little script I wrote that pulls secrets at runtime and only gives agents
  the access they need. That's how I let Claude and Codex work with me without handing over real
  access.
- **alint + Renovate + pre-commit** — keeps every repo up to date, not just dependencies but the
  tooling too. Renovate bumps the shared config, alint checks it, pre-commit fixes it. I change
  something once and it shows up everywhere.

So I can open any repo on any machine and everything's already set up.

## Homelab

Two clusters I run (and break now and then):

- **rke2** — an Intel NUC (amd64) running RKE2, does the heavier stuff.
- **berry-stack** — a Raspberry Pi k3s cluster for the small always-on things.

All the state sits on a **TrueNAS** box, off the clusters. An nfs-subdir provisioner gives workloads
storage over NFS (my poor man's EFS), and databases run on ZFS RAID with snapshots so they're always
backed up. Storage stays at home, which keeps it cloud-sovereign and means I can wipe a whole cluster
and not lose anything.

It's all GitOps: GitLab CI builds, Flux reconciles, OpenTofu owns the state.

## Find me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&style=flat-square&logoColor=white)](https://www.linkedin.com/in/patrickpfenning/)
[![GitLab](https://img.shields.io/badge/GitLab-FC6D26?logo=gitlab&style=flat-square&logoColor=white)](https://gitlab.com/ptrck-sh)
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&style=flat-square&logoColor=white)](https://github.com/ppfenning92)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?logo=instagram&style=flat-square&logoColor=white)](https://www.instagram.com/ppfenning92)

## Stack

**Infra & ops**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&style=for-the-badge&logoColor=white)
![OpenTofu](https://img.shields.io/badge/OpenTofu-ffda18?logo=opentofu&style=for-the-badge&logoColor=black)
![Flux CD](https://img.shields.io/badge/Flux_CD-5468FF?logo=flux&style=for-the-badge&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab_CI-FC6D26?logo=gitlab&style=for-the-badge&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?logo=ansible&style=for-the-badge&logoColor=white)
![Podman](https://img.shields.io/badge/Podman-892CA0?logo=podman&style=for-the-badge&logoColor=white)
![Buildah](https://img.shields.io/badge/Buildah-892CA0?style=for-the-badge&logoColor=white)
![Skopeo](https://img.shields.io/badge/Skopeo-1A1A2E?style=for-the-badge&logoColor=white)

**Cloud**

![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonwebservices&style=for-the-badge&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?logo=googlecloud&style=for-the-badge&logoColor=white)

**Development**

![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&style=for-the-badge&logoColor=white)
![Gleam](https://img.shields.io/badge/Gleam-FFAFF3?logo=gleam&style=for-the-badge&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&style=for-the-badge&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&style=for-the-badge&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&style=for-the-badge&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?logo=gnubash&style=for-the-badge&logoColor=white)
