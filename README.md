# 🏙️ CivicPulse - AI Civic Issue Reporter

An open-source, on-device multimodal civic intelligence application built for **Hacktoberfest Hack Day Prayagraj × GDG**.

CivicPulse empowers citizens to report urban infrastructure damage (potholes, waterlogging, garbage overflows) by automatically analyzing evidence photos using an open-weight vision transformer model, routing grievances to the appropriate municipal authority in Prayagraj, and producing formal bilingual complaint letters.

---

## 📌 Problem Statement

Every day, citizens in urban areas encounter hazards like broken roads, blocked drains, and garbage dumps. However, civic participation remains low due to critical bottlenecks:

1. **Jurisdictional Confusion:** Citizens rarely know which civic agency handles a specific issue (e.g., Public Works Department vs. Nagar Nigam Civil Division vs. Jal Sansthan).
2. **Drafting Friction:** Writing formal, legally structured grievance petitions to commissioners is tedious and intimidating.
3. **Language Barriers:** Official administrative communications often require formal Hindi or English phrasing that everyday citizens find difficult to compose.
4. **Data Privacy & API Dependency:** Most AI applications rely on commercial, proprietary cloud APIs that pose privacy risks and require paid subscriptions.

---

## 💡 The Solution

CivicPulse provides a **100% open-weight, locally computed pipeline** that converts an uploaded photo into direct civic action:

* **Zero Proprietary API Keys:** Runs locally on-device / GPU using open-source models from Hugging Face.
* **Multimodal Visual Inspection:** Detects hazards, pavement damage, waste accumulation, and structural risks.
* **Automated Municipal Routing:** Directly maps issues to verified administrative contacts in Prayagraj (Prayagraj Nagar Nigam, PWD, Jal Sansthan) alongside official phone helplines.
* **Bilingual Petitions:** Produces formal, standardized grievance letters in both English and clean Hindi.
* **Direct Mail Escalation:** Features a single-click web Gmail launcher that populates the recipient email, subject line, and grievance body for instant dispatch.

---

## 🛠️ Architecture & Tech Stack

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Multimodal Vision Model** | `Salesforce/blip-image-captioning-large` | Open-weight vision transformer for visual inspection and feature extraction |
| **Inference Framework** | PyTorch & Hugging Face `transformers` | Local GPU-accelerated inference with zero external network dependencies |
| **Frontend UI** | Streamlit | Responsive, real-time web interface |
| **Deployment & Tunneling** | Cloudflare Tunnel (`cloudflared`) | Secure zero-trust public HTTPS tunneling for live demos |
| **Software License** | MIT License | 100% Free and Open-Source Software (FOSS) |

---

## 🏛️ Administrative Routing Matrix (Prayagraj Jurisdiction)

| Detected Issue Type | Primary Agency | Redressal Email | Helpline |
| :--- | :--- | :--- | :--- |
| **Potholes / Pavement Cracks** | Public Works Department (PWD) / Civil Works | `cealldpwd@nic.in` | `1800-180-0400` |
| **Solid Waste / Garbage Overflow** | Prayagraj Nagar Nigam (Health & Sanitation) | `nagarnigamald@gmail.com` | `1533 / 0532-2400858` |
| **Drainage / Waterlogging / Sewage** | Jal Sansthan Prayagraj / Urban Drainage | `gm-jalsansthanald@up.gov.in` | `0532-2460838` |
| **General Infrastructure Hazard** | Municipal Corporation Control Room | `nagarnigamald@gmail.com` | `0532-2400858` |

---

## 🚀 Getting Started

### Prerequisites

* Python 3.10+
* CUDA-enabled GPU (or Google Colab T4 GPU environment)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/PriyanshKesarwani/OpenCivic-Issue-Reporter.git
   cd OpenCivic-Issue-Reporter
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Streamlit application:**
   ```bash
   streamlit run app.py
   ```

4. Open `http://localhost:8501` in your browser.

---

## 📦 Repository Structure

```text
OpenCivic-Issue-Reporter/
├── app.py              # Streamlit application with BLIP model inference and Gmail routing
├── requirements.txt    # Python dependencies
├── LICENSE             # MIT Open Source License
└── README.md           # Comprehensive project documentation
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👥 Hackathon Team & Acknowledgements

* **Developer:** Priyansh Kesarwani ([@PriyanshKesarwani](https://github.com/PriyanshKesarwani))
* **Event:** Hacktoberfest Hack Day Prayagraj × GDG
* **Track:** Best Open-Source AI Project
