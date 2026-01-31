# Learning Notes Repository

A structured repository for organizing course notes, concepts, and exercises in markdown format.

## 📚 Active Courses

<!-- Add links to your courses here -->

- [Example Course Name](courses/example-course-name/README.md)

## 📁 Repository Structure

```
ai-ia/
├── courses/                          # All course materials
│   └── {course-name}/               # Individual course folder
│       ├── README.md                # Course overview and index
│       ├── lectures/                # Lecture notes
│       ├── concepts/                # Concept explanations
│       ├── exercises/               # Practice problems and solutions
│       ├── resources/               # Additional materials, links, cheat sheets
│       └── images/                  # Course-specific images and diagrams
├── templates/                       # Markdown templates for notes
│   ├── lecture-notes-template.md
│   ├── concept-notes-template.md
│   ├── exercise-notes-template.md
│   └── course-readme-template.md
└── README.md                        # This file
```

## 🚀 Getting Started

### Creating a New Course

1. Create a new folder in `courses/` with a descriptive name (use lowercase with hyphens):

   ```bash
   mkdir -p courses/your-course-name/{lectures,concepts,exercises,resources,images}
   ```

2. Copy the course README template:

   ```bash
   cp templates/course-readme-template.md courses/your-course-name/README.md
   ```

3. Fill in the course information and update the [Active Courses](#-active-courses) section above

### Creating Notes

Use the templates in the `templates/` folder as starting points:

- **Lecture Notes**: Copy `lecture-notes-template.md` for class notes or video lectures
- **Concept Notes**: Copy `concept-notes-template.md` for in-depth concept explanations
- **Exercise Notes**: Copy `exercise-notes-template.md` for practice problems and solutions

### Adding Images

1. Save images in the course's `images/` folder: `courses/{course-name}/images/`
2. Reference them in markdown using relative paths:
   ```markdown
   ![Description](../images/diagram.png)
   ```

## 📝 Note-Taking Tips

- Use descriptive filenames (e.g., `neural-networks-basics.md` instead of `lecture-1.md`)
- Add relevant tags in the frontmatter for easy searching
- Link related concepts within the course
- Update the course README with links to new notes
- Use checkboxes `- [ ]` for tracking learning objectives and questions

## 🔍 Finding Notes

- Browse by course in the `courses/` directory
- Each course has a README with links to all notes
- Use your editor's search functionality to find specific topics or tags

## ✏️ Markdown Features

This repository supports standard markdown including:

- Code blocks with syntax highlighting
- Math equations (if your markdown viewer supports KaTeX/LaTeX)
- Tables for organizing information
- Task lists for tracking progress
- Images and diagrams

## 📖 Template Usage

All templates include YAML frontmatter for metadata:

```yaml
---
title: "Note Title"
course: "Course Name"
date: YYYY-MM-DD
tags: [tag1, tag2]
---
```

This helps with organization and enables potential future automation or tooling.
