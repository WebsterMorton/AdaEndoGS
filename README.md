# AdaEndoGS

## Under Review | Adaptive Enlightening Model for Endoscopy Based on 3D Gaussian Splatting

📝 
👨‍🔬 Authors: Fei Xia, Yiding Wen, Yuanfan Liu, Huanmei Guan, and Fei Luo  
🏛️ Affiliation: School of Computer Science, Wuhan University


## Abstract
Endoscopic imaging is indispensable for minimally invasive surgeries and clinical diagnosis. However, inherent physical limitations—such as constrained light paths and narrow surgical cavities—often result in uneven illumination and dark regions in captured images. These issues obscure fine anatomical structures, hindering accurate observation and diagnosis.

To address this challenge, we propose **AdaEndoGS**, an adaptive enlightening model for endoscopic scenes that integrates 3D Gaussian Splatting (3DGS) with physical lighting simulation. Our key contributions are:
- 🎯 **Illuminatable 3D Scene Representation**: Extend standard 3DGS by augmenting each Gaussian with surface properties (normal vector, roughness, reflectance), enabling precise modeling of light-matter interactions.
- 📡 **Adaptive Virtual Light Planning**: Leverage ray tracing to identify dark regions, combining Gaussian opacity, surface normal, and viewpoint information to dynamically place virtual light sources.
- ⚡ **Physically Consistent Enhancement**: Ensure enhanced images maintain anatomical fidelity and color consistency, avoiding over-exposure, under-exposure, or structural distortion.

Comprehensive experiments on the VEIDLA (synthetic) and C3VD (real-world) endoscopic datasets validate the effectiveness of AdaEndoGS. Compared with state-of-the-art methods (RetinexNet, EnlightenGAN, Aleth-NeRF, vanilla 3DGS), our model achieves superior performance in dark region detail recovery and illumination uniformity, with more physically realistic results.

### Ablation Study Highlights
📊 Key component validation on VEIDLA dataset (PSNR↑, SSIM↑, LPIPS↓):
- Complete AdaEndoGS: PSNR=22.936, SSIM=0.908, LPIPS=0.165
- W/O DiffuseMLP: PSNR=21.181 (↓1.755), SSIM=0.897, LPIPS=0.182
- W/O L<sub>tone-mse</sub>: PSNR=22.113, SSIM=0.889, LPIPS=0.174
- W/O L<sub>ssim</sub>: PSNR=18.371 (↓4.565), SSIM=0.792, LPIPS=0.211


*🔒 The source code will be released later. Stay tuned for updates!*
