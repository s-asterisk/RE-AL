# RE:AL (Real-time Expressive Audio Lyricism)  
**A Framework for Neural Singing Voice Synthesis**  

![RE:AL System Architecture](https://github.com/user-attachments/assets/63c9be21-49ac-4485-9d20-dd5fa5ff4a63)  

[![License: GPLv3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)  
![Python](https://img.shields.io/badge/Python-3.8+-blue)  
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-orange)  

---

## 1. Overview  
RE:AL is a neural singing voice synthesis framework combining lyric-to-melody conversion with parametric voice modulation. The system architecture enables:  

- Conversion of textual lyrics into MIDI-compatible melodic structures  
- Spectral parameter estimation for singing voice synthesis  
- Cross-lingual phoneme alignment (English/Japanese)  
- Pitch-accurate vocal rendering with emotional expressiveness controls  

---

## 2. Technical Features  

### 2.1 Core Components  
- **Lyric-to-MIDI Transformer**: Attention-based sequence modeling for melody generation  
- **Parametric Vocoder**: Hybrid WORLD/Crepe pipeline for F0 estimation and correction  
- **Bi-LSTM Duration Model**: Phoneme-level timing prediction with prosodic features  
- **Multilingual Phonemizer**: CMUdict/OpenJTalk integration for English/Japanese support  

### 2.2 Synthesis Pipeline  
1. Text normalization → Phoneme conversion  
2. Melody prediction (LSTM/Transformer)  
3. Duration modeling → Pitch contour generation  
4. WORLD-based spectral parameter synthesis  
5. Crepe-based pitch refinement  

---

## 3. Development Progress  

| Module                | Implementation Status      | Current Version |  
|-----------------------|----------------------------|-----------------|  
| Phoneme Alignment     | Production-ready (MFA v2.2) | 2.2.0           |  
| Base Melody Generator | LSTM Prototype              | 0.4.1-alpha     |  
| WORLD Integration     | Beta Testing                | 1.1.3-beta      |  
| Emotion Modulation    | Research Prototype          | 0.0.8-dev       |  

---

## 4. Installation Guide  
Coming Soon

### 4.1 System Requirements  
- Python 3.8+  
- FFmpeg 4.3+  
- CUDA 11.7+ (Recommended)  

### 4.2 Environment Setup  
```bash  
git clone https://github.com/s-asterisk/RE-AL.git  
cd RE-AL  

python -m venv .venv  
source .venv/bin/activate  

pip install -r requirements/core.txt  
pip install -r requirements/audio.txt  
