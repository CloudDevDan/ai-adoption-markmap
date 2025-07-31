# 🗺️ Dan’s Microsoft AI Adoption Markmap

Welcome to **Dan’s Microsoft AI Adoption Markmap** - a structured, visual reference built on top of Microsoft's official [AI Adoption Scenario](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/ai/) within the [Azure Cloud Adoption Framework (CAF)](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/).

This project helps you visualise how to plan, build, govern, and operate AI solutions using Microsoft technologies – including Azure OpenAI, Copilot, and traditional machine learning workloads. Whether you're a startup testing AI for the first time or an enterprise scaling AI across departments, this map is designed to bring clarity and structure to your journey.

This resource is built using [**Markmap**](https://markmap.js.org/), a JavaScript-powered tool that turns Markdown lists into **interactive mind maps**. The result is a dynamic, explorable way to understand and organize terminology across a broad AI landscape - from foundational learning paradigms to Microsoft-specific AI services.

<a href="https://ai-adoption.daniel.mcloughlin.cloud/" target="_blank">
  <img src="https://img.shields.io/badge/View%20The%20Interactive%20Map-Live-blue?style=for-the-badge" alt="View the Interactive Map" />
</a>

---

## 🌐 Related Projects

Explore my other related projects:

- [🗺️ Dan’s Azure CAF Markmap](https://github.com/CloudDevDan/azure-caf-markmap)
- [🗺️ Dan’s Azure WAF Markmap](https://github.com/CloudDevDan/azure-waf-markmap)
- [🗺️ Dan’s Microsoft App Modernization Framework Markmap](https://github.com/CloudDevDan/app-modernization-markmap)
- [🧠 Dan’s AI Terminology Tracker](https://github.com/CloudDevDan/dans-ai-terminology-tracker)
- [☁️ Dan’s Blog](https://daniel.mcloughlin.cloud/)
- [☁️ Beginner To Builder with Azure AI Foundry](https://daniel.mcloughlin.cloud/series/azureai)

---

## 🔍 What Is Microsoft AI Adoption (CAF)?

The **Microsoft AI Adoption** framework is a scenario within CAF that helps organisations adopt AI responsibly and effectively by following a set of six repeatable phases:

- 🎯 **AI Strategy**
- 📅 **AI Plan**
- 🛠 **AI Ready**
- 🧭 **Govern AI**
- ⚙️ **Manage AI**
- 🛡 **Secure AI**

Each phase provides guidance tailored to both startups and enterprises, along with checklists, best practices, and platform recommendations.

You can explore all checklist items and architecture options via this visual Markmap.

<!-- ---

## 📚 Further Reading
If you're looking to better understand why the Azure Cloud Adoption Framework matters and how it fits into the broader cloud transformation journey, check out this article from the Azure Architecture team:

👉 [Why you need a Cloud Adoption Framework (CAF)... and probably a WAF too](https://techcommunity.microsoft.com/blog/azurearchitectureblog/why-you-need-a-cloud-adoption-framework-caf-and-probably-a-waf-too/3667426)
> Published on Microsoft Tech Community

This piece provides insight into how CAF supports structure and accountability in cloud journeys - and why governance (and sometimes a "WAF") shouldn't be an afterthought. -->

---

## 🎯 About This Project

I've built this project because I'm a visual learner, and while the Microsoft documentation for the Azure Cloud Adoption Framework (CAF) is excellent and comprehensive, the sheer volume of information can be overwhelming. Visualising the framework in an interactive map helps me better understand the structure, flow, and relationships between its components.

By making this project open, I hope others can benefit from this format too - whether you're just beginning your cloud journey or looking for a clearer way to communicate CAF principles to your team.

> Note: All content and links are accurate as of **31 July 2025**. I’ll review and update periodically - pull requests are welcome!

> **Disclaimer:** This project is not affiliated with or endorsed by Microsoft. All content and intellectual property referenced belong to Microsoft. I'm simply building a free and useful visual tool around the excellent work they've already done.

---

### Screenshots
<p align="center">
  <img src="./img/overview.png" alt="Tracker Screenshot" width="800" />
</p>
<p align="center">
  <img src="./img/expanded.png" alt="Tracker Screenshot - Expanded Nodes" width="800" />
</p>

---

## 🧠 What You'll Find

- A fully interactive [Markmap](https://markmap.js.org) of Microsoft’s AI adoption lifecycle
- Checklist-driven structure from official Learn documentation
- Startup and enterprise guidance side-by-side
- Links to governance, security, and operations practices
- Integration of both Azure-native and Copilot-based AI models
  
---

## 📈 Visual Format

All terminology is structured in a Markdown file, which is rendered visually using **Markmap**.

You can:
- View it interactively in the browser
- Navigate through the hierarchy
- Expand/collapse terms as needed

---

## 🤝 Community Contributions

Feel free to:
- Suggest new terms or definitions
- Submit pull requests for corrections or additions
- Help grow the visual map

---

## 🪪 License

This project is licensed under the **MIT License** - you're free to use, share, remix, and build upon it, as long as attribution is given.

--- 

## 🛠 How It's Built

This project uses [Markmap](https://markmap.js.org) to convert a Markdown list into an interactive mind map.  
After exporting the map, a custom **post-processing script** applies visual enhancements including:

- Dark mode theme
- Custom font and header
- White text and dark background for readability
- A favicon
- Branding and blog link

---

## ⚙️ Setup Instructions

Install the Markmap CLI (if not already installed):

```bash
npm install -g markmap-cli
```

Then run this command from the root of the repo:

```bash
npx markmap-cli markmap.md -o ./docs/index.html --no-open && node postprocess-map.js
```

This generates the visual map and applies styling in one go.

---

## 🔗 Link Checker

This project includes a `check-links.js` script that scans all external links in `markmap.md` to:

- Identify broken or redirected URLs
- Report any issues in a dedicated `broken-links.log` file
- Help maintain high-quality, up-to-date reference links for learners

### ✅ Why this exists:
Because this tracker is intended to be long-lived and reliable, it's important to regularly check that:
- All links point to official and active sources (e.g., Microsoft Learn, Wikipedia, GitHub)
- There are no outdated, redirected, or dead references in the mind map

### ▶️ How to run it:

```bash
node check-links.js
```

This will:
- Output results to the terminal (with ✅ and ❌ indicators)
- Write any issues to `broken-links.log` for review
- Automatically clear the log if no issues are found

---

## 🌐 Why the `/docs` Folder?

The `docs` folder is used because GitHub Pages has been configured to serve static content from it.  
The `index.html` is published at:

📍 `https://clouddevdan.github.io/azure-caf-markmap/index.html`