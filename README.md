# Make 3D Diffusion Easier: Accelerating Multidimensional MRI with A Unified Autocalibrated Diffusion Framework
Accelerated dynamic magnetic resonance imaging (MRI) is highly expected in clinical applications. **However, its reconstruction remains challenging due to the inherently high dimensionality and complexity of spatiotemporal information.** Recent diffusion model has emerged as a robust reconstruction approach for spatial imaging, but their applications to spatiotemporal data remain underexplored. Therefore, it is essential to develop a new diffusion model tailored for dynamic MRI reconstruction, to better visualize the changes in organ physiological functions. 

![Method_DiffACS](https://github.com/wangziblake/STDM/blob/main/Figure/Method_DiffACS.png)

Here, we propose **a novel spatiotemporal diffusion model specifically designed for accelerated dynamic MRI**. Our main contributions are summarized as follows: 

1) A **flexible and robust** spatiotemporal diffusion model is proposed for dynamic MRI reconstruction. The learned spatiotemporal prior is agnostic to undersampling scenarios, allowing our method to **flexibly adapt to changes in reconstructions without re-training**.
2) By **analyzing the latent feature distributions** of different datasets, we find that the spatiotemporal diffusion shows greater potential than the existing spatial diffusion for **achieving robust reconstruction across diverse data**.
3) A **simple and effective** diffusion enhancement framework is proposed. It employs dual-directional orthogonal 2D models as a 3D spatiotemporal prior to **avoid visual misalignment and improve reconstruction performance**.
4) For both healthy cases and patients, the proposed method consistently provides state-of-the-art performance in **highly accelerated reconstruction** and shows remarkable robustness across **various undersampling scenarios and unseen data**, including patient data, real-time MRI data, non-Cartesian radial sampling, and different anatomies.

Given the **amazing adaptability and generalization capability**, we believe that our spatiotemporal diffusion model offers a promising direction for achieving more reliable dynamic MRI in diverse scenarios. Furthermore, this innovative approach holds great potential to be extended to the inverse problems in other medical modalities involving dynamic acquisitions.

![Example_DiffACS](https://github.com/wangziblake/STDM/blob/main/Figure/Example_DiffACS.png)

**The preprint paper can be seen at (coming soon ...)**

**Email: Dr. Zi Wang (zi.wang@imperial.ac.uk); Dr. Guang Yang (g.yang@imperial.ac.uk)**


## DiffACS framework
The training and testing codes of DiffACS framework are released here.

Run the main code for training, use:
```
/DiffACS_maincode/DiffACS/DiffACS_Train_withCSM_Minibatch_InOrder_torch_CineSAX.py
/DiffACS_maincode/DiffACS/DiffACS_Train_withCSM_Minibatch_InOrder_torch_T1Mapping.py
/DiffACS_maincode/DiffACS/DiffACS_Train_withCSM_Minibatch_InOrder_torch_BreastDCE320.py
```
Run the main code for reconstruction, use:
```
/DiffACS_maincode/DiffACS/DiffACS_RD_Recon_torch.py
```

Python environment should be: python=3.6.13, pytorch=1.10.1

**Note: The software is used for academic only, and cannot be used commercially.**


## Citation
If you want to use the code, please cite the following paper:

Zi Wang et al., Accelerating multidimensional MRI with a unified autocalibrated diffusion framework, ***arXiv preprint***, 2026.


## Acknowledgement
The authors thank Drs. Michael Lustig, Ricardo Otazo, Hyungjin Chung, Jong Chul Ye, and Yang Song for sharing their codes online. 


![Visitors](https://visitor-badge.laobi.icu/badge?page_id=<wangziblake>.<DiffACS>)
