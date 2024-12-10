# LaTeX Document Repository

## Project Overview
This repository contains a comprehensive LaTeX document project with robust automation and organization strategies.

## Repository Structure
```
├── .github/workflows/     # GitHub Actions configuration
├── src/                   # Source files
│   ├── main.tex           # Primary LaTeX document
│   ├── chapters/          # Individual chapter files
│   ├── figures/           # Project graphics and images
│   └── bibliography/      # BibTeX references
└── README.md              # Project documentation
```

## Prerequisites
- LaTeX Distribution (TeXLive recommended)
- Make
- Git

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/your-latex-project.git
cd your-latex-project
```

### 2. Install Dependencies
#### macOS
```bash
brew install --cask mactex
brew install latexmk
```

#### Ubuntu/Debian
```bash
sudo apt-get update
sudo apt-get install texlive-full latexmk
```

## Compilation


### Continuous Integration
This project uses GitHub Actions for automatic compilation:
- PDF is generated on every push to `main`
- Compilation errors are reported in the Actions tab

Note that for this to work, you need to add as secret to your repository the `GITHUB_TOKEN` with the `repo` scope.

## Writing Guidelines

### Adding Chapters
1. Create new chapter files in `src/chapters/`
2. Include them in `main.tex` using `\input{chapters/your-chapter.tex}`

### Managing References
- Store BibTeX references in `src/bibliography/references.bib`
- Use `\bibliography{bibliography/references}` in your main document

### Adding Figures
- Place figures in `src/figures/`
- Use relative paths when including in LaTeX

### Adding listings
- Place listings in `src/listing/`
- Use the relative import command for import a code snippet (currently support Yaml, Dockerfile and Python).


## Contribute to the project
All contributions are welcome! Here's how you can help:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push and create a Pull Request

## License
GNU GENERAL PUBLIC LICENSE

## Contact
Giovanni Antonioni - antonioni.giovanni9@gmail.com