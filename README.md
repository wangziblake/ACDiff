# Make 3D Diffusion Easier: Accelerating Multidimensional MRI with Unified Autocalibrated Diffusion Framework
Multidimensional magnetic resonance imaging (MRI) combines spatial encoding with an additional acquisition-dependent dimension (e.g., motion dynamics, contrast evolution, and pharmacokinetic dynamics), providing rich information for diverse applications including dynamic, quantitative, and perfusion imaging. **Highly accelerated multidimensional MRI reconstruction** can substantially facilitate high-throughput and patient-friendly imaging. 

Recent diffusion models show great promise with their flexibility and robustness at high acceleration factors. However, **the complexity and instability of high-dimensional diffusion** often force existing approaches to decompose the natural **3D spatial-acquisition (i.e., 2D spatial and 1D acquisition-dependent dimension) problem** into multiple 2D sub-problems, limiting their ability to capture the full 3D imaging data distribution.

In this work, we focus on the fundamental challenge of enabling **effective and stable 3D diffusion modeling** for accelerated multidimensional MRI. Rather than tailoring diffusion models to specific applications or decomposing the problem into lower-dimensional subspaces, we identify and exploit **a key common prior** that ubiquitously exists across multidimensional MRI acquisitions, namely the autocalibration signal (ACS). By leveraging ACS as a reliable and physically grounded conditioning source, we demonstrate that complex 3D diffusion process can be effectively guided in **a unified manner**, leading to consistent performance improvements across **diverse multidimensional imaging tasks**.

![Method_DiffACS](https://github.com/wangziblake/DiffACS/blob/main/Figure/Method_DiffACS.png)

Our main contributions are summarized as follows: 

1) A unified ACS-conditioned 3D diffusion framework (DiffACS) is proposed for multidimensional MRI reconstruction. It **reduces the complexity of 3D diffusion** by constraining the solution space, thereby guiding the model more efficiently toward the **underlying 3D data distribution** in a simple manner.
2) An element-wise cross-attention mechanism is designed to effectively inject the ACS information into the diffusion process, facilitating **the accurate recovery of high-frequency structural details**.
3) By effectively integrating autocalibration information into **a unified diffusion paradigm**, DiffACS not only **breaks the performance bottleneck** of vanilla 3D diffusion but also provides a practical and scalable framework that **bridges physical acquisition priors and data-driven generative modeling**.
4) Under **various acceleration configurations**, the unified DiffACS framework consistently achieves state-of-the-art performance and strong robustness across representative multidimensional MRI applications, including **dynamic, quantitative, and perfusion imaging**.

Given its **strong versatility and scalability**, we believe that the proposed unified autocalibrated diffusion framework represents **a promising and general reconstruction solution** for accelerated multidimensional MRI. Furthermore, this study offers a principled pathway toward unified generative frameworks for inverse problems in multidimensional medical imaging.

![Example_DiffACS](https://github.com/wangziblake/DiffACS/blob/main/Figure/Example_DiffACS.png)

**The preprint paper can be seen at (coming soon ...)**

**Email: Dr. Zi Wang (zi.wang@imperial.ac.uk); Dr. Guang Yang (g.yang@imperial.ac.uk)**


## DiffACS framework (Under construction)
The training and testing codes of DiffACS framework are released here.

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

Zi Wang et al., Accelerating multidimensional MRI with unified autocalibrated diffusion framework, ***arXiv preprint***, 2026.


## Acknowledgement
The authors thank Drs. Michael Lustig, Ricardo Otazo, Hyungjin Chung, Jong Chul Ye, and Yang Song for sharing their codes online. 


![Visitors](https://visitor-badge.laobi.icu/badge?page_id=<wangziblake>.<ACDiff>)
