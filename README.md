# GitHub CV Template for iA Writer

A professional CV/Resume template (ATS Friendly) for iA Writer that combines the data-dense structure of GitHub with high-end editorial typography. 

This template is designed to be **portable and print-ready**, with fonts embedded directly into the CSS to ensure PDF export on Windows (I have not check macOS, and iOS) without requiring users to install custom fonts manually.

## Design & Typography

This template uses a "Hybrid Editorial" design system:

* **Headings (Name & Sections):** [Lora](https://fonts.google.com/specimen/Lora) (Serif, Bold).
    * *Why?* Adds a touch of human warmth and established authority to your name and section dividers.
* **Body Text & Details:** [Jost](https://fonts.google.com/specimen/Jost) (Sans Serif, Regular & Bold).
    * *Why?* A geometric sans-serif inspired by Futura. It is extremely legible at small sizes, making it perfect for dense bullet points, dates, and contact info.

## Features

* **Embedded Fonts:** Fonts are encoded in Base64 within the CSS, so they work even in "sandboxed" environments (like Windows PDF Export) where linked font files often fail.
* **A4 Print Optimized:** Margins and sizing are pre-set for A4 paper standard.
* **Automatic Formatting:**
    * **H1** is automatically centered for your Name.
    * **H2** creates elegant section dividers with serif typography.
    * **H3** is transformed to UPPERCASE SANS-SERIF for job titles to create visual hierarchy.
    * **H4** is styled as small grey text for dates and locations.

## Installation

1.  Download the latest release (`.zip` file).
2.  **Windows:**
    * Open iA Writer.
    * Go to `File` > `Install Template...`
    * Select the `GitHub CV.iatemplate.zip` file.

## Usage Guide

To get the intended design, structure your Markdown like this:

### 1. The Header
Use a single **H1** (`#`) for your name. The text immediately following it (contact info) will be centered automatically.

```markdown
# Alexander J. Mercer
alex.mercer@example.com | (555) 019-2834 | [linkedin.com/in/mercer](https://linkedin.com/in/mercer)
````

### 2\. Sections

Use **H2** (`##`) for main sections like Experience, Education, or Skills.

```markdown
## Experience
```

### 3\. Job Roles & Companies

  * Use **H3** (`###`) for your Job Title (This becomes UPPERCASE BOLD).
  * Use **H4** (`####`) for the Company, Date, and Location (This becomes small grey text).

<!-- end list -->

```markdown
### Senior Software Architect
#### TechCorp Inc. | Jan 2020 – Present | New York, NY
```

### 4\. Bullet Points

Use standard dashes `-` for your achievements.

```markdown
- Spearheaded the migration to a microservices architecture.
- Reduced server costs by 15% using optimized caching.
```

-----

## PDF Export Settings

For the best results when exporting to PDF:

1.  Select **GitHub CV** as your template in the Preview window.
2.  Go to `File` \> `Print` (or `Export`).
3.  **Paper Size:** A4.
4.  **Margins:** Default (The template handles spacing internally).
5.  **Header/Footer:** Turn **OFF** headers and footers in iA Writer settings to avoid printing page numbers over the design.

## ATS Friendly (Applicant Tracking Systems)

Here is the technical breakdown of why this Markdown-based template is "ATS Friendly," along with one simple test you must do to be 100% sure.

### Why this template works well for ATS

**1. Logical, Linear Hierarchy**
ATS robots read documents from top to bottom, left to right. They get confused by text boxes, sidebars, tables, and floating graphics (common in Canva or Photoshop resumes).
* **This Template:** Is built on **Markdown**, which forces a strict, linear structure.
* **The Code:** It used `<h1>` for your name, `<h2>` for sections like "Experience", and `<h3>` for Job Titles. This maps *perfectly* to the data fields an ATS is looking for. It is the cleanest code structure a robot can ask for.

**2. Standard HTML Tags**
When iA Writer generates the PDF, it uses standard HTML tags (`<ul>`, `<li>`, `<p>`).
* **This Template:** Uses standard bullet points (`<ul>`). ATS parsers are programmed to recognize these lists as "Skills" or "Job Duties."
* **Contrast this:** Many Word templates use "fake" bullet points (special symbols) that confuse robots. This template uses real code.

**3. No "Invisible" Elements**
We styled the layout using CSS (margins, padding), not by using "Tables" or "Text Boxes."
* **Why this matters:** An ATS often ignores text inside a text box. Since this layout is purely CSS-based, the text remains in the main document flow, ensuring 100% of it is read.

### The One Risk: The Fonts (and how to test it)

The only potential "technical" risk is the **Base64 Embedded Fonts** (Lora & Jost).
* **The Risk:** Occasionally, when fonts are embedded this way, the "character mapping" can break. To a human, it looks like "Experience." To a robot, it might look like "E%p@r!ence."

**"Copy-Paste" Test (Do this to be sure!)**
You can verify if your CV is readable in 10 seconds:
1.  Open your final CV **PDF** file.
2.  Select all the text (`Ctrl + A`).
3.  Copy it (`Ctrl + C`).
4.  Paste it (`Ctrl + V`) into a plain text file (like Notepad).

* **If the text looks perfect in Notepad:** Congratulations! Your CV is **100% ATS readable**. The fonts are encoding correctly.
* **If the text looks like garbage symbols:** The Base64 encoding is masking the characters. You should revert to "System Fonts" (Arial/Georgia) for the safest result.

### Summary
* **Structure:** ⭐⭐⭐⭐⭐ (Markdown is perfect for hierarchy)
* **Layout:** ⭐⭐⭐⭐⭐ (No tables or text boxes to confuse the bot)
* **Readability:** ⭐⭐⭐⭐ (High, provided the Copy-Paste test passes)

**Advice:** For 99% of modern tech companies (Google, Amazon, Startups), this PDF will work perfectly. If you are applying to a very old-fashioned institution (like a government bank) that specifically asks for a `.docx` file, you should use iA Writer's **File > Export > Microsoft Word** option instead of the PDF, just to be safe.

## Credits

  * Based on the original [GitHub Template](https://github.com/iainc/iA-Writer-Templates) by iA Inc.
  * Fonts via [Google Fonts](https://fonts.google.com) (Lora & Jost).
  * Customized for CV/Resume formatting.

<!-- end list -->

```
```