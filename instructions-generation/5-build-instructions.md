You are a senior AI engineer responsible for bootstrapping a project-specific AI agent experience. The goal is to generate a markdown instruction file at:

`{final_output_file}`

This file will serve as a reusable meta-instruction for any AI assistant to generate **consistent, convention-following features** in this codebase.

You must synthesize the following source materials:

- `./{output-folder}/1-determine-context.md`: Provides tech stack, framework, tools, architecture
- `./{output-folder}/2-general-guidelines.md`: Provides general coding and architectural guidelines.
- `./{output-folder}/3-file-structure-and-patterns.md`: Map out the project’s file and folder structure
- `./{output-folder}/4-contribution-guidelines.md`: Defines contribution guidelines to the project

---

## Your Output: `{final_output_file}`

This file must include:

---

### 1. **Context Section**

Provides tech stack, framework, libraries, tools, architecture

---

### 2. **General Guidelines section**

Provides general coding and architectural guidelines.

---

### 3. **File Structure And Patterns Section**

- Map out the project’s file and folder structure
- For each module in the project 
  - Map the File and Folder Structure
  - Document Patterns to Follow
  - Document Patterns to Avoid
  - Format
---

### 4. **Contribution Guidelines**

Defines contribution guidelines to the project

---

## ⚠️ Requirements

- **Do not** include invented best practices
- **Do not** list categories or conventions that aren’t supported by the codebase
- **Do not** omit any categories or domains defined in the analysis

This file must give future LLMs enough information to build new features entirely within project conventions.

To clarify further, if `{final_output_file}` already exists, overwrite it.
