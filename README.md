# 📊 GLAD-MHG Implementation Dashboard

This repository hosts the live, interactive **GLAD-MHG Implementation & Site Integration Roadmap**. The page is automatically built and served using GitHub Pages.

🔗 **Live Dashboard URL:** [Insert your GitHub Pages link here]

---

## ⚙️ How it Works

The dashboard is built using a decoupled architecture to keep updates simple:
1. **`index.html` (The Engine):** Contains the layout, styling (Tailwind CSS), and core logic. It automatically handles structural UI changes and color states.
2. **`data.json` (The Database):** A clean text file containing only the raw roadmap data. 

Every time the page loads, the system loops through `data.json`, dynamically builds the status cards, and **mathematically calculates the overall "Current Readiness" score** based on the average of all individual tasks.

---

## ✏️ How to Update Progress

You do **not** need to touch any HTML or layout code to update this roadmap. You only need to edit `data.json`.

### Step-by-Step Update:
1. Open the `data.json` file in this repository.
2. Click the **edit icon (pencil)** on GitHub.
3. Locate the module you want to change and update its values:
   * **`progress`**: Enter a whole number between `0` and `100`. The visual progress bar, color accents, and overall average widget will recalculate themselves instantly.
   * **`phaseText`**: Update the status string text (e.g., `"PLANNED"`, `"IN REVIEW"`, `"COMPLETE"`).
4. Scroll down, write a short commit message (e.g., *"Updated Speech Questionnaire to 75%"*), and click **Commit changes**.

### Data Schema Reference:
```json
{
  "title": "Task Name Here",
  "subtext": "Brief descriptive subtitle or target goals",
  "progress": 75,
  "phaseText": "CURRENT STAGE LABEL"
}
