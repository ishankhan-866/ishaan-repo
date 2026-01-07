
# 📘 Standard Operating Procedure (SOP)
## Git Branching Strategy

![Git Branching Strategy Diagram](./images/git-branching-strategy.png)

---

### **Document Information**

| Field            | Details                  |
|------------------|--------------------------|
| **Author**       | Your Name Here           |
| **Version**      | 1.0                      |
| **Last Updated** | YYYY-MM-DD               |
| **Approved By**  | Engineering Lead         |

---

## 1. 🎯 Purpose

The purpose of this SOP is to define a **standard Git branching strategy** that ensures:
- Code stability
- Parallel development
- Easy collaboration
- Controlled releases
- Faster bug fixes

---

## 2. 📌 Scope

This SOP applies to:
- All developers
- QA engineers
- DevOps teams
- Any project using Git for version control

---

## 3. 🧱 Branching Model Overview

We follow a **Git-based branching model** consisting of the following branch types:


---

## 4. 🌿 Branch Types & Rules

### 4.1 `main` Branch
- Represents **production-ready code**
- Always stable and deployable
- Protected branch (no direct commits)

✅ **Allowed Actions**
- Merge from `develop`
- Emergency hotfix merges

❌ **Not Allowed**
- Direct commits
- Feature development

---

### 4.2 `develop` Branch
- Integration branch for all completed features
- Base branch for feature development

✅ **Allowed Actions**
- Merge feature branches
- Merge bugfix branches

---

### 4.3 `feature/*` Branch
- Used for new features or enhancements

**Naming Convention:**

**Rules:**
- Created from `develop`
- Merged back into `develop`
- Deleted after merge

---

### 4.4 `bugfix/*` Branch
- Used for fixing bugs found during development or testing

**Naming Convention:**

---

### 4.5 `hotfix/*` Branch
- Used for **critical production issues**

**Rules:**
- Created from `main`
- Merged into both `main` and `develop`

**Example:**

---

## 5. 🔀 Merge Strategy

| Branch Type | Merge Method        |
|------------|---------------------|
| Feature     | Squash & Merge      |
| Bugfix      | Squash & Merge      |
| Hotfix      | Merge Commit        |
| Develop → Main | Merge Commit |

---

## 6. 🧪 Code Review & Quality Checks

Before merging:
- ✅ Minimum **1–2 code reviewers**
- ✅ All CI checks must pass
- ✅ No unresolved comments
- ✅ Code follows style guidelines

---

## 7. 🏷️ Versioning & Releases

- Follow **Semantic Versioning**:  
  `MAJOR.MINOR.PATCH`
- Tag releases on the `main` branch

**Example:**

---

## 8. 🚀 Deployment Flow

1. Features merged into `develop`
2. QA testing on staging
3. `develop` merged into `main`
4. Release tagged
5. Production deployment

---

## 9. 🔐 Branch Protection Rules

- `main` and `develop` must be protected
- Require pull requests
- Require passing status checks
- Disable force push

---

## 10. 📎 References

- Git Documentation
- Internal Engineering Guidelines
- CI/CD Pipeline Documentation

---

## 11. ✍️ Change History

| Version | Date       | Description           | Author       |
|--------|------------|----------------------|--------------|
| 1.0    | YYYY-MM-DD | Initial version       | Your Name   |

---

> 📢 **Note:** This SOP must be reviewed quarterly and updated as needed.
