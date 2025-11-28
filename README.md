# 🏷️ Auto-Annotation Arxiv Daily

[![Daily Update](https://github.com/Ezharjan/DailyAutoAnnotationArxiv/workflows/Run%20AutoAnnotation%20Arxiv%20Papers%20Daily/badge.svg)](https://github.com/Ezharjan/DailyAutoAnnotationArxiv/actions)
[![License](https://img.shields.io/github/license/Ezharjan/DailyAutoAnnotationArxiv)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/Ezharjan/DailyAutoAnnotationArxiv)](https://github.com/Ezharjan/DailyAutoAnnotationArxiv/commits/main)

> **Automatically tracking the latest research papers in Auto-Annotation and Computer Vision from arXiv**

📊 **12 Research Domains** | 🔄 **Daily Updates** | 🤖 **Fully Automated** | 🌐 **[Live Website](https://Ezharjan.github.io/DailyAutoAnnotationArxiv/)**

---

## 📋 Table of Contents

- [🎯 About](#-about)
- [✨ Features](#-features)
- [🚀 Quick Start](#-quick-start)
- [🎓 Usage](#-usage)
- [⚙️ Configuration](#️-configuration)
- [🌐 Deployment](#-deployment)
- [📚 Research Domains](#-research-domains)
- [🛠️ Troubleshooting](#️-troubleshooting)
- [🤝 Contributing](#-contributing)

---

## 🎯 About

**Auto-Annotation Arxiv Daily** is an automated research paper tracking system that:

- 📰 **Fetches** latest papers from arXiv every 24 hours
- 🎯 **Filters** by 150+ Auto-Annotation and Computer Vision keywords across 12 domains
- 🔗 **Links** to code repositories when available
- 📊 **Organizes** papers by research domain
- 🌐 **Publishes** to a beautiful website with search

Perfect for researchers and AI enthusiasts who want to stay updated on:
- Auto-annotation and annotation automation
- Vision foundation models (CLIP, GroundingDINO, SAM)
- 3D object detection and LiDAR perception
- Autonomous driving and sensor fusion
- Few-shot and zero-shot learning
- And more!

**Last Updated**: Auto-generated daily at 9:00 AM UTC

---

## ✨ Features

### 🤖 Fully Automated
- ✅ Daily arXiv paper fetching via GitHub Actions
- ✅ Automatic commit and website deployment
- ✅ Weekly code repository link updates
- ✅ Zero manual intervention required

### 🎨 Beautiful Web Interface
- ✅ Modern Jekyll theme with search
- ✅ Mobile-responsive design
- ✅ Dark/light mode support
- ✅ Sidebar navigation by domain
- ✅ Quick stats dashboard

### 🔍 Smart Organization
- ✅ 12 comprehensive Auto-Annotation and Computer Vision domains
- ✅ 150+ curated research keywords
- ✅ Automatic categorization
- ✅ Code repository detection
- ✅ JSON data export

### ⚡ Easy Customization
- ✅ Simple YAML configuration
- ✅ Add your own topics/keywords
- ✅ Adjustable paper count
- ✅ Configurable update schedule
- ✅ Interactive local testing

---

## 🚀 Quick Start

### Prerequisites
- Python 3.7+
- pip
- Git (for GitHub deployment)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/Ezharjan/DailyAutoAnnotationArxiv.git
cd DailyAutoAnnotationArxiv

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run interactive test
python test_local.py
# Choose option 1 for quick test

# 4. Check results
cat README.md
```

That's it! The script will fetch papers and generate the paper list.

---

## 🎓 Usage

### Local Testing

#### Interactive Mode (Recommended)
```bash
python test_local.py
```

**Options:**
1. **Quick test** - 2 topics, 5 papers (30 seconds)
2. **Full test** - All 12 topics (2-5 minutes)
3. **Update links** - Refresh code repository links

#### Direct Execution
```bash
# Fetch all papers
python daily_arxiv.py

# Update code links only
python daily_arxiv.py --update_paper_links
```

### Generated Files
- `README.md` - Main paper list (table format)
- `docs/index.md` - Web-friendly version
- `docs/auto-annotation-arxiv-daily.json` - Complete data
- `docs/auto-annotation-arxiv-daily-web.json` - Web-optimized data

---

## ⚙️ Configuration

### Basic Settings

Edit `config.yaml`:

```yaml
# How many papers per topic
max_results: 15

# Your GitHub info (for deployment)
user_name: "YourGitHubUsername"
repo_name: "DailyAutoAnnotationArxiv"

# Base directory (usually /docs for GitHub Pages)
base_url: "https://yourusername.github.io/DailyAutoAnnotationArxiv/"
```

### Adding Research Topics

```yaml
keywords:
    "Your Topic Name":
        filters: ["keyword 1", "keyword 2", "multi word phrase"]
```

**Example:**

```yaml
keywords:
    "3D Object Detection":
        filters: 
            - "3D Object Detection"
            - "LiDAR Detection"
            - "Point Cloud Detection"
            - "3D Bounding Box"
            - "BEV Detection"
```

### Adjusting Paper Count

- **5-10**: Focused, high-quality (faster)
- **15-20**: Balanced (recommended)
- **20+**: Comprehensive (may include tangential)

### Update Schedule

Edit `.github/workflows/autoannotation-arxiv-daily.yml`:

```yaml
schedule:
  - cron: "0 2 * * *"  # Daily at 2 AM UTC
```

Change to:
- `"0 */12 * * *"` - Every 12 hours
- `"0 0 */2 * *"` - Every 2 days
- `"0 0 * * 1,4"` - Monday & Thursday

Use [crontab.guru](https://crontab.guru/) for custom schedules.

---

## 🌐 Deployment

### GitHub Pages (Recommended)

#### 1. Fork or Create Repository
```bash
git add .
git commit -m "Initial commit: Auto-Annotation Arxiv Daily"
git push origin main
```

#### 2. Update Configuration

**Edit `.github/workflows/autoannotation-arxiv-daily.yml`:**
```yaml
env:
  GITHUB_USER_NAME: YourUsername  # Change this
  GITHUB_USER_EMAIL: your@email.com
```

**Edit `config.yaml`:**
```yaml
user_name: "YourUsername"  # Change this
```

#### 3. Enable GitHub Actions
1. Settings → Actions → General
2. Workflow permissions: **Read and write**
3. Save

#### 4. Enable GitHub Pages
1. Settings → Pages
2. Source: **Deploy from branch**
3. Branch: `main`, Folder: `/docs`
4. Save

#### 5. Trigger First Run
1. Actions tab
2. "Run AutoAnnotation Arxiv Papers Daily"
3. "Run workflow"

Your site: `https://yourusername.github.io/DailyAutoAnnotationArxiv/`

---

## 📚 Research Domains

Current tracking covers 12 comprehensive Auto-Annotation and Computer Vision domains:

<details>
<summary><strong>🏷️ Auto-Annotation & Annotation Automation</strong></summary>

- Auto-annotation pipelines
- Automatic labeling
- Annotation tools
- Semi-automatic annotation
- Label generation
- Annotation quality control
</details>

<details>
<summary><strong>🔮 Foundation Models for Vision</strong></summary>

- Vision foundation models (VFM)
- CLIP and visual grounding
- GroundingDINO
- Open-vocabulary detection
- Zero-shot detection
- Foundation model adaptation
</details>

<details>
<summary><strong>🎯 Few-Shot & Zero-Shot Learning</strong></summary>

- Few-shot learning (FSL)
- Zero-shot learning
- Few-shot detection
- Meta-learning
- Prototypical networks
- Transfer learning
</details>

<details>
<summary><strong>👤 Active Learning & Human-in-the-Loop</strong></summary>

- Active learning
- Human-in-the-loop annotation
- Interactive annotation
- Uncertainty sampling
- Sample selection
- Crowdsourcing
</details>

<details>
<summary><strong>📦 3D Object Detection & LiDAR</strong></summary>

- 3D object detection
- LiDAR detection
- Point cloud detection
- 3D bounding box
- BEV detection
- Camera-LiDAR fusion
</details>

<details>
<summary><strong>🖼️ 2D Object Detection & Segmentation</strong></summary>

- Object detection
- Instance segmentation
- Semantic segmentation
- SAM (Segment Anything)
- DETR and detection transformers
- Panoptic segmentation
</details>

<details>
<summary><strong>🚗 Autonomous Driving & Perception</strong></summary>

- Autonomous driving perception
- nuScenes, KITTI, Waymo
- Multi-modal perception
- Sensor fusion
- Traffic scene understanding
- Vehicle and pedestrian detection
</details>

<details>
<summary><strong>🔗 Multi-Modal Learning & Fusion</strong></summary>

- Multi-modal learning
- Vision-language models
- Camera-LiDAR fusion
- Sensor fusion
- Cross-modal retrieval
- 2D-3D lifting
</details>

<details>
<summary><strong>💬 Prompt Learning & Engineering</strong></summary>

- Prompt learning
- Visual prompting
- Prompt tuning
- In-context learning
- Chain-of-thought
- Instruction following
</details>

<details>
<summary><strong>🌐 3D Vision & Geometry</strong></summary>

- 3D computer vision
- 3D reconstruction
- SLAM
- Depth estimation
- Pose estimation
- Camera calibration
</details>

<details>
<summary><strong>📊 Dataset Curation & Benchmarking</strong></summary>

- Dataset curation
- Benchmark datasets
- Annotation benchmarks
- Data quality
- Evaluation protocols
- Dataset construction
</details>

<details>
<summary><strong>🤖 LLM & Large Language Models</strong></summary>

- Large language models
- GPT and instruction understanding
- Vision-language integration
- Multi-modal LLMs
- Text understanding
- LLM for annotation
</details>

---

## 🛠️ Troubleshooting

### Installation Issues

**"Import arxiv could not be resolved"**
```bash
pip install arxiv requests pyyaml
```

**"Python not found"**
```bash
# Install Python 3.7+ from python.org
# Verify: python --version
```

### Paper Fetching Issues

**"No papers found"**
- Check internet connection
- Increase `max_results` in config.yaml (try 20)
- Use broader keywords

**"Papers not relevant"**
- Edit config.yaml keywords
- Add specific domain terms: "annotation", "detection", "segmentation"
- Review and refine filters

**"SSL/Connection errors"**
- Handled gracefully with warnings
- Papers save even if code link fetch fails
- Check firewall/proxy settings if persistent

### GitHub Actions Issues

**"Workflow not running"**
1. Enable Actions (Settings → Actions)
2. Grant write permissions
3. Check YAML syntax
4. View Actions tab for errors

**"Permission denied"**
- Settings → Actions → General
- Workflow permissions: **Read and write**

**"Website not updating"**
- Wait 2-5 minutes after Action completes
- Check Pages settings (should show "Active")
- Clear browser cache

### Data Quality Issues

**"Too many irrelevant papers"**
- Reduce `max_results` (try 10)
- Use more specific keywords
- Add negative filters (if needed)

**"Missing important papers"**
- Increase `max_results` (try 20-25)
- Add broader synonym keywords
- Check arXiv categories are correct

---

## 🤝 Contributing

We welcome contributions! Here's how:

### Adding Keywords

1. Fork the repository
2. Edit `config.yaml`
3. Test locally: `python test_local.py`
4. Submit pull request

### Reporting Issues

Found a bug? [Open an issue](https://github.com/Ezharjan/DailyAutoAnnotationArxiv/issues) with:
- Description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Error messages (if any)

### Suggesting Features

Have an idea? [Start a discussion](https://github.com/Ezharjan/DailyAutoAnnotationArxiv/discussions) about:
- New research domains
- UI improvements
- Additional features
- Integration ideas

---

## 📊 Statistics

- **Research Domains**: 12
- **Keywords**: 150+
- **Papers per Day**: ~50-100 (varies)
- **Update Frequency**: Every 24 hours
- **Auto-update Schedule**: 9:00 AM UTC
- **Link Updates**: Weekly (Mondays)

---

## 📞 Support

- 📖 **Documentation**: See files in this repo
- 🐛 **Bug Reports**: [GitHub Issues](https://github.com/Ezharjan/DailyAutoAnnotationArxiv/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/Ezharjan/DailyAutoAnnotationArxiv/discussions)
- 📧 **Email**: mysoft@111.com

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file.

---

## 🙏 Acknowledgments

- arXiv API for paper access
- Papers with Code for repository links
- GitHub Actions for automation
- Jekyll and Just the Docs theme

---

## 🔗 Links

- 🌐 **Live Website**: https://Ezharjan.github.io/DailyAutoAnnotationArxiv/
- 📦 **GitHub Repo**: https://github.com/Ezharjan/DailyAutoAnnotationArxiv
- 📊 **JSON Data**: [auto-annotation-arxiv-daily.json](docs/auto-annotation-arxiv-daily.json)
- 📘 **Detailed Usage**: [docs/README.md](docs/README.md)

---

<div align="center">

## 🎉 Happy Researching!

**Stay updated with the latest in Auto-Annotation and Computer Vision**

Made with ❤️ for the research community

</div>

---
