---
sidebar_position: 1
---

# High Performance Computing

Let's discover **High Performance Computing in less than 10 minutes**.

## Getting Started

**High Performance Computing (HPC)** refers to the use of advanced computing technologies to solve complex problems that require significant computational power. HPC systems typically consist of large clusters of computers, each with multiple processors or cores, interconnected by high-speed networks. These systems are designed to perform calculations and data analysis tasks at a much faster rate than traditional computing systems.

HPC is used in a wide range of fields, including scientific research, engineering, finance, and healthcare. It allows researchers and analysts to run simulations, model complex systems, and analyze large amounts of data quickly and efficiently. HPC is particularly important for applications that require large-scale data analysis, such as weather forecasting, gene sequencing, and drug discovery.

To take advantage of HPC systems, applications must be designed to run in parallel, meaning that they can be divided into smaller tasks that can be processed simultaneously on different processors. HPC systems also require specialized software, including programming languages and libraries that are optimized for high-performance computing..

**Learn more** on **[HPC](https://en.wikipedia.org/wiki/High-performance_computing)**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 16.14 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.

## Generate a new site

Generate a new Docusaurus site using the **classic template**.

The classic template will automatically be added to your project after you run the command:

```bash
npm init docusaurus@latest my-website classic
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

The command also installs all necessary dependencies you need to run Docusaurus.

## Start your site

Run the development server:

```bash
cd my-website
npm run start
```

The `cd` command changes the directory you're working with. In order to work with your newly created Docusaurus site, you'll need to navigate the terminal there.

The `npm run start` command builds your website locally and serves it through a development server, ready for you to view at http://localhost:3000/.

Open `docs/intro.md` (this page) and edit some lines: the site **reloads automatically** and displays your changes.
