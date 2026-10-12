# DevOps Collaboration Lab

Welcome to the **DevOps Collaboration and Workflow Practice Repository**. This repository is created for our university DevOps course lab to practice modern version control workflows, team collaboration strategies, and continuous integration foundations using **Git** and **GitHub**.

---

## 👥 Team Members & Roles

| Member Name | GitHub Username | Assigned Lab Role |
| :--- | :--- | :--- |
| **Haseeb Tariq** | [@haseeb-ml-engineer](https://github.com) | Repo Manager |
| *Sharjeel Ikhlaq* | [@Sharjeel Ikhlaq](#) | QA Engineer |


---

## 🎯 Learning & Practice Objectives

Our team is utilizing this project workspace to master the following industry-standard core practices:
* **Branching Strategies:** Implementing standard Git feature-branch workflows without touching the stable production code.
* **Pull Request (PR) Reviews:** Practicing mandatory peer reviews, handling code changes, and approving branch mergers.
* **Merge Conflict Resolution:** Safely handling overlapping code changes locally before syncing with the remote server.
* **DevOps Best Practices:** Writing clean commit logs, tracking documentation updates, and standardizing folder directories.

---

## 🌿 Our Branching Policy (Git Flow)

To keep our project stable and avoid breaking each other's code, we strictly enforce this branch layout:
* **`main`**: Production-ready, stable codebase. Direct pushes to `main` are strictly locked!
* **`development`**: Integration branch where all completed team features are brought together for deployment testing.
* **`feature/xxx`**: Temporary working branches created by individual team members for explicit tasks (e.g., `feature/lab1-setup`, `feature/bugfix-config`).

---

## 🛠️ Step-by-Step Contribution Workflow

To collaborate successfully without overriding your team member's progress, always execute changes through these steps:

### 1. Synchronize Your Local Computer
Before starting any new work, update your local computer with the latest cloud code:
```bash
git checkout development
git pull origin development
```

### 2. Isolate Your Work on a New Feature Branch
Create a descriptive local branch and switch to it instantly:
```bash
git checkout -b feature/your-feature-name
```

### 3. Stage and Record Your Milestones
Save clean, granular snapshots of your progress locally:
```bash
git add .
git commit -m "feat: implement baseline configuration profile for lab exercise"
```

### 4. Upload Code to GitHub & Request Review
Push your feature branch to the remote host and open a **Pull Request** targeting the `development` branch:
```bash
git push -u origin feature/your-feature-name
```
*⚠️ **Rule:** Do not merge your own Pull Request! Tag a teammate to review and approve your submission.*

---

## 🚦 Resolving Merge Conflicts Smoothly

If Git blocks your merge due to conflicting changes on the same line, resolve it locally in your terminal:
1. Ensure your local environment is up-to-date:
   ```bash
   git checkout development
   git pull origin development
   ```
2. Switch back to your feature branch and pull the updates directly into it:
   ```bash
   git checkout feature/your-feature-name
   git merge development
   ```
3. Open the flagged files in your editor, choose the correct lines of code, remove the `<<<<<<<` and `>>>>>>>` markers, then save:
   ```bash
   git add .
   git commit -m "fix: resolve merge conflict with development branch updates"
   git push origin feature/your-feature-name
   ```

---

## 📁 Repository Structure
```text
├── .github/             # GitHub workflow automation policies
├── documentation/       # Assignment guidelines and lab manuals
├── exercises/          # Source scripts and code configurations
└── README.md            # Repository overview and collaboration rules
```
