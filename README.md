# Make 3D Diffusion Easier: Accelerating Multidimensional MRI with Unified Autocalibrated Diffusion Framework
Multidimensional magnetic resonance imaging (MRI) combines spatial encoding with an additional acquisition-dependent dimension (e.g., motion dynamics, contrast evolution, and pharmacokinetic dynamics), providing rich information for diverse applications including dynamic, quantitative, and perfusion imaging. **Highly accelerated multidimensional MRI reconstruction** can substantially facilitate high-throughput and patient-friendly imaging. 

Recent diffusion models show great promise with their flexibility and robustness at high acceleration factors. However, these existing approaches circumvent **the instability of high-dimensional manifolds** by decomposing **3D acquisitions (i.e., 2D spatial and 1D acquisition-dependent dimension)** into multiple 2D sub-problems, which disrupts the intrinsic coupling and correlations across spatial and acquisition dimensions and prevents the model from capturing the full 3D data distribution.

In this work, we focus on the fundamental challenge of enabling **effective and stable high-dimensional diffusion modeling** for faithful multidimensional MRI reconstruction. Rather than tailoring diffusion models to specific applications or decomposing the problem into lower-dimensional subspaces, we identify and exploit **a key common prior** that ubiquitously exists across multidimensional MRI acquisitions, namely the autocalibration signal (ACS). By leveraging ACS as **a physics-informed inductive bias**, we demonstrate that **diverse multidimensional imaging tasks** can be addressed under **a unified generative paradigm** without architectural modifications.

![Overview_ACDiff](https://github.com/wangziblake/ACDiff/blob/main/Figure/Overview_ACDiff_v3.png)

Our main contributions are summarized as follows: 

1) A unified autocalibrated 3D diffusion framework (ACDiff) is proposed for faithful multidimensional MRI reconstruction. By leveraging ACS as a physics-informed inductive bias, the proposed framework **navigates the unstable landscapes of high-dimensional manifolds** and constrains the reverse diffusion trajectory toward **physically plausible reconstructions**.
2) A novel autocalibrated cross-attention mechanism is designed to effectively project low-frequency k-space priors from ACS as **geometric anchors** within the latent space, facilitating **the stable and faithful recovery of high-frequency structural details** that are typically lost to stochastic noise.
3) Under **various acceleration configurations (6x, 8x, 10x)**, the unified ACDiff framework consistently achieves state-of-the-art performance and strong robustness across representative multidimensional MRI applications, including **dynamic, quantitative, and perfusion imaging**.
4) ACDiff not only substantially **breaks the performance bottleneck** of vanilla 3D diffusion (up to 3.48 dB PSNR and 7.94% SSIM gains) but also provides a practical and scalable framework that **bridges physical acquisition priors and data-driven generative modeling**.

Given its **strong versatility and scalability**, we believe that the proposed unified autocalibrated diffusion framework represents **a promising and general reconstruction solution** for accelerated multidimensional MRI. Furthermore, this study offers a principled pathway toward unified generative paradigm for inverse problems in multidimensional medical imaging.

**The preprint paper can be seen at (coming soon ...)**

**Email: Dr. Zi Wang (zi.wang@imperial.ac.uk); Dr. Guang Yang (g.yang@imperial.ac.uk)**


## ACDiff framework (Under construction)
The training and testing codes of ACDiff framework are released here.

Run the main code for training, use:
```
/ACDiff_maincode/ACDiff/ACDiff_Train_withCSM_Minibatch_InOrder_torch_CineSAX.py
/ACDiff_maincode/ACDiff/ACDiff_Train_withCSM_Minibatch_InOrder_torch_T1Mapping.py
/ACDiff_maincode/ACDiff/ACDiff_Train_withCSM_Minibatch_InOrder_torch_BreastDCE320.py
```
Run the main code for reconstruction, use:
```
/ACDiff_maincode/ACDiff/ACDiff_RD_Recon_torch.py
```

Python environment should be: python=3.6.13, pytorch=1.10.1

**Note: The software is used for academic only, and cannot be used commercially.**


## Citation
If you want to use the code, please cite the following paper:

Zi Wang et al., Accelerating multidimensional MRI with unified autocalibrated diffusion framework, ***TBD***, 2026.


## Acknowledgement
The authors thank Drs. Michael Lustig, Ricardo Otazo, Hyungjin Chung, Jong Chul Ye, and Yang Song for sharing their codes online. 


![Visitors](https://visitor-badge.laobi.icu/badge?page_id=<wangziblake>.<ACDiff>)
