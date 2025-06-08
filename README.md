# AnomalyFTP

## Results
These are the results obtained from:

**1) GLASS:**
![glass1](results/glass1.png)

**2) SimpleNet**
![SimpleNet](results/SimpleNet.png)

---

## **Unsupervised Anomaly Detection for Industrial Visual Inspection: Implementation and Evaluation**

AnomalyFTP is an open-source implementation focused on unsupervised anomaly detection for industrial visual inspection tasks. The repository provides tools and code for detecting visual anomalies in industrial settings, where abnormal samples are rare and defects can range from subtle scratches to significant structural issues.

---

## Key Features

- Implements state-of-the-art unsupervised anomaly detection methods tailored for industrial images.
- Designed for industrial inspection scenarios where labeled anomalies are scarce.
- Supports evaluation and benchmarking on standard datasets.

---

## Methodology

The repository explores advanced anomaly detection techniques, including models inspired by recent research **GLASS** and **SimpleNet**.

### GLASS: Global and Local Anomaly co-Synthesis Strategy

**GLASS** (Global and Local Anomaly co-Synthesis Strategy) is a unified framework for synthesizing a broader and more controllable range of anomalies at both the feature and image levels. It consists of:

- **Global Anomaly Synthesis (GAS):** Synthesizes weak, near-in-distribution anomalies at the feature level using Gaussian noise guided by gradient ascent and truncated projection. This approach enhances the detection of subtle defects that are close to normal samples.
- **Local Anomaly Synthesis (LAS):** Generates strong, far-from-distribution anomalies at the image level by overlaying textures, providing a diverse set of synthetic anomalies.

GLASS achieves state-of-the-art results on major industrial benchmarks such as MVTec AD (detection AUROC of 99.9%), VisA, and MPDD, and it excels in weak defect detection. Its effectiveness and efficiency have been validated in real-world industrial applications[1][3][4][5].

### SimpleNet

**SimpleNet** is a lightweight and application-friendly network for image anomaly detection and localization. It includes:

- A pre-trained feature extractor for local feature extraction.
- A shallow feature adapter for domain adaptation.
- An anomaly feature generator that injects Gaussian noise during training.
- A binary anomaly discriminator for distinguishing normal and anomalous features.

SimpleNet achieves high accuracy and fast inference, making it suitable for deployment in industrial environments.

---


---

## Getting Started

1. **Clone the repository:**

```bash
git clone https://github.com/nabayansaha/AnomalyFTP.git
cd AnomalyFTP
```

2. **Install dependencies:**
   - Ensure you have Python 3.x and pip installed.
   - Install required packages (see requirements.txt if provided).

3. **Prepare your data:**
   - Organize your industrial inspection images as described in the documentation.

4. **Run the code:**
   - Follow the usage instructions in the repository to train and evaluate anomaly detection models.

---

## Results

- The repository includes sample results and visualizations to demonstrate anomaly localization and detection performance.
- Example outputs (see included images: glass1.png, SimpleNet.png) showcase the ability to identify and highlight defective regions in industrial products.

---

## License

This project is released under the license specified in the repository.

---

## References

- [SimpleNet: A Simple Network for Image Anomaly Detection and Localization]

---

For more details, usage instructions, and contribution guidelines, please refer to the repository documentation.
