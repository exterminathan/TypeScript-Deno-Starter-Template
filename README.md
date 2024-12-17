# Project Setup and Development Guide

This repository is a starter template for developing in TypeScript and HTML/CSS, using the Deno runtime and the Vite JS Build tool. The project is designed to be used with the GitHub Pages/Actions workflow. 

---


## Table of Contents

1. [Installation](#installation)
2. [Setting Up the Project](#setting-up-the-project)
3. [GitHub Setup Instructions](#github-setup-instructions)
4. [Installing Packages](#installing-packages)
5. [Managing Dependencies](#managing-dependencies)
6. [Start Developing!](#start-developing!)

---

## **1. Installation**

To install Deno, follow the official instructions at [https://deno.com/](https://deno.com/) or
[https://github.com/denoland/deno](https://github.com/denoland/deno).

To install Vite, run the following command:
```bash
npm install vite@latest
```

---

## **2. Setting Up the Project**

Make sure Deno is properly installed by running the following command:

```bash
deno --version
```

---

## **3. GitHub Setup Instructions**

### Enabling GitHub Pages

1. Go to your repository settings:  
   **Settings > Pages > Build and Deployment**
2. Set the **Source** to **“GitHub Actions”**.

### Enabling GitHub Actions

1. Navigate to the **Actions** tab in your repository.
2. Click the green button labeled **“Enable Actions”**.

---

## **4. Installing Packages**

To install new packages using Deno, use the following command:

```bash
deno install npm:package-name
```

To verify the installed packages:

```bash
npm list
```

- If any installed packages are marked as **extraneous**, it means they are not referenced in the `package.json` file.

---

## **5. Managing Dependencies**

Dependencies are tracked in two files:

1. **`package.json`** for npm packages
2. **`deno.json`** for the Deno runtime

### Adding a Dependency

**Step 1:** In `package.json`, add the dependency under `"dependencies"`:

```json
"dependencies": {
  /* existing dependencies */
  "package-name": "1.0.0"
}
```

**Step 2:** In `deno.json`, add the dependency under `"imports"`:

```json
"imports": {
  "package-name": "npm:package-name@^1.0.0"
}
```
---

## **6. Start Developing!**
To start the development environment and generate the `deno.lock` file, run:

```bash
deno run dev
```

