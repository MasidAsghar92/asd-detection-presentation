# ASD Detection Using AI and Brain MRI - Presentation

> A professional presentation about using artificial intelligence and brain MRI scans for early Autism Spectrum Disorder (ASD) detection.

[![Generate PPTX](https://github.com/MasidAsghar92/asd-detection-presentation/actions/workflows/generate-pptx.yml/badge.svg)](https://github.com/MasidAsghar92/asd-detection-presentation/actions/workflows/generate-pptx.yml)

## 📊 About This Presentation

This repository contains a complete presentation covering:

- **Introduction to ASD** and the importance of early detection
- **Literature Review** of current AI and MRI research
- **Existing Systems** and their limitations
- **Proposed Approach** using 3D-CNN and explainable AI
- **System Architecture** with 10 key modules
- **Requirements** (functional and non-functional)
- **Use Cases** for clinical deployment
- **Future Work** and next steps

## 🎯 Quick Start

### Download the Latest PPTX

**Option 1: From GitHub Actions Artifacts**
1. Go to [Actions](https://github.com/MasidAsghar92/asd-detection-presentation/actions)
2. Click on the latest successful workflow run
3. Download the `ASD-Detection-Presentation` artifact
4. Unzip and open `ASD_Detection_Presentation.pptx`

**Option 2: From Releases**
1. Go to [Releases](https://github.com/MasidAsghar92/asd-detection-presentation/releases)
2. Download the latest `ASD_Detection_Presentation.pptx`

**Option 3: Generate Manually Trigger**
1. Go to [Actions](https://github.com/MasidAsghar92/asd-detection-presentation/actions/workflows/generate-pptx.yml)
2. Click "Run workflow"
3. Download from artifacts when complete

## 📝 Edit the Presentation

The presentation is written in **Marp** markdown format for easy editing.

### Edit Online (Recommended)
1. Open [`presentation.md`](./presentation.md)
2. Click the ✏️ edit button
3. Make your changes
4. Commit - the PPTX will regenerate automatically!

### Edit Locally

```bash
# Clone the repository
git clone https://github.com/MasidAsghar92/asd-detection-presentation.git
cd asd-detection-presentation

# Edit the presentation
code presentation.md  # or your favorite editor

# Commit and push
git add presentation.md
git commit -m "Update presentation content"
git push

# The PPTX will be generated automatically by GitHub Actions
```

## 🛠️ Generate PPTX Locally

### Prerequisites
- Node.js (v18 or higher)
- npm

### Steps

```bash
# Install Marp CLI
npm install -g @marp-team/marp-cli

# Generate PPTX
marp presentation.md --pptx -o ASD_Detection_Presentation.pptx

# Generate PDF (alternative)
marp presentation.md --pdf -o ASD_Detection_Presentation.pdf

# Generate HTML (for web viewing)
marp presentation.md --html -o index.html
```

### Using Docker (no local installation needed)

```bash
docker run --rm -v $PWD:/home/marp/app/ marpteam/marp-cli presentation.md --pptx -o ASD_Detection_Presentation.pptx
```

## 📚 Presentation Structure

| Slide # | Title |
|---------|-------|
| 1 | Title: ASD Detection Using AI and Brain MRI |
| 2 | Introduction to ASD Detection |
| 3 | Literature Review – Key Points |
| 4 | Existing Systems – Short Summary |
| 5 | Proposed Approach |
| 6 | System Modules |
| 7 | Functional Requirements |
| 8 | Non-Functional Requirements |
| 9 | Use Case Overview |
| 10 | Conclusion |
| 11 | Thank You |

## 🤝 Contributing

Want to improve the presentation? Feel free to:

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -m 'Add improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Masid Asghar**

- GitHub: [@MasidAsghar92](https://github.com/MasidAsghar92)

## 🙏 Acknowledgments

- [Marp](https://marp.app/) - Markdown Presentation Ecosystem
- Research community working on ASD detection using AI

---

**Note**: This presentation is for educational and research purposes. The proposed system is a research concept and not a medical diagnostic tool.
