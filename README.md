# BrainPARA

A highly structured, automated Obsidian vault built on the [PARA Method](https://fortelabs.com/blog/para/) (Projects, Areas, Resources, Archive). It leverages custom templating and dataview scripts to automate metadata, bidirectional linking, and task management.

## 🗂️ Vault Structure

- **`PROJECTS/`**: Active efforts with a specific goal and deadline. Each project contains an index file (`00000.md`), a Kanban task board, and related resources.
- **`AREAS/`**: Spheres of ongoing activity with a standard to be maintained (e.g., Health, Finances).
- **`RESOURCES/`**: Topics or themes of ongoing interest.
- **`ARCHIVE/`**: Inactive items from the above categories.
- **`Templates/`**: Core scripts and layout templates that automate vault maintenance.

## ✨ Key Features

### 🤖 Interactive File Generation (Templater)
- **Guided Creation**: Templates use interactive prompts to walk you through creating new files, ensuring no metadata is ever missed.
- **Smart Tagging**: Automatically detects existing areas and topics in your vault to offer autocomplete suggestions, preventing duplicate or misspelled tags. 
- **Auto-Filing**: New files automatically inherit the parent tags, project names, and folder paths of the project they are created in.

### 📊 Dynamic Dashboards (Dataview & DataviewJS)
- **Project Indexing**: Every project root (`00000.md`) acts as a dynamic dashboard. It automatically queries and lists all related notes and tasks.
- **Topic Grouping**: A custom DataviewJS script groups project files by their `#topic/` tags into clean markdown tables, instantly organizing scattered research and resources.
- **Orphan File Prevention**: Ensures that all notes are visible on the index page so nothing gets lost in the folder hierarchy.

### 📋 Integrated Task Management (Kanban)
- **Zero-Friction Task Boards**: Generating a new project automatically generates a linked Kanban board alongside it.
- **Direct-to-Board Notes**: When creating a new `Resource` note, the template prompts you to automatically add a linked card directly to the project's "Backlog" or "In Progress" column on the Kanban board.

### 🧠 Knowledge Synthesis (Idea & Source Management)
- **Bidirectional Linking**: When creating an `Idea` note, the system prompts you to link it to specific `Source` notes. It automatically writes the reciprocal links back into the source note's `ideas-extracted` field.
- **Reading Status Automation**: Allows you to mark a source note as `reading_status: integrated` directly from the prompt when you finish extracting ideas from it.
- **Granular Note Types**: Enforces strict `Type` frontmatter (`Index`, `Tasks`, `Resource`, `Idea`, `Source`) so your vault understands the functional purpose of every file.

## 🚀 Getting Started

1. Open Obsidian and select **Open folder as vault**.
2. Select this repository folder.
3. Ensure the following community plugins are installed and enabled:
   - **Dataview** (Enable JavaScript Queries in settings)
   - **Kanban**
   - **Templater** (Set the template folder to `Templates/`)
4. Create a new project by using the `ProjectIndexTemplate.md` to automatically generate the necessary dashboards and Kanban boards.

## 🛠️ Usage

When adding new files, use the integrated templates to ensure correct metadata mapping. The vault relies on specific frontmatter keys (`Parent`, `Type`, `Project`, and `tags`) to dynamically organize your dashboard views and link ideas back to their source material.
