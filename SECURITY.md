# Security Policy

🔒 We will do our best _to our knowledge_ to provide maximum security when you're
using our open-sourced projects.

**If you are looking for just reporting an issue process, [move quickly to
reporting](#reporting) section**.

---

## Static Application Security Testing

⚙️ We are using the following SAST tools/services in our projects to maintain the
security aspect:

| Tool / Service | Purpose                                                                                                                   | Usage                                                                                                     |
| -------------- | ------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [DeepScan]     | Analyze JavaScript projects which targets runtime errors and quality issues.                                              | Installed [`GitHub Apps`*] - [DeepScan app]                                                               |
| [GitGuardian]  | Scan source code to detect API keys, passwords, certificates, encryption keys and other sensitive data.                   | Installed [`Github Apps`*] - [GitGuardian app]; [`GitHub Actions`*] workflows: [`ci-cd`*], [`scheduled`*] |
| [Snyk]         | Vulnerability scanner for project codebase.                                                                               | Installed [`Github Apps`*] - [Snyk app]; [`GitHub Actions`*] workflows: [`ci-cd`*], [`scheduled`*]        |

[deepscan]: https://deepscan.io
[deepscan app]: https://github.com/marketplace/deepscan
[gitguardian]: https://www.gitguardian.com/
[gitguardian app]: https://github.com/marketplace/gitguardian
[snyk]: https://snyk.io
[snyk app]: https://github.com/marketplace/snyk

## Dependency management

In order to ensure that our project depedencies stay up to date and are secure,
we use the following tools/services:

| Tool/service   | Purpose                                                             | Usage                                           |
| -------------- | ------------------------------------------------------------------- | ----------------------------------------------- |
| [Deadpendency] | Automated checks on projects dependencies remain healthy over time. | Installed [`GitHub Apps`*] - [Deadpendency app] |
| [Renovate]     | Automated dependencies updates in projects.                         | Installed [`GitHub Apps`*] - [Renovate app]     |

[deadpendency]: https://deadpendency.com
[deadpendency app]: https://github.com/marketplace/deadpendency
[renovate]: https://www.whitesourcesoftware.com/free-developer-tools/renovate/
[renovate app]: https://github.com/marketplace/renovate

### Annotations

[`github actions`*]: #github-actions
[`github apps`*]: #github-apps
[`ci-cd`*]: #continuous-integration-and-delivery
[`scheduled`*]: #scheduled

#### Github Actions

It is configured with [GitHub Actions] workflows inside the public repositories
of [our GitHub organisation] - in the directory `./.github/workflows`.

[github actions]: https://docs.github.com/en/actions
[our github organisation]: https://github.com/adchitects

##### Continuous Integration and Delivery

It is configured in `./.github/workflows/ci-cd.yml` workflow file.\
**It runs on every push or pull request action to the `main` branch.**

##### Scheduled

It is configured in `./.github/workflows/scheduled.yml` workflow file.\
**It runs on the `main` branch, on specified period** _(not longer than
once a week)_.

#### Github Apps

The application is installed within our organisation with access to our public
repositories.\
**It runs on every push or pull request.**

---

## Reporting

📟 If you have found a security issue or have any concerns or doubts regarding
privacy rights, please get in touch with us.\
There are possible options _(the first one is recommended)_:

1. **Create GitHub's Security Advisory** in the specific project repository
   where the security issue exists _(in the `Security` tab/pane)_.
1. Traditionally, via email: dev@adchitects.co.

⚠️ We are all ears, but please, **DO NOT create a GitHub issue for reporting a
vulnerability**.

### Vulnerability report process

1. 🗓️ **Our team should acknowledge your report within 7 days** 
1. 🕵️ The team will investigate and update the issue with relevant information.

    1. ❌ If the team **does NOT confirm the report**, no further action will
       be taken by us. We will be sure to inform you regarding this result.
    1. ✅ If the team **confirms the report**, the team will take action to fix
       it immediately:
        1. Commits will be handled in a private repository for review and testing.
        1. Release a new patch version from the private repository.
        1. Write an announcement post disclosing the vulnerability.
