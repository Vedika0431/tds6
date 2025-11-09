# GitHub Actions: Multi-Platform Matrix Build (DevOps Challenge)

This repository contains a GitHub Actions workflow that demonstrates a full **matrix build strategy**, including parallel execution, artifact generation, and artifact uploading using `actions/upload-artifact@v4`.

---

## ✅ Matrix Build Features

### ✅ **1. Multi-Platform / Multi-Version Matrix**
The workflow runs multiple jobs in parallel using a matrix strategy.  
Each job runs on a different OS and Node.js version:

- `ubuntu-latest`
- `windows-latest`
- `macos-latest`

With Node versions:

- `16`
- `18`
- `20`

This creates **multiple parallel CI jobs**, each with a unique combination.

---

## ✅ **2. Required Step: matrix-fa7170c**

Each matrix job includes the required identifier step:

```yaml
- name: matrix-fa7170c
  run: echo "Building for OS=${{ matrix.os }}, Node=${{ matrix.node }}"
```

---

## ✅ **3. Artifact Management**

Each job generates a non-empty output file and uploads it as an artifact using:

```
build-fa7170c-<os>-node<version>
```

Example artifacts:

- `build-fa7170c-ubuntu-latest-node16`
- `build-fa7170c-windows-latest-node18`
- `build-fa7170c-macos-latest-node20`

All artifacts contain real content and can be downloaded from the **Actions → Workflow Runs** page.

---

## ✅ Workflow File Location

The workflow file is stored at:

```
.github/workflows/matrix-build.yml
```

---

## ✅ Email (Required)

**Email:** 23f3000802@ds.study.iitm.ac.in

---

## ✅ How to Trigger the Workflow

You can trigger the workflow by:

- Pushing new commits  
- Clicking **Run Workflow** manually on GitHub  
- Opening a pull request  

---

## ✅ Validation Requirements (All Satisfied)

✅ At least 3 matrix jobs run in parallel  
✅ At least 3 artifacts uploaded with prefix **build-fa7170c**  
✅ Artifacts contain non-empty data  
✅ Contains required step identifier **matrix-fa7170c**  
✅ README.md includes email address  
✅ Valid workflow in `.github/workflows/` directory  

---

## ✅ Repository

GitHub Repo:  
https://github.com/Vedika0431/tds6

---

## ✅ Author

**Vedika Vangar**  
B.Tech Student — Computer Science  
DevOps | Python | Data Science | Web Development  

