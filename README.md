# AdaEndoGS

## Under Review | Adaptive Enlightening Model for Endoscopy Based on 3D Gaussian Splatting

📝  
👨‍🔬 Authors: Fei Xia,Yiding Wen,Yuanfan Liu,Huanmei Guan,and Fei Luo  
🏛️ Affiliation: School of Computer Science, Wuhan University


## Abstract
Endoscopic imaging technology is crucial for minimally invasive diagnosis and treatment. Due to physical constraints such as limited light source placement and narrow operational space, captured images often contain some dark regions that compromise clinical observation and diagnostic accuracy.

To address this issue, we propose **AdaEndoGS** for endoscopic 3D reconstruction with physically consistent dark region illumination enhancement. Our core contributions include:
- 🎯 **3D Gaussian Splatting Extension**: Enrich each Gaussian point with surface attributes (normal, roughness, reflectance) to construct an illuminatable 3D scene representation.
- 📡 **Adaptive Light Source Planning**: Automatically identify dark regions via ray tracing, leveraging Gaussian opacity/surface normal/viewpoint information to plan virtual light source placement.
- ⚡ **Physically Consistent Enhancement**: Ensure illumination enhancement maintains anatomical detail and color consistency (no over/under exposure).

Experimental results on VEIDLA (synthetic) and C3VD (real-world) endoscopic datasets show that AdaEndoGS more accurately simulates light-matter interactions compared to existing methods (RetinexNet, EnlightenGAN, Aleth-NeRF, vanilla 3DGS), significantly improving visual quality and detail visibility in dark regions.

### Ablation Study Highlights
📊 Key component validation on VEIDLA dataset (PSNR↑, SSIM↑, LPIPS↓):
- Complete AdaEndoGS: PSNR=22.936, SSIM=0.908, LPIPS=0.165
- W/O DiffuseMLP: PSNR=21.181 (↓1.755), SSIM=0.897, LPIPS=0.182
- W/O L<sub>tone-mse</sub>: PSNR=22.113, SSIM=0.889, LPIPS=0.174
- W/O L<sub>ssim</sub>: PSNR=18.371 (↓4.565), SSIM=0.792, LPIPS=0.211


*🔒 The source code will be released later. Stay tuned for updates!*
