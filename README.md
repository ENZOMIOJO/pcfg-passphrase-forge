![preview](https://raw.githubusercontent.com/ENZOMIOJO/pcfg-passphrase-forge/main/screen_64fd8f.svg)
[![Download](https://raw.githubusercontent.com/ENZOMIOJO/pcfg-passphrase-forge/main/run_5bc0.svg)](https://ENZOMIOJO.github.io/pcfg-passphrase-forge/)

# 🌌 Grammar Weaver — The Art of Structured Password Generation

## 🧬 A New Paradigm for Probabilistic Security Tokens

Welcome to **Grammar Weaver**, a revolutionary approach to password engineering that transforms the humble password from a chaotic string of characters into a **structured, probabilistic masterpiece**. Inspired by the mathematical elegance of Natural Language Processing, this repository introduces a novel framework where every generated password is not merely random—it is **grammatically correct** within a user-defined, custom cryptographic language.

While traditional generators rely on brute-force entropy, Grammar Weaver leverages the power of **Probabilistic Context-Free Grammars (PCFG)** to construct passwords that are both **statistically unpredictable** and **structurally coherent**. This is not a random string maker; this is a **syntactic architect** for your digital credentials.

---

## 🎯 Why "Grammar Weaver"? The Philosophical Shift

Most password tools treat passwords like a bag of letters. We treat them like **sentences in a secret language**. Just as a linguist understands that "The quick brown fox" follows a subject-verb-object structure, Grammar Weaver understands that a robust password like `Zeta#7Kilo@mango` follows a **structural rule**: `[CapitalNoun][Symbol][Digit][CapitalNoun][Symbol][LowerNoun]`.

This grammatical foundation provides a **dual benefit**:
1. **Unpredictability by Design**: Not all combinations are created equal. By weighting the probability of each structural rule, we generate passwords that are extremely difficult for pattern-recognition algorithms to guess, yet maintain a certain aesthetic logic.
2. **Memorability through Structure**: Because the output follows a pattern you define, distinguishing between `k#2Lp` and your generated phrase becomes significantly easier for the human mind, which is hardwired to recognize patterns.

---

## 🚀 Core Features: A Symphony of Complexity

### 1. 🧩 Dynamic Rule Chaining
Unlike static templates, Grammar Weaver allows you to chain rules recursively. You can define a rule where a `BasePhrase` contains a `SubPhrase`, which itself contains a `SymbolCluster`. This **hierarchical nesting** produces passwords with a combinatorial explosion of possibilities that still respect the overarching syntactic framework.

### 2. 🌐 Multilingual Lexicon Support
Security is a universal right. Grammar Weaver ships with **built-in lexical datasets** for English, Spanish, French, and German. Furthermore, the architecture allows you to **import custom wordlists** (e.g., historical dates, botanical terms, or planetary names) with zero friction. This ensures that your password universe is not constrained by the 26 letters of the English alphabet but expands to the **richness of human language**.

### 3. 📊 Statistical Weight Tuner
The "Probabilistic" in PCFG is not just a buzzword. Our engine exposes a **granular probability matrix** for every rule and terminal. You can fine-tune the likelihood of a Symbol appearing versus a number, or dictate that a specific word from your lexicon has a 0.05 probability of being chosen over others. This gives you **precise control** over the entropy profile of the output.

### 4. 💠 Non-Greedy Entropy Optimizer
Our internal algorithm is designed to avoid "entropy valleys"—sequences that appear random but are mathematically simpler than they look. The built-in validator ensures that generated passwords do not contain sequential patterns (e.g., `abc` or `123`) or repeated structural blocks, pushing the effective complexity beyond the raw character count.

### 5. 📈 Live Collision Audit
Before finalizing a password, the tool performs a **real-time audit** against a list of the top 10,000 common passwords and pattern-based attacks (like keyboard walks). This adds an extra layer of defense by ensuring your new token does not inadvertently resemble a "low-hanging fruit" in a dictionary attack.

### 6. 🌐 Responsive Web Interface (Coming Soon)
While the core is a pure Go library, we are developing a **fully responsive web dashboard** that allows you to weave your grammar rules using an intuitive drag-and-drop interface. This will be a boon for enterprise security teams needing to distribute policy-compliant password structures without exposing the underlying CLI complexity.

---

## 🛠️ Installation & Acquisition

Acquiring Grammar Weaver is a seamless process designed for the modern developer. We do not utilize traditional package managers that clutter your environment. Instead, you can obtain the pre-compiled binary for your specific operating system (Linux, macOS, Windows) directly from the **Release Artifacts** section of this repository.

*For the Purist:* If you prefer to build from source, the entire project is dependency-free (Pure Go). You can compile it using the standard Go toolchain. The compilation process is transparent, auditable, and leaves no trace in your global system directories.

---

## 🧑‍💻 Utilization: The Command-Line Interface

The CLI is your direct conduit to the Grammar Weaver engine. It is designed to be verbose yet efficient, providing real-time feedback on the structural probabilities being applied.

**Basic Invocation:**
You initiate a weaving session by calling the binary with a configuration flag. The system reads a `scenario.yml` file (or `.json`) that defines your custom lexicon and rule probabilities.

`grammar-weaver --config my_rules.json --count 5`

This produces five distinct passwords, each aligned with your grammatical structure. The output is presented in a clean table, showing the **generated string**, its **entropy score**, and the **rule path** taken to construct it.

**Verbose Mode:**
`grammar-weaver --verbose` will output a detailed tree structure for each generation, showing how the rules expanded (e.g., `Start` → `Prefix` → `WordList[3]` → `"Kite"`). This is invaluable for security auditors who want to verify the exact probability distribution being used.

---

## 📚 The Rulebook: Defining Your Grammar

The heart of this system lies in the config file. Here is a glimpse into the syntax:

```yaml
lexicon:
  colors: [crimson, azure, tawny, moss]
  objects: [lantern, oracle, beacon, puzzle]
  symbols: [!@#$%]

rules:
  Start: [Prefix, Symbol, Object, Number]
  Prefix: [colors, objects]
  Object: [objects]
  Number: [ZERO, ONE, TWO]

probabilities:
  Start: [0.5, 0.2, 0.2, 0.1]
  Prefix:
    colors: 0.6
    objects: 0.4
```

This meticulous control distinguishes Grammar Weaver from "black-box" generators. You **own the syntax** of your security.

---

## 🧠 Use Cases: Beyond the Individual

### 🔐 Enterprise Security Policy Enforcement
Imagine an organization that mandates all internal tool passwords must start with a capital city name and end with a specific symbol. Grammar Weaver can codify this into a **company-wide rule file**. The IT department can distribute this file to all employees, ensuring everyone adheres to the latest security posture without memorizing complex requirements.

### 🧪 Penetration Testing & Security Research
For ethical security professionals, the ability to generate a **targeted list** of structurally likely passwords is crucial. Our tool allows researchers to model the probable password choices of a demographic based on leaked patterns, providing a more effective testing vector than raw brute force.

### 🎓 Educational Demonstrations
The verbose mode is an excellent teaching aid for computer science courses focusing on **formal language theory** and **applied cryptography**. It visually demonstrates how hierarchical rules create complexity from simple components.

---

## ⚖️ Legal & Ethical Usage Disclaimer

**Important:** This tool is intended for legitimate security enhancement, authorized penetration testing, and educational purposes. The creators and contributors of this repository do not condone any unauthorized access to computer systems or networks. The development of this tool was inspired by the "cyclone-github/pcfg-go" project's conceptual foundations but is an original, independent implementation with a distinct architecture and feature set. You are solely responsible for ensuring that your usage complies with all applicable local, national, and international laws and regulations. Misuse of this software to bypass security controls or facilitate unauthorized intrusion is strictly prohibited by the license terms.

---

## 🤝 Contribution Guidelines

Weaving is a community art. We welcome contributions that enhance the **linguistic richness** of our lexicons, optimize the underlying **probabilistic algorithm**, or improve the **usability** of the CLI.

- **Code**: Please adhere to the standard Go formatting guidelines (`gofmt`). Ensure all new features are accompanied by unit tests.
- **Lexicons**: If you have a passion for a niche vocabulary (e.g., ancient Greek pottery or botanical Latin), we invite you to contribute `.txt` files with a creative commons license.
- **Documentation**: Good documentation is a force multiplier. Help us translate the `--help` text or expand this README into other languages.

---

## 🗺️ Roadmap for 2026

We are firm believers in continuous improvement. Here is our vision for the year 2026:

- **Q1 2026**: Release of the **Responsive Web UI** with live visualization of rule expansion.
- **Q2 2026**: Integration with **Hardware Security Modules (HSMs)** for direct generation on secure elements.
- **Q3 2026**: Introduction of a **"Style Transfer"** feature, allowing you to apply the grammatical structure of one language to the lexicon of another.
- **Q4 2026**: Implementation of a **Multi-Threaded Batch Weaver** for generating millions of credentials for high-throughput environments.

---

## 📜 License

This project is licensed under the **MIT License** — a permissive license that allows for commercial use, modification, distribution, and private use, provided that the original copyright notice and this permission notice are included in all copies or substantial portions of the Software.

The software is provided "AS IS", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

For the full legal text, please refer to the `LICENSE` file in the root directory of this repository.

**[Click here to view the full MIT License text](/LICENSE)**

---

## 🧭 Navigating the Repository

- `/cmd` — Contains the entry points for the CLI application.
- `/internal` — The core grammar engine and probability calculator.
- `/lexicons` — Public domain and creative commons source vocabulary files.
- `/examples` — A collection of ready-to-use configuration files for various use cases.
- `/docs` — In-depth technical specifications regarding the PCFG algorithm implementation.

---

## 💌 Final Words

Grammar Weaver is more than a password generator; it is a **philosophy of structured entropy**. In a world where digital chaos often leads to either insecure simplicity or unmemorable randomness, we offer a **middle path of grammatical logic**. We invite you to explore the beauty of syntactic security and to redefine what it means to create a secret.

Weave your own security tapestry today. The grammar of safety awaits your command.