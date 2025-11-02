# DevOps Assignment: Automated GitHub Pages Deployment

[![Update README with Recent Activity](https://github.com/kaigiii/devops-pages-lab/actions/workflows/activity-log.yml/badge.svg)](https://github.com/kaigiii/devops-pages-lab/actions/workflows/activity-log.yml)

This project demonstrates a complete CI/CD pipeline for deploying a static website with auto-generated content using GitHub Pages and GitHub Actions. It fulfills the requirements for the DevOps course assignment, with additional enhancements to achieve an 'O' (Outstanding) level of quality.

---

## 🎯 Project Goal

The primary objective is to build a hands-off, automated system that:
1.  Hosts a personal project site using GitHub Pages.
2.  Dynamically populates the site with recent GitHub activity.
3.  Follows DevOps best practices such as Infrastructure as Code (IaC) and CI/CD.

## ⚙️ How It Works: The Architecture

This project's automation is powered by a single GitHub Actions workflow. The process is as follows:

1.  **Trigger:** The workflow is triggered automatically on a schedule (every 30 minutes) or can be run manually.
2.  **Permissions:** The job is granted `contents: write` permission to allow it to commit changes back to the repository.
3.  **Action Execution:** It utilizes the `jamesgeorge007/github-activity-readme` community action to fetch my latest public activity.
4.  **Automated Commit:** The action automatically updates the `Recent Activity` section within this `README.md` file and commits the changes.
5.  **Deployment:** GitHub Pages detects the change in the `main` branch and uses Jekyll to render the `index.md` file. This file, in turn, includes this README, seamlessly deploying the updated content to the live site.

## 🔧 Challenges & Solutions

During development, a critical workflow failure occurred where the initial action (`TheDanniCraft/activity-log`) was consistently "Unable to resolve".

*   **Problem:** The workflow failed at the setup stage, unable to download the specified action.
*   **Analysis:** After verifying syntax and ruling out simple typos, the issue was likely due to a runner cache problem or an intermittent issue with the action's hosting.
*   **Solution:** Instead of remaining blocked, I pivoted to a more robust and widely-used alternative, `jamesgeorge007/github-activity-readme`. This change immediately resolved the issue and demonstrated a key DevOps principle: **flexibility and the ability to adapt tooling to achieve the desired outcome.**

## ⭐ Enhancements for O-Level Grade

To exceed the standard requirements, the following enhancements were implemented:

*   **Professional Theming:** Applied the 'Cayman' Jekyll theme to the GitHub Pages site for a clean, professional, and responsive user interface.
*   **Dynamic Status Badge:** Integrated a workflow status badge at the top of this README, providing instant visual feedback on the health of the CI/CD pipeline.
*   **In-depth Documentation:** This README serves as comprehensive documentation, explaining the project's architecture, challenges, and solutions, making it transparent and easy to understand.

---

## 🚀 Recent Activity

<!--START_SECTION:activity-->
<!--END_SECTION:activity-->
