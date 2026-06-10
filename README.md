Remote sensing semantic segmentation is a core task in Earth observation and plays an
important role in urban planning and land-use classification. The emergence of vision foundation model
(VFM) has significantly boosted the segmentation performance. However, in real-world deployment, a pretrained VFM must handle remote sensing images from other domains that it has never encountered. In this
work, we advance domain generalization in remote sensing image segmentation by concentrating on the
central challenge, namely, large cross-domain appearance shifts. A novel joint spectral-spatial adapter (SSA)
is proposed to implement parameter-efficient fine-tuning on a frozen VFM, enabling better generalization
capability. Technically, the proposed adapter consists of three components. Layer-wise spectral factorization
combines a Haar-wavelet pyramid with spectrum-aware splitting to stabilize the content and structurepreserving details under cross-domain variations. Spectral-spatial mixture-of-expert modeling then refines
these features through both spectrum and spatial updates, each of which is empowered by an expert
model. Before decoding the segmentation map, energy-aware dynamic routing adaptively fuses expert
outputs to suppress domain-specific styles without discarding boundaries and fine structures. On the ISPRS
Vaihingen→Potsdam and Potsdam→Vaihingen settings, the proposed method achieves 62.6% and 71.0%
mIoU, respectively, improving over the strongest comparable DINOv2-based baseline by 1.5 and 3.8
percentage points. On WHU Aerial→Satellite II and Satellite II→Aerial, it further improves F1/IoU to
46.9%/43.2% and 74.1%/72.3%, respectively
