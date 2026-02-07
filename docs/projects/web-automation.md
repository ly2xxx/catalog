# 🌐 Web Automation & Browser Tools

Browser automation, web scraping, and content extraction tools powered by Playwright.

**Total Projects:** 3 | **Stars:** 1

---

## 🚀 Featured Projects

### [grabit](https://github.com/ly2xxx/grabit)
**Streamlit-based web content extraction tool**

Beautiful Streamlit application for scraping and processing web pages using Playwright. Extract clean content, screenshots, and structured data from any website.

- **Tech Stack:** Python, Streamlit, Playwright
- **Features:** 
  - Full page screenshots
  - Text content extraction
  - Markdown conversion
  - Interactive UI
  - Batch processing support
- **Status:** 🟢 Active (Updated: 2026-02-05)
- **Use Cases:** Content research, web archiving, data extraction, competitive analysis

---

### [browser-use_poc](https://github.com/ly2xxx/browser-use_poc)
**Browser automation proof-of-concept**

Experiments with browser automation patterns and techniques. Demonstrates advanced Playwright usage for complex web interactions.

- **Tech Stack:** Python, Playwright, Browser automation
- **Features:**
  - Complex navigation workflows
  - Form automation
  - Dynamic content handling
  - Screenshot and PDF generation
- **Status:** 🟡 Stable (Updated: 2025-01-26)
- **Use Cases:** Testing automation, data scraping, workflow automation

---

### [picture-search-poc](https://github.com/ly2xxx/picture-search-poc) ⭐ 1
**Image search proof-of-concept**

Experimental image search and analysis tool. Explores computer vision techniques for finding and categorizing images.

- **Tech Stack:** Python, Computer Vision
- **Features:**
  - Image similarity search
  - Visual analysis
  - Automated categorization
- **Status:** 🔴 Archived (Updated: 2024-04-28)
- **Stars:** ⭐
- **Note:** Completed POC, concept validated

---

## 🔧 Technology Deep Dive

### Playwright Advantages

These projects leverage Playwright for:

- **Cross-browser support** - Chrome, Firefox, Safari
- **Modern web handling** - SPA, dynamic content, lazy loading
- **Rich automation** - Screenshots, PDFs, network interception
- **Headless/headed modes** - Debug visually or run in background

### Common Patterns

1. **Content Extraction:**
   ```python
   # Pattern used in grabit
   page.goto(url)
   content = page.content()
   markdown = html_to_markdown(content)
   ```

2. **Screenshot Capture:**
   ```python
   # Full page screenshots
   page.screenshot(path="output.png", full_page=True)
   ```

3. **Data Scraping:**
   ```python
   # Extract structured data
   data = page.evaluate("() => document.querySelector('.data').innerText")
   ```

---

## 📊 Project Comparison

| Feature | grabit | browser-use_poc | picture-search-poc |
|---------|--------|-----------------|-------------------|
| **UI** | Streamlit Web App | CLI/Script | CLI |
| **Focus** | Content extraction | Automation workflows | Image search |
| **Status** | 🟢 Active | 🟡 Stable | 🔴 Archived |
| **Complexity** | Medium | High | Medium |
| **Best For** | Research, archiving | Testing, workflows | Image analysis |

---

## 🎯 Use Cases

### Content Research
Use **grabit** to extract clean content from articles, blogs, and documentation sites for research or archiving.

### Automation Testing
Use **browser-use_poc** patterns to automate repetitive web testing tasks and validation workflows.

### Image Analysis
Reference **picture-search-poc** for computer vision approaches to image similarity and categorization.

---

## 🚀 Getting Started

### Quick Start with Grabit

```bash
# Clone the repository
git clone https://github.com/ly2xxx/grabit.git
cd grabit

# Install dependencies
pip install -r requirements.txt

# Install Playwright browsers
playwright install

# Run the app
streamlit run app.py
```

Visit `http://localhost:8501` and start extracting web content!

---

## 📚 Learning Resources

- [Playwright Python Docs](https://playwright.dev/python/)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [Web Scraping Best Practices](https://www.scraperapi.com/blog/web-scraping-best-practices/)
- [Playwright Automation Patterns](https://playwright.dev/python/docs/intro)

---

## 🔗 Related Projects

- **AI/ML:** Combine with `ai-pdf-chat` for content Q&A
- **Business Tools:** Use with `mailclerk` for email content extraction
- **Utilities:** Pair with `net-test` for web service monitoring

---

*Updated: 2026-02-07*
