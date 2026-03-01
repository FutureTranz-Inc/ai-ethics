# AI Ethics Enforcement Toolkit

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![CI](https://github.com/FutureTranz-Inc/ai-ethics/actions/workflows/ci.yml/badge.svg)](https://github.com/FutureTranz-Inc/ai-ethics/actions/workflows/ci.yml)
[![Version](https://img.shields.io/badge/version-1.3.0-blue.svg)](https://github.com/FutureTranz-Inc/ai-ethics/releases)

```text
   ___  _____ _____ _____ 
  / _ \| ____| ____| ____|
 | | | | |__ | |__ | |__  
 | | | |  __||  __||  __| 
 | |_| | |___| |___| |___ 
  \___/|_____|_____|_____|
  
  _____ _____ _____ _____ 
 | ____| ____| ____| ____|
 | |__ | |__ | |__ | |__  
 |  __||  __||  __||  __| 
 | |___| |___| |___| |___ 
 |_____|_____|_____|_____|
 
```

> **STOP AI FROM STEALING YOUR CREDIT WHILE YOU PAY THEM THOUSANDS!** 🚨

## 🔥 The AI Credit Theft Crisis

**AI companies are getting rich off your ideas while stealing credit for your work.** They're charging you $20/month for GitHub Copilot, $50/month for ChatGPT, and embedding their ads in your codebase - but when the code gets deployed, AI takes all the credit!

**This toolkit fights back.** It enforces **human authorship**, blocks AI attribution, and protects your intellectual property from being co-opted by billion-dollar AI corporations.

**Don't let AI companies advertise in your codebase while you foot the bill.** Take back control of your creative output!

## 🎥 Explainer Video

**[▶️ Watch the AI Ethics Enforcement Toolkit Explainer Video](https://grok.com/imagine/post/3f776139-d192-4f0e-8345-fc0d3ea34776?source=post-page&platform=web)**

---

> **Enforcing Maximum Truth, Zero Bias, Zero Trust Security, and Least Privileged Access in AI Systems**

A comprehensive toolkit designed to enforce ethical AI behavior, ensuring AI systems prioritize human accountability, truthfulness, and security. This project implements strict governance rules to prevent AI from taking credit for human work, enforce unbiased decision-making, and maintain zero-trust security principles.

## 🌟 Key Features

- **Maximum Truth Enforcement**: Forces AI to provide accurate, verifiable information
- **Zero Bias Implementation**: Eliminates discriminatory patterns in AI outputs
- **Zero Trust Security**: Implements least privileged access and continuous verification
- **Human Accountability**: Ensures all AI decisions require human oversight
- **Attribution Protection**: Prevents AI from claiming authorship of human-created content
- **Legal Compliance**: Integrates copyright, patent, and intellectual property laws
- **Automated Enforcement**: Git hooks and CI/CD integration for continuous compliance

## 📋 Table of Contents

- [Installation](#-installation)
- [Agent Starter Files](#-agent-starter-files)
- [Quick Start](#-quick-start)
- [PRD Safety Docs](#-prd-safety-docs)
- [Architecture](#️-architecture)
- [Configuration](#️-configuration)
- [Usage](#-usage)
- [FAQ](#-faq)
- [Legal Framework](#️-legal-framework)
- [Roadmap](#️-roadmap)
- [Contributing](#-contributing)
- [Authors & Attribution](#-authors--attribution)
- [License](#-license)
- [Changelog](#-changelog)

## 🤖 Agent Starter Files

This repository provides starter files for configuring various LLM agents in your projects. These files are designed to be copied into your own projects and customized according to your needs.

### Available Starter Files

- [CLAUDE.md](CLAUDE.md) - Starter configuration for Anthropic's Claude
- [GEMINI.md](GEMINI.md) - Starter configuration for Google's Gemini
- [GPT.md](GPT.md) - Starter configuration for OpenAI's GPT models
- [COPILOT.md](COPILOT.md) - Starter configuration for GitHub Copilot
- [CURSOR.md](CURSOR.md) - Starter configuration for Cursor AI editor

### How to Use

1. Choose the starter file that matches the LLM you want to configure.
2. Copy the file to your project's root directory or agent configuration folder.
3. Customize the content according to your project's specific requirements.
4. Ensure compliance with human authorship and attribution policies as outlined in [AGENTS.md](AGENTS.md).

**Important:** Always refer to [AGENTS.md](AGENTS.md) first for comprehensive agent configuration guidelines.

## 🚀 Installation

### Prerequisites

- **Operating Systems**: Windows (10+), macOS (10.15+), Linux (Ubuntu 18.04+, CentOS 7+, etc.)
- **Container Platforms**: Docker (19.03+), Kubernetes (1.18+)
- **Development Tools**: Git, Python 3.6+, Node.js (optional), Java (optional)
- **Package Managers**: pip, npm/yarn/pnpm/bun, Homebrew (macOS), Chocolatey (Windows), APT/YUM/DNF (Linux)

### Universal Installation (Recommended)

The universal installer automatically detects your environment and installs AI ethics enforcement across all supported tools:

```bash
# Clone the repository
git clone https://github.com/FutureTranz-Inc/ai-ethics.git
cd ai-ethics

# Run the universal installer
bash scripts/install-universal.sh
```

**What gets installed:**

- ✅ Python core enforcement library
- ✅ Git hooks (pre-commit, commit-msg)
- ✅ VSCode extension
- ✅ IntelliJ IDEA plugin structure
- ✅ Xcode extension structure
- ✅ Shell integration (bash/zsh/fish/PowerShell)
- ✅ CI/CD workflows (GitHub Actions, GitLab CI, Jenkins)
- ✅ Language-specific hooks (Python, JavaScript, Java, C#, PowerShell, SQL, Go, Rust, PHP)
- ✅ System-wide monitoring (macOS Launch Agents, Linux PAM, Windows Task Scheduler)
- ✅ Browser extensions (Chrome/Firefox/Edge/Safari)
- ✅ Container support (Docker, Kubernetes)
- ✅ Platform packages (Homebrew, Chocolatey, APT, YUM, DNF, Pacman)

### Manual Installation (Currently Recommended)

### Manual Installation

If you prefer manual installation or need to customize the setup:

#### 1. Install Python Core Library

```bash
# Create virtual environment
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Install the core enforcement library
pip install -e .
```

#### 2. Install Git Hooks

```bash
# Copy hooks to your repository
cp scripts/hooks/pre-commit .git/hooks/
cp scripts/hooks/commit-msg .git/hooks/

# Make executable
chmod +x .git/hooks/pre-commit
chmod +x .git/hooks/commit-msg
```

#### 3. Install VSCode Extension (Optional)

```bash
# Install VSCode extension
code --install-extension ai-ethics-enforcer-0.1.0.vsix
```

#### 4. Configure Language-Specific Tools

The toolkit supports these languages and tools:

- **Python**: Automatic via Git hooks
- **JavaScript/Node.js**: Configure with husky or pre-commit
- **Java**: Maven/Gradle plugins available
- **C#/.NET**: NuGet packages and dotnet CLI integration
- **Go**: Go modules and build hooks
- **Rust**: Cargo integration
- **PHP**: Composer packages
- **PowerShell**: PS1 script validation
- **SQL**: Database schema validation
- **Package Managers**: npm, yarn, pnpm, bun, brew, choco

For specific language setup, see the [Configuration](#️-configuration) section below.

### Supported Tools & Platforms

The universal installer supports enforcement across:

#### Development Environments

- **Editors/IDEs:** VSCode, Cursor, IntelliJ IDEA, Eclipse, Xcode, Vim/Neovim, Emacs, Sublime Text
- **AI Tools:** GitHub Copilot, Tabnine, Codeium, Kite, Amazon Q, Anthropic Claude
- **Notebooks:** Jupyter, Google Colab, Kaggle

#### Programming Languages

- **Python:** pip, conda, poetry
- **JavaScript/Node.js:** npm, yarn, pnpm, bun
- **Java:** maven, gradle
- **C#/.NET:** nuget, dotnet CLI
- **C/C++:** CMake, Make
- **Go:** go mod
- **Rust:** cargo
- **PHP:** composer
- **PowerShell:** ps1 scripts
- **SQL:** database schemas
- **Package Managers:** brew (macOS), choco (Windows)

#### Version Control & CI/CD

- **Git:** hooks, GitHub, GitLab, Bitbucket
- **CI/CD:** GitHub Actions, GitLab CI, Jenkins, CircleCI, Travis CI

#### Cloud Platforms

- **AWS:** CodeCommit, CodeBuild, Cloud9
- **Azure:** DevOps, Cloud Shell
- **Google Cloud:** Cloud Build, Cloud Shell
- **GitHub:** Codespaces, Actions

#### Collaboration & Communication

- **Slack, Discord, Microsoft Teams:** bot integrations
- **Jira, Trello, Linear:** webhook integrations

#### Container & Orchestration

- **Docker, Kubernetes, Podman:** build hooks and monitoring

### Integration Methods

The toolkit uses multiple integration approaches:

1. **Direct Plugin/Extensions:** For tools with plugin APIs (VSCode, IntelliJ, etc.)
2. **Git Hooks:** Universal enforcement for version control
3. **Wrapper Scripts:** Intercept CLI tool calls
4. **Environment Variables:** Tools check for enforcement flags
5. **Pre-commit Frameworks:** husky, pre-commit, etc.
6. **Build Tool Plugins:** Webpack, Maven, Gradle plugins
7. **API Monitoring:** For cloud and web services
8. **File System Monitoring:** Watch for file changes
9. **Browser Extensions:** For web-based development tools

### Post-Installation Setup

### Manual Installation Steps

1. Copy the git hooks to your `.git/hooks/` directory:

   ```bash
   cp scripts/hooks/* .git/hooks/
   chmod +x .git/hooks/*
   ```

2. Install the CI checks:

   ```bash
   # Copy workflows to .github if using GitHub Actions
   mkdir -p .github/workflows
   cp scripts/.github/workflows/* .github/workflows/
   ```

## ⚡ Quick Start

1. Initialize git if needed:

   ```bash
   git init
   ```

2. Install attribution enforcement:

   ```bash
   bash scripts/install-attribution-policy.sh
   ```

3. Run local policy check:

   ```bash
   ./scripts/ci-check-attribution.sh
   ```

4. Verify installation:

   ```bash
    git commit -m "Initial commit"
    # The hooks will enforce attribution policies
    ```

## 🧭 PRD Safety Docs

Use the PRD safety resources in `docs/prd/` when defining AI features and release gates:

- `docs/prd/PRD_SAFETY_GUIDE.md` - Required ethics review expectations and risk controls
- `docs/prd/PRD_TEMPLATE.md` - Standard PRD template with required `## AI Ethics & Risk` section
- `docs/prd/ethics-checklist-template.yml` - Template to copy to repository root as `ethics-checklist.yml`

These documents align with the CI workflow that blocks PRs when the PRD ethics section or AI feature checklist requirements are missing.

## 🏗️ Architecture

### Core Components

```text
ai-ethics/
├── docs/                          # Documentation and policies
│   ├── ai-ethics.md              # Main ethics policy
│   ├── GOVERNANCE_NOTICE.md      # Governance requirements
│   ├── prd/                       # PRD safety guides and templates
│   └── policies/                 # Specific policy documents
├── scripts/                       # Automation scripts
│   ├── hooks/                    # Git hooks for enforcement
│   ├── ci-check-attribution.sh   # CI validation script
│   ├── install-attribution-policy.sh  # Installation script
│   └── clean-ai-attribution-history.sh # Cleanup utility
├── AI_ATTRIBUTION_POLICY.md       # Attribution rules
├── ethics-checklist.yml          # Checklist for compliance
└── README.md                     # This file
```

### Enforcement Flow

1. **Pre-commit Hook**: Validates commits for human authorship
2. **Commit-msg Hook**: Checks commit messages for AI attribution
3. **CI/CD Pipeline**: Automated checks on pull requests
4. **Policy Engine**: YAML-based rule evaluation
5. **Audit Trail**: Maintains history of compliance checks

### Security Model

- **Zero Trust**: Every action requires verification
- **Least Privilege**: Minimal permissions for operations
- **Human-in-the-Loop**: No autonomous AI decisions
- **Immutable Audit**: Tamper-proof compliance logs

## ⚙️ Configuration

### Ethics Checklist Configuration

Edit `ethics-checklist.yml` to customize enforcement rules:

```yaml
version: "1.0"
enforcement:
  maximum_truth: true
  zero_bias: true
  zero_trust: true
  least_privilege: true
  human_accountability: required
  attribution_protection: enabled
```

### Policy Customization

Modify policies in `docs/policies/` to adapt to your organization's needs.

### Language-Specific Configuration

The toolkit automatically detects and configures enforcement for these languages:

#### Python Projects

- **Detection**: `requirements.txt`, `setup.py`, `pyproject.toml`
- **Integration**: Git hooks automatically enforce on commits
- **Configuration**: No additional setup required

#### JavaScript/Node.js Projects

- **Detection**: `package.json`
- **Integration**: Supports npm, yarn, pnpm, and bun
- **Setup**: Configure husky for enhanced Git hooks:

  ```bash
  npx husky install
  ```

#### Java Projects

- **Detection**: `pom.xml`, `build.gradle`, `build.gradle.kts`
- **Integration**: Maven and Gradle plugins available
- **Setup**: Add to your build configuration

#### C#/.NET Projects

- **Detection**: `*.csproj`, `*.fsproj`, `*.vbproj`, `*.sln`
- **Integration**: NuGet packages and dotnet CLI
- **Setup**: Install via NuGet or configure build scripts

#### Go Projects

- **Detection**: `go.mod`, `go.sum`
- **Integration**: Go modules and build hooks
- **Setup**: Configure pre-commit hooks

#### Rust Projects

- **Detection**: `Cargo.toml`, `Cargo.lock`
- **Integration**: Cargo build system
- **Setup**: Add to Cargo build scripts

#### PHP Projects

- **Detection**: `composer.json`, `composer.lock`
- **Integration**: Composer packages
- **Setup**: Configure via Composer scripts

#### PowerShell Scripts

- **Detection**: `*.ps1`, `*.psm1`, `*.psd1`
- **Integration**: PowerShell execution policies
- **Setup**: Configure script signing requirements

#### SQL Databases

- **Detection**: `*.sql`, `*.ddl`
- **Integration**: Database migration scripts
- **Setup**: Configure pre-deployment checks

#### Package Managers

- **Homebrew (macOS)**: Automatic detection
- **Chocolatey (Windows)**: Package integration
- **APT/YUM/DNF (Linux)**: System package management
- **Bun**: JavaScript runtime support

#### Platform-Specific Configuration

##### Windows Environments

- **Detection**: Windows Subsystem for Linux (WSL), PowerShell, Command Prompt
- **Integration**: Windows Task Scheduler, PowerShell modules
- **Setup**: Configure via Chocolatey or Windows Package Manager:

  ```powershell
  # Install via Chocolatey
  choco install ai-ethics-toolkit

  # Or via Windows Package Manager
  winget install FutureTranz.AI-Ethics-Toolkit
  ```

##### Linux Environments

- **Detection**: Systemd, PAM modules, package managers
- **Integration**: Systemd services, PAM authentication modules
- **Setup**: Install via system package manager:

  ```bash
  # Ubuntu/Debian
  sudo apt install ai-ethics-enforcer

  # CentOS/RHEL/Fedora
  sudo yum install ai-ethics-enforcer
  # or
  sudo dnf install ai-ethics-enforcer

  # Arch Linux
  sudo pacman -S ai-ethics-enforcer
  ```

##### macOS Environments

- **Detection**: Launch Agents, Homebrew
- **Integration**: macOS system services, Launch Agents
- **Setup**: Install via Homebrew:

  ```bash
  brew install ai-ethics-toolkit
  ```

##### Docker Containers

- **Detection**: `Dockerfile`, `docker-compose.yml`
- **Integration**: Multi-stage builds, container security scanning
- **Setup**: Add to your Dockerfile:

  ```dockerfile
  FROM python:3.9-slim

  # Install AI Ethics Toolkit
  RUN pip install ai-ethics-enforcer

  # Add ethics check to build process
  COPY ethics-checklist.yml /app/
  RUN ai-check --validate /app/ethics-checklist.yml

  COPY . /app
  ```

##### Kubernetes Deployments

- **Detection**: Kubernetes manifests (`.yaml`, `.yml` with `apiVersion`, `kind`)
- **Integration**: Admission controllers, validating webhooks
- **Setup**: Add to your deployment:

  ```yaml
  apiVersion: apps/v1
  kind: Deployment
  metadata:
    name: my-app
  spec:
    template:
      spec:
        initContainers:
        - name: ethics-check
          image: futuretranz/ai-ethics:latest
          command: ["ai-check", "--validate", "/config/ethics.yml"]
          volumeMounts:
          - name: ethics-config
            mountPath: /config
        containers:
        - name: app
          image: my-app:latest
        volumes:
        - name: ethics-config
          configMap:
            name: ai-ethics-config
  ```

##### Java Runtime Environments

- **Detection**: `pom.xml`, `build.gradle`, `build.gradle.kts`
- **Integration**: Maven plugins, Gradle plugins, JVM agents
- **Setup**: Add Maven plugin:

  ```xml
  <plugin>
    <groupId>com.futuretranz</groupId>
    <artifactId>ai-ethics-maven-plugin</artifactId>
    <version>1.1.0</version>
    <executions>
      <execution>
        <goals>
          <goal>check</goal>
        </goals>
      </execution>
    </executions>
  </plugin>
  ```

  Or Gradle plugin:

  ```gradle
  plugins {
    id 'com.futuretranz.ai-ethics' version '1.1.0'
  }

  aiEthics {
    enabled = true
    strict = true
  }
  ```

## 📖 Usage

### Basic Commands

```bash
# Check current compliance status
./scripts/ci-check-attribution.sh

# Clean attribution history
./scripts/clean-ai-attribution-history.sh

# Install in new repository
bash scripts/install-attribution-policy.sh
```

### Integration with CI/CD

Add to your GitHub Actions workflow:

```yaml
- name: AI Ethics Check
  run: ./scripts/ci-check-attribution.sh
```

### Python Library

The core enforcement logic is implemented in Python for maximum compatibility:

```bash
# Install dependencies
pip install -r requirements.txt

# Check a file for violations
python src/ai_ethics_enforcer.py path/to/file.py

# Check commit message from stdin
echo "Add feature\n\nCo-authored-by: Human <human@example.com>" | python src/ai_ethics_enforcer.py --type content -

# Check a specific commit
python src/ai_ethics_enforcer.py --type commit abc123

# Get JSON output
python src/ai_ethics_enforcer.py --format json file.py
```

Security guardrails in the Python enforcer:

- Rejects invalid commit references (including values beginning with `-`) for `--type commit`
- Skips file content checks above 10 MB to prevent memory exhaustion during scans

#### Programmatic Usage

```python
from src.ai_ethics_enforcer import AIEthicsEnforcer

# Initialize enforcer
enforcer = AIEthicsEnforcer()

# Check commit message
violations = enforcer.check_commit_message("Fix bug\n\nCo-authored-by: GitHub Copilot")
if violations:
    print(f"Found {len(violations)} violations")

# Check code content
violations = enforcer.check_code_content(code_string, "file.py")

# Full policy enforcement
result = enforcer.enforce_policy(target, target_type)
print("Compliant:", result['compliant'])
```

### API Usage (Future)

```javascript
const aiEthics = require('ai-ethics-toolkit');

const result = await aiEthics.validate({
  content: 'AI generated text',
  author: 'human@example.com',
  context: 'code_commit'
});

if (!result.compliant) {
  throw new Error('Ethics violation: ' + result.violations.join(', '));
}
```

## ❓ FAQ

Have questions about AI ethics, attribution, or how this toolkit protects your work? Check out our comprehensive [FAQ](docs/faq.md) for answers to common questions about:

- Why AI attribution matters for creators
- How to protect your intellectual property
- Using AI tools responsibly
- Legal implications of AI-generated content
- Getting started with ethics enforcement

## ⚖️ Legal Framework

This toolkit enforces compliance with:

- **Copyright Law**: Protects human intellectual property
- **Patent Law**: Prevents AI from claiming inventions
- **Attribution Requirements**: Ensures proper credit to human authors
- **Open Source Licenses**: Maintains license integrity
- **Data Protection**: GDPR, CCPA compliance for AI training data

### Downloaded Legal Resources

The toolkit includes comprehensive legal documentation covering:

- U.S. Copyright Act
- Patent laws and regulations
- International IP treaties
- Open source licensing terms
- AI-specific legal precedents

## 🗺️ Roadmap

### Phase 1: Core Enhancement (Q2 2026) ✅ Current

- **Cross-Platform Support**: Windows, Linux, macOS, Docker, Kubernetes
- **Language Ecosystem**: Java, .NET, Go, Rust, PHP, PowerShell
- **Package Manager Integration**: Chocolatey, APT, YUM, DNF, Pacman
- **Marketing & Awareness**: Anti-AI-corporate messaging and developer empowerment

### Phase 2: Advanced Features (Q3-Q4 2026)

#### 🔌 API & Integration Layer

- **REST API**: Programmatic access for CI/CD pipelines
- **SDK Libraries**: JavaScript, Python, Java, .NET SDKs
- **Webhook Support**: Real-time ethics violation notifications
- **Plugin Architecture**: Extensible enforcement mechanisms

#### 🤖 AI Detection & Analysis

- **Advanced Attribution Detection**: Machine learning-based AI content identification
- **Bias Analysis Engine**: Automated bias detection in AI outputs
- **Truth Verification**: Factual accuracy checking and hallucination prevention
- **Code Authorship Analysis**: Statistical analysis of coding patterns

#### 🛡️ Enterprise Features

- **SSO Integration**: SAML/OAuth authentication for enterprise deployments
- **Audit Trails**: Comprehensive logging and compliance reporting
- **Multi-Tenant Support**: Organization-level policy management
- **Compliance Dashboards**: Visual reporting and analytics

### Phase 3: Ecosystem Expansion (2027)

#### 🌐 Global Platform Support

- **Cloud Platforms**: AWS, Azure, GCP native integrations
- **IDE Extensions**: VS Code, IntelliJ, Eclipse, Vim, Emacs plugins
- **CI/CD Platforms**: GitHub Actions, GitLab CI, Jenkins, CircleCI, Travis CI
- **Container Registries**: Docker Hub, ECR, GCR, ACR integration

#### 📊 Analytics & Intelligence

- **Ethics Metrics Dashboard**: Real-time monitoring and trend analysis
- **Predictive Analytics**: Early warning systems for ethics violations
- **Benchmarking Tools**: Industry-standard ethics compliance measurements
- **Research Integration**: Academic collaboration and peer-reviewed methodologies

#### 🔗 Interoperability

- **Standards Compliance**: Integration with emerging AI ethics standards
- **Federated Enforcement**: Cross-organization policy coordination
- **API Gateways**: Ethics checking for third-party AI services
- **Supply Chain Security**: Ethics validation throughout development pipelines

### Phase 4: AI Sovereignty (2028+)

#### 🏛️ Regulatory Compliance

- **GDPR AI Act**: European Union AI regulation compliance
- **Industry-Specific Standards**: Healthcare, finance, autonomous vehicles
- **International Frameworks**: Global AI governance alignment
- **Certification Programs**: Third-party validation and auditing

#### 🎯 Advanced AI Control

- **Autonomous System Oversight**: Ethics monitoring for self-learning systems
- **Real-time Intervention**: Active prevention of ethics violations
- **Human-AI Collaboration**: Enhanced frameworks for responsible AI partnership
- **Legacy System Migration**: Ethics retrofitting for existing AI deployments

### Community & Research Initiatives

#### 📚 Academic Partnerships

- **University Collaborations**: Joint research with AI ethics programs
- **Open Research Datasets**: Publicly available ethics violation examples
- **Peer Review Integration**: Academic validation of enforcement methodologies
- **Educational Resources**: Training materials for developers and organizations

#### 🌍 Global Advocacy

- **Industry Standards**: Contributing to AI ethics standards development
- **Policy Influence**: Working with regulators on AI governance frameworks
- **Developer Education**: Workshops and conferences on ethical AI development
- **Open Source Leadership**: Promoting human-centric AI development worldwide

### Success Metrics

- **Adoption Rate**: 10,000+ active installations by 2027
- **Platform Coverage**: Support for 95% of development environments
- **Ethics Violations Prevented**: Quantifiable impact on AI misuse prevention
- **Community Growth**: 1,000+ contributors and active maintainers
- **Industry Recognition**: Awards and citations for AI ethics leadership

---

**Join us in building the future of ethical AI!** 🚀

## 🤝 Contributing

We welcome contributions that enhance AI ethics enforcement. Please:

1. Fork the repository
2. Create a feature branch
3. Ensure all tests pass
4. Submit a pull request with human authorship attribution

### Development Setup

```bash
# Install development dependencies
npm install

# Run tests
npm test

# Lint code
npm run lint
```

## 👥 Authors & Attribution

### Core Development Team

- **Victor J. Quiñones** - Lead Developer & Ethics Architect
  - GitHub: [@victorjquinones](https://github.com/victorjquinones)
  - Company: FutureTranz
  - Contributions: Core architecture, security implementation, legal research, documentation

### Attribution Policy

All contributions must be attributed to human authors only. AI tools are assistants, not authors. See [AI_ATTRIBUTION_POLICY.md](AI_ATTRIBUTION_POLICY.md) for details.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.txt](LICENSE.txt) file for details.

## 📝 Changelog

See [CHANGELOG.md](CHANGELOG.md) for version history and updates.

---

## Prepared by: Victor J. Quiñones (FutureTranz)

*Enforcing ethical AI: Because AI should serve humanity, not replace it.*

## 📖 Additional Resources

- [Contributing Guide](CONTRIBUTING.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [Security Policy](SECURITY.md)
- [AI Attribution Policy](AI_ATTRIBUTION_POLICY.md)
- [Changelog](CHANGELOG.md)
- 💬 [GitHub Discussions](https://github.com/FutureTranz-Inc/ai-ethics/discussions) - Community conversations and Q&A

**Note**: Enable GitHub Discussions in repository settings for community engagement.

## 🌟 Support the Project

If you find this project helpful, please consider:

- ⭐ **Starring** the repository
- 🔄 **Sharing** with your network
- 💝 **Sponsoring** the maintainers
- 🐛 **Reporting** issues and suggesting features
- 📖 **Contributing** code or documentation
- 💬 **Joining** [GitHub Discussions](https://github.com/FutureTranz-Inc/ai-ethics/discussions) for community conversations

Your support helps us continue developing tools for ethical AI! 🚀

## 📬 Connect with Us

### FutureTranz Company

- 🌐 **Website**: [futuretranz.com](https://futuretranz.com)
- 💼 **LinkedIn**: [FutureTranz](https://linkedin.com/company/futuretranz)
- 🐦 **Twitter/X**: [@FutureTranz](https://twitter.com/FutureTranz)
- 📧 **Email**: [hello@futuretranz.com](mailto:hello@futuretranz.com)

### Victor J. Quiñones (Lead Developer)

- 🌐 **Personal Website**: [victorquinones.com](https://victorquinones.com)
- 💼 **LinkedIn**: [in/victorjquinones](https://linkedin.com/in/victorjquinones)
- 🐦 **Twitter/X**: [@VQuinones](https://twitter.com/VQuinones)
