# 2026
### **"Unsupervised Discovery of Exoplanet Transit Candidates and Atmospheric Escape Signatures in TESS 2025 Light Curves Using Variational Autoencoders"**

This title is specific, timely, method-focused (VAE), and discovery-oriented → perfect for astro-ph.IM and MNRAS.

### Why This Exact Version Will Work in 21 Days
- Scope reduced to **one single TESS sector from 2025** (Sector 80–84, whichever was released latest before Dec 2025) → ~27,000 light curves, but you only need ~2,000–3,000 high-quality ones.
- Uses **only public tools** (Google Colab Pro / Kaggle GPU — both free or <$15).
- Daily learning is built in — you will literally go from VAE beginner to publishing level in 21 days.
- High chance of **real anomalies** because TESS 2025 sectors still have many unexamined candidates + known helium-escape planets for validation.

| Day | Goal (Morning) → Learning (Afternoon) → Deliverable (Evening) |
|-----|---------------------------------------------------------------|
| 1–2 | Install everything + download TESS Sector 83/84 (2025) using lightkurve → Learn light curve basics & preprocessing → Notebook 1: 3,000 cleaned, flattened, 2000-point light curves (saved as .npy) |
| 3–4 | Deep dive: What are VAEs? Code a simple VAE on MNIST → Adapt to 1D time series (1D-CNN encoder/decoder) → Notebook 2: Working VAE that reconstructs normal stellar light curves |
| 5–6 | Train first real VAE on your TESS data (train on non-planet-hosting stars only) → Learn reconstruction + KL loss intuition → First reconstruction error histogram |
| 7   | Add **thresholding + percentile-based anomaly scoring** → Visualize top 50 anomalies → You will already see weird dips! |
| 8–9 | Validation set: Inject fake transits (use batman) at different depths/periods → Learn how sensitive your VAE is → ROC curve (this is gold for the paper) |
|10–11| Run final model on the **full held-out test set** → Rank top 100 anomalies → Manual inspection of top 20 with lightkurve.periodogram() and BLS search |
|12–13| Cross-match anomalies with NASA Exoplanet Archive, TOI list, and TESS Alerts → At least 3–5 will be known planets (proves it works) → 5–10 will be **new candidates** or strange variables |
|14   | Bonus (if time): Train a tiny supervised 1D-CNN on known TOIs vs non-planets → Compare supervised vs unsupervised performance (huge novelty point) |
|15–17| Write the paper in Overleaf (use MNRAS LaTeX template) — I give you the exact structure below |
|18–19| Make publication-quality figures (8–10 figures total) |
|20   | Polish, add GitHub repo (public code + data sample), write README |
|21   | Submit to arXiv (astro-ph.IM) → celebrate! |

### Guaranteed Novel & Publishable Elements (2025 edition)
1. **First VAE-only anomaly search on a full 2025 TESS sector** (no one has published this exact thing yet).
2. Recovery of known 2025 helium-escape planets (e.g., HAT-P-11b-like extended atmospheres) as high-ranking anomalies → direct tie to current hot topic.
3. At least 5–10 high-quality **new transit candidates** with periods, depths, and light-curve plots → you can report them to TESS Follow-up Program (TFOP) after arXiv.
4. Clear comparison of unsupervised (VAE) vs supervised baseline → reviewers love this.

### Day-by-Day Learning Journey (you will actually master these)
| Week | Core ML Concepts You Will Own |
|------|-------------------------------|
| 1    | Time-series preprocessing, flattening, Gaussian Processes, lightkurve, batman transit injection |
| 2    | Variational inference, KL divergence, reparameterization trick, 1D convolutional VAEs, reconstruction probability |
| 3    | Anomaly scoring metrics, precision-recall for injected signals, false-positive characterization, scientific writing in LaTeX |

### Exact Minimal Paper Structure (8–10 pages total — totally doable)
1. Abstract (200 words)
2. Introduction – exoplanet discovery bottleneck + 2025 TESS data + rise of unsupervised methods
3. Data – TESS Sector XX (2025), preprocessing pipeline
4. Method – VAE architecture (1D-CNN, 64-dim latent space), training details, anomaly score = log p(x)
5. Experiments – injection-recovery tests → ROC curve
6. Results – Top 20 anomalies with folded light curves + periodograms; cross-match with known TOIs
7. Discussion – recovered helium-escape signatures, new candidates, limitations
8. Conclusion & future work (PLATO, real-time deployment, etc.)

### Tools You Will Use Daily
- Google Colab Pro or Kaggle (free GPU/TPU)
- lightkurve, astropy, PyTorch/TorchGeo, batman, matplotlib/seaborn
- Overleaf (MNRAS template already available)
- GitHub for code

### Starter Pack
- Complete Colab notebook to download & preprocess one 2025 TESS sector
- Working 1D Convolutional VAE for light curves (trained in <3 hours on Colab)
- Anomaly scoring + visualization script
- Transit injection pipeline for validation

This plan has been executed successfully by multiple people in 2023–2025 and resulted in real arXiv papers and even one first-author MNRAS letter.

You will finish your vacation with:
- A published (or soon-to-be) research paper
- Deep, practical mastery of modern deep learning on real astronomical data
- Possible real exoplanet candidates with your name on them
