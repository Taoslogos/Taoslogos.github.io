# taos.dev — Personal Portfolio & Blog

Welcome to the repository for my personal website and blog. This project serves as a minimal, high-performance, and responsive portfolio showcasing what I'm learning, building, and exploring across electronics engineering, software development, AI, and cybersecurity.

🌐 **Live Site:** [https://taoslogos.github.io](https://taoslogos.github.io)

---

## 🚀 Overview & Philosophy

The site is designed with an **offline-first, zero-database, and zero-framework** philosophy. 
* **Pure Client-Side:** Everything runs inside a single, highly optimized `index.html` file.
* **No Build Step:** Markdown files are parsed dynamically in the browser using `marked.js`.
* **Lightweight UI:** Icons are loaded on-demand via the Iconify API framework, keeping the initial bundle incredibly small.
* **Multi-Theme Engine:** Includes customized `Dark`, `Light`, and `Terminal` (matrix-style hackerspace) themes utilizing raw CSS variables.

---

## 🛠️ Tech Stack

* **Frontend:** Vanilla HTML5, Semantic CSS3, JavaScript (ES6+)
* **Markdown Parser:** [marked.js](https://marked.js.org/) (for rendering blog contents dynamically)
* **Icons:** [Iconify](https://iconify.design/) (Lucide & Logos sets)
* **Fonts:** Inter & JetBrains Mono (via Google Fonts)
* **API Integration:** GitHub REST API (for live-animating profile statistics)

---

## ✍️ How to Add a New Blog Post

Because the blog is completely self-contained, you don't need to touch database configurations or write HTML templates to post an update. 

1. Open `index.html`.
2. Locate the `POSTS` array inside the `<script>` tag.
3. Copy an existing post block object and paste it at the bottom of the array:

```javascript
{
  slug: "your-post-slug",
  title: "Your Descriptive Post Title",
  date: "YYYY-MM-DD",
  tags: ["Tag1", "Tag2"],
  image: "[https://picsum.photos/seed/yourcustomseed/800/600.jpg](https://picsum.photos/seed/yourcustomseed/800/600.jpg)",
  excerpt: "A brief 1-2 sentence hook displayed on the homepage preview card.",
  content: `### Use Standard Markdown Headers

Your blog post text goes here. You can write regular paragraphs, include links, or blockquotes.

\`\`\`python
# Code blocks automatically render with an interactive "Copy" button
def hello_world():
    print("Hello from Taos!")
\`\`\`

The parser handles standard formatting smoothly.`
}
