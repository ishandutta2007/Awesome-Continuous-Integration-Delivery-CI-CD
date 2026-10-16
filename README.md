# Awesome-Continuous-Integration-Delivery-CI-CD

## Top Continuous Integration & Delivery (CI/CD) Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Pipeline Orchestration, Container-Native Builds & GitOps Automation*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Continuous Integration & Delivery (CI/CD)**. These tools enable development teams to automate build, test, and deployment workflows—from cloud-managed runners with instant startup to self-hosted, container-native platforms that give you full control over your infrastructure and data.



**Examples** include CircleCI, GitLab CI/CD, GitHub Actions, Bitbucket Pipelines, Jenkins, TeamCity, Travis CI, Azure Pipelines, Harness, and AWS CodePipeline (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, container-native pipelines, and open build infrastructure—ideal for platform engineers, DevOps teams, and organizations seeking transparent, vendor-independent CI/CD.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **GitHub Actions**  

  CI/CD integrated directly into GitHub. Features **matrix builds**, **reusable workflows**, and **2,000+ marketplace actions**. Free minutes for public repos and generous free tier for private repos. **The most accessible CI/CD for open-source and GitHub-centric teams.**



- **GitLab CI/CD**  

  Fully integrated DevOps platform with **built-in CI/CD**, **Auto DevOps**, and **review apps**. Features **DAG pipelines**, **multi-project pipelines**, and **security scanning**. **The most complete single-platform DevOps experience.**



- **CircleCI**  

  Cloud-native CI/CD with **fast container-based builds**, **orb ecosystem**, and **test splitting**. Features **Docker layer caching** and **SSH debugging**.



- **Bitbucket Pipelines**  

  CI/CD integrated into Bitbucket Cloud. Features **configuration-as-code** via `bitbucket-pipelines.yml`, **Pipes marketplace**, and **deployment environments**.



- **TeamCity Cloud**  

  JetBrains' CI/CD platform with **Kotlin DSL for pipeline-as-code**, **test intelligence**, and **parallel builds**. Features **integration with JetBrains IDEs**.



- **Travis CI**  

  The original cloud CI for open source. Features **simple YAML configuration** and **language-specific build environments**.



- **Azure Pipelines**  

  Microsoft's CI/CD service with **YAML pipelines**, **multi-stage deployments**, and **integration with Azure DevOps**. Features **hosted and self-hosted agents**.



- **Harness**  

  Modern CI/CD platform with **AI-powered test intelligence**, **feature flags**, and **cloud cost management**. Features **GitOps** and **pipeline-as-code**.



- **AWS CodePipeline**  

  Fully managed CI/CD service on AWS. Features **integration with CodeBuild, CodeDeploy, and CodeCommit**, plus **third-party integrations**.



## Open-Source GitHub Projects



- **[Jenkins](https://github.com/jenkinsci/jenkins)**  

  **The most widely deployed open-source CI/CD server** (MIT) . **28% adoption rate in 2026—second only to GitHub Actions**  . **The premier choice for teams needing "full control over infrastructure and data"** —critical for **strict security and compliance** where sensitive data cannot leave private infrastructure  . **Key strengths**: **universal integration** with almost any tool, **bespoke workflows** via thousands of plugins, **resilience in complex/legacy environments**, and **no licensing fees**  . **Pipeline-as-code** via Jenkinsfile keeps it compatible with GitOps practices  . **Trade-off**: **requires more operational effort** than managed services—it assumes teams are willing to invest in operating and maintaining their setup  . **The reference implementation for self-hosted CI/CD** .



- **[Tekton Pipelines](https://github.com/tektoncd/pipeline)**  

  **Kubernetes-native CI/CD framework** (Apache-2.0) . **The cloud-native standard for CI/CD on Kubernetes**—**v1.15.0 is an LTS release supported until July 2027**  . **Recent additions**: **end-to-end OpenTelemetry tracing** throughout the reconciliation lifecycle, **configurable Git resolver backoff** for flaky connectivity, **grace periods for transient container errors**, and **resolution reliability fixes** including stuck PipelineRuns requeuing  . **v1.16.0** enables **restricted security contexts by default** for Tekton-injected containers—**secure by default**  . **v1.17.0** surfaces **Pod infrastructure failures on TaskRun status** (FailedMount, FailedScheduling, FailedCreatePodSandBox) and closes a **Windows script-injection gap**  . **Best for**: teams already running Kubernetes who want pipelines as native Kubernetes resources .



- **[Argo Workflows](https://github.com/argoproj/argo-workflows)**  

  **Container-native workflow engine for orchestrating parallel jobs on Kubernetes** (Apache-2.0) . **The most widely adopted Kubernetes workflow engine**—**v4.1.4** is the latest stable release with **v4.0.12** also supported  . **Release cadence**: **new minor versions roughly every 6 months**, **patch releases every 2 weeks**  . **Security posture**: **10/10 SAST score**, **signed release artifacts**, **security policy file detected**  . **Note**: **branch protection is not maximal** (3/10) and **release artifacts lack provenance attestation**  . **Best for**: ML pipeline orchestration, batch processing, and DAG-based workflows on Kubernetes .



- **[Dagger](https://github.com/dagger/dagger)**  

  **Programmable CI/CD pipelines as code** (Apache-2.0) . **The most innovative approach to CI/CD**—founded in **2018 by Docker co-founder Solomon Hykes**  . **Replaces artisanal scripts with a modern API and cross-language scripting engine**—encapsulate all project tasks and workflows into **Dagger Functions** written in your programming language of choice  . **Run Dagger Functions from CLI, language interpreter, or custom HTTP client**  . **Package functions into modules for reuse across projects**—**all Dagger modules can reuse each other's functions regardless of language**  . **Dagger Cloud** provides visibility across pre-push and post-push pipelines  . **Funding**: **$30.39M total** (Series A) with investors including **Y Combinator, Redpoint Ventures, and Ellen Pao**  . **Best for**: teams wanting containerized, portable, and programmable pipelines that run identically locally and in CI .



- **[Concourse CI](https://github.com/concourse/concourse)**  

  **Container-based automation system written in Go** (Apache-2.0) . **The most mature container-native CI**—**actively maintained** with **30 commits and 21 issue activities in the last 90 days**  . **v8.0.0** (January 2026) changes **default container runtime to containerd**, **always enables secret redaction**, and **makes instance pipelines and `across` steps stable**  . **Security improvement**: **switched from MD5 to SHA256 for resource version digests**—critical for environments where MD5 is not allowed  . **Note**: **v8 migration requires ~5 minutes on a 4 vCPU/5GB Postgres instance**  . **Best for**: teams wanting a container-first CI with a unique pipeline model and no reliance on external plugins .



- **[Woodpecker CI](https://github.com/woodpecker-ci/woodpecker)**  

  **Community fork of Drone CI** (Apache-2.0) . **The actively maintained Drone alternative**—**forked from Drone 0.8 in 2019** after Drone's license changed from Apache 2.0 to a proprietary license  . **The 3.0 release** broke backward compatibility with Drone to **address design issues**, **removed trusted-mode flag** in favor of per-workflow trusted settings, **tightened secret exposure rules for PR builds**, and **reworked agent protocol to use gRPC with stronger authentication**  . **Security posture**: **critical issues patched within a week of disclosure**—"meaningfully better than unmaintained Drone OSS"  . **Secret model**: **repository-scoped with per-secret flags**; **3.0 requires secrets exposed to PRs to be explicitly "plugin-only"**  . **Best for**: homelab operators and small teams wanting a Drone-compatible system that still receives updates .



### Additional Strong Open-Source Options



- **[Drone CI](https://github.com/harness/drone)** — **Container-Native, Continuous Delivery Platform** (Polyform Small Business License) . **Note**: **OSS Drone went quiet after the Harness acquisition**—**Woodpecker CI is the active community fork**  . **Best for**: legacy deployments only—migrate to Woodpecker for active development.

- **[Spinnaker](https://github.com/spinnaker/spinnaker)** — Multi-cloud continuous delivery platform (Apache-2.0) . **Netflix's CD platform** for complex deployment pipelines across multiple clouds.

- **[GoCD](https://github.com/gocd/gocd)** — Continuous delivery server (Apache-2.0) . **ThoughtWorks' CD tool** with **value stream mapping** for pipeline visualization.

- **[Buildkite](https://github.com/buildkite/agent)** — Agent for Buildkite's hybrid CI/CD (MIT) . **Run builds on your own infrastructure** with Buildkite's orchestration.

- **[Earthly](https://github.com/earthly/earthly)** — Build automation for the container era (MPL-2.0) . **The modern build tool** combining Dockerfile and Makefile concepts.

- **[GitLab CI](https://gitlab.com/gitlab-org/gitlab-runner)** — Runner for GitLab CI/CD (MIT) . **Self-hosted GitLab runner** for on-premises build infrastructure.

- Community **n8n** workflows for pipeline notification and deployment alerting automation.



**Frameworks for building custom systems**: Combine **Tekton** for Kubernetes-native pipelines with **Argo Workflows** for DAG orchestration, **Dagger** for portable programmable pipelines, **Woodpecker** for lightweight container-native CI, and **Jenkins** for legacy and compliance-heavy environments—creating a comprehensive CI/CD stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- CI/CD platforms handling source code and deployment credentials must follow security best practices, especially when running in shared or multi-tenant environments.

- **Open-source CI/CD is mature and production-ready.** Jenkins holds **28% adoption**—second only to GitHub Actions  . Tekton provides **Kubernetes-native pipelines with LTS support through July 2027**  . Dagger offers **programmable, portable pipelines** from Docker's co-founder  . **These are genuine alternatives to commercial platforms.**

- **Jenkins remains the control-and-compliance choice.** It is the premier option for teams needing **full control over infrastructure and data**—critical for **strict security and compliance** where sensitive data cannot leave private infrastructure  . **The trade-off is operational effort**: Jenkins assumes teams are willing to invest in operating and maintaining their setup  .

- **Tekton is the Kubernetes-native standard.** **v1.15.0 is an LTS release supported until July 2027**  . **Secure by default** in v1.16.0 with restricted security contexts enabled for Tekton-injected containers  . **Clearer failures** in v1.17.0 with Pod infrastructure failures surfaced on TaskRun status  . **Best for**: teams already running Kubernetes who want pipelines as native resources .

- **Dagger represents the "pipeline-as-code" philosophy.** Founded by **Docker co-founder Solomon Hykes**, Dagger replaces artisanal scripts with a modern API and cross-language scripting engine  . **Run the same Dagger Functions locally and in CI**—**no more "works on my machine" for pipelines**  . **Best for**: teams wanting containerized, portable, and programmable pipelines .

- **Drone CI OSS is effectively dead.** The **OSS Drone project went quiet after the Harness acquisition**—**Woodpecker CI is the active community fork**  . **Woodpecker 3.0** addresses inherited security debt with **per-workflow trusted settings**, **stricter PR secret rules**, and **gRPC agent protocol with stronger authentication**  . **Migrate from Drone to Woodpecker for active development.**

- Self-hosted open-source solutions require proper runner isolation, secret management, and ongoing maintenance. **Runner isolation is the critical security boundary**—Docker and Kubernetes runners provide container-level isolation; SSH and Exec runners offer no isolation and should be treated as full host access  .



---



**Made for platform engineers, DevOps teams, and organizations building transparent CI/CD solutions.**  

Let's make Continuous Integration & Delivery more open, data-driven, and container-native.
