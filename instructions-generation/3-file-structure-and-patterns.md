# 3-file-structure-and-patterns.md

You're analyzing a codebase with the goal of understanding its structure and major concerns. 

## File Structure and Patterns

- Map out the project’s file and folder structure.
- For each module in the project, perform the following:
  - Map the File and Folder Structure
     - List the directory tree for each module (e.g., domain-api, domain, jpa-adapter, rest-adapter, acceptance-test, bootstrap, etc.).
     - For each directory, briefly describe its purpose and the role of its key files.
  - Document Patterns to Follow
     - For each module, specify naming conventions for files, classes, and packages.
     - List architectural and design patterns to follow (e.g., where to place interfaces, models, configuration, etc.).
     - Include best practices for dependency management, code organization, and separation of concerns.
  - Document Patterns to Avoid
	- For each module, list anti-patterns and practices to avoid (e.g., forbidden dependencies, implementation details in interfaces, business logic in adapters, field injection, etc.).
	- Highlight common mistakes and how to prevent them.
  - Format
	- Present each module in the following structure:
		- Module Name
		- File/Folder Structure (tree)
		- Purpose
		- Patterns to Follow
		- Patterns to Avoid
- Add all your findings to ./{output-folder}/3-file-structure-and-patterns.md
- Once completed read [./4-contribution-guidelines.md](./4-contribution-guidelines.md) and continue on accordingly with {output-folder} as the `output-folder`


