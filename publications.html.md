---
# title: "Publications"
format: 
  html:
    keep-md: true
jupyter: python3
echo: false
---


## Publications and Preprints
**Damage Sensing Digital Twin for Piezocomposites Integrating Neural Operator with Parametrically Upscaled Constitutive Damage Model** (2026). _**Y. Liu**, S. Ghosh_. _submitted_ , .

<details>
<summary>Abstract</summary>

Detection and tracking of structural damage under challenging operating conditions are integral to structural health monitoring (SHM) for improving structural reliability and reducing maintenance costs by preventing unwarranted catastrophic failures. Many currently used SHM practices are post-mortem-based and rely on sparse arrays of surface-mounted sensors that detect surface or near-surface damage states, but not those that evolve from the material's interior. In most cases, surface sensors detect cracks that may have already grown into a dominant failure mode from a subsurface location. To overcome these challenges, this paper develops a powerful deep learning-augmented Virtual Damage Sensing Digital Twin (VDS-DT) platform for piezoelectric composites. The platform integrates multiscale-multiphysics modeling, characteristic microstructure representation, and geometry-informed neural operator (GINO) in a bottom-up and top-down sequence to efficiently predict full-field damage evolution in the structure and underlying microstructure in real time, based on measurements at an optimal number and placement of surface-mounted sensors. The VDS-DT comprises three major ingredients, viz. (i) Parametrically Upscaled Coupled Constitutive Damage Model (PUCCDM), whose constitutive coefficients are explicit functions of the underlying Representative Aggregated Microstructural Parameters (RAMPs), (ii)  PUCCDM data-trained GINO that fuses location-specific RAMP fields with electric measurements at a sparse sensor network to reconstruct full field electromechanical and damage fields in structures of arbitrary geometries, and (iii) genetic algorithm (GA) optimized compact, informative sensor layouts. Spatio-temporally evolving damage predictions by the VDS-DT across multiple scales with a few sensors clearly demonstrate its high potential as a scalable, real-time SHM tool for engineering systems.

</details>
        

**The strength of the Brazilian fracture test** (2024). _A. Kumar, **Y. Liu**, J. E. Dolbow, O. Lopez-Pamies_. _Journal of the Mechanics and Physics of Solids_ 182, 105473.
[![DOI: 10.1016/j.jmps.2023.105473](https://img.shields.io/badge/DOI-10.1016/j.jmps.2023.105473-blue.svg)](https://doi.org/10.1016/j.jmps.2023.105473)

<details>
<summary>Abstract</summary>
Since its introduction in the 1940s until present times, the so-called Brazilian test has been embraced by practitioners worldwide as a method of choice to indirectly measure the tensile strength of concrete, rocks, and other materials with a large compressive strength relative to their tensile strength. This is because of the ease that the test affords in both the preparation of the specimen (a circular disk) and the application of the loads (two platens compressing the specimen between them). Yet, this practical advantage has to be tempered by the fact that the observations from a Brazilian test — being an indirect experiment in the sense that it involves not uniform uniaxial tension but non-uniform triaxial stress states throughout the specimen —have to be appropriately interpreted to be useful. The main objective of this paper is to carry out a complete quantitative analysis of where and when fracture nucleates and propagates in a Brazilian test and thereby establish how to appropriately interpret its results. We do so by deploying the phase-field fracture theory of Kumar et al. (2020), which has been recently established as a complete theory of fracture capable of accurately describing the nucleation and propagation of cracks in linear elastic brittle materials under arbitrary quasistatic loading conditions. The last section of this paper puts forth a new protocol to deduce the tensile strength of a material from a Brazilian test that improves on the current ISRM and ASTM standards.
</details>
        

**A model-based simulation framework for coupled acoustics, elastodynamics, and damage with application to nano-pulse lithotripsy** (2024). _**Y. Liu**, P. Zhong, O. Lopez-Pamies, J. E. Dolbow_. _International Journal of Solids and Structures_ 289, 112626.
[![DOI: 10.1016/j.ijsolstr.2023.112626](https://img.shields.io/badge/DOI-10.1016/j.ijsolstr.2023.112626-blue.svg)](https://doi.org/10.1016/j.ijsolstr.2023.112626)

<details>
<summary>Abstract</summary>
We develop a model for solid objects surrounded by a fluid that accounts for the possibility of acoustic pressures giving rise to damage on the surface of the solid. The propagation of an acoustic pressure in the fluid domain is modeled by the acoustic wave equation. On the other hand, the response of the solid is described by linear elastodynamics coupled with a gradient damage model, one that is based on a cohesive-type phasefield description of fracture. The interaction between the acoustic pressure and the deformation and damage of the solid are represented by transmission conditions at the fluid–solid interface. The resulting governing equations are discretized using a finite-element/finite-difference method that pays particular attention to the spatial and temporal scales that need to be resolved. Results from model-based simulations are provided for a benchmark problem as well as for recent experiments in nano-pulse lithotripsy. A parametric study is performed to illustrate how damage develops in response to the driving force (magnitude and location of the acoustic source) as a function of the fracture resistance of the solid. The results are shown to be qualitatively consistent with experimental observations for the location and size of the damage fields on the solid surface. A study of limiting cases also suggests that both the threshold for damage and the critical fracture energy are important to consider in order to capture the transition from damage initiation to complete localization. A low-cycle fatigue model is proposed that degrades the fracture resistance of the solid as a function of accumulated tensile strain energy, and it is shown to be capable of capturing damage localization in simulations of multi-pulse nano-pulse lithotripsy.
</details>
        

**A computational framework for simulating crack nucleation and growth in materials subjected to dynamic loads** (2024). _**Y. Liu**_. _Duke University_ , 153.

<details>
<summary>Abstract</summary>
Understanding dynamic fracture is essential for predicting the structural integrity and lifespan of engineering components, especially in critical fields like aerospace, civil engineering, and materials manufacturing. Dynamic fracture involves crack propagation under rapid loading conditions, where the loading rate impacts the fracture process. Dynamic fracture is particularly important in scenarios such as impact, fragmentation, and high-speed machining, where materials are subjected to sudden and extreme forces. Both crack nucleation and propagation are crucial in dynamic fracture. The precise conditions under which cracks nucleate is the key to predict failure onset and implementing preventive measures. Once a crack has nucleated, its propagation under dynamic loading is also challenging due to complex stress wave interactions and inertial effects that influence the crack path and speed. Traditional fracture analysis methods often struggle to accurately predict crack behavior under these dynamic conditions.The research presented in this dissertation aims to address the aforementioned challenges. A unified computational framework is developed to simulate both crack nucleation and growth under dynamic loads. In essence, a phase-field model designed for fracture under quasi-static loading conditions is extended to account for dynamic fracture. The framework accounts for an arbitrary material strength surface through an external driving force in the evolution equation for the phase field. The framework is appealing because it models arbitrary material strength without compromising Griffith's criterion. The developed computational framework has been validated against a broad range of experimental observations, demonstrating the importance of accurately representing material strength. A complete analysis of fracture nucleation and propagation during the Brazilian test is presented; the framework also simulates coupled acoustics, elastodynamics, and damage with application to nano-pulse lithotripsy; and the framework has been validated against the impact experiments by Kalthoff and Winkler, a dynamic version of the Brazilian fracture test, and a recent experiment investigating crack initiation, propagation, and branching in soda-lime glass specimens.
</details>
        

**On the effects of material strength in dynamic fracture: A phase-field study** (2024). _**Y. Liu**, O. Lopez-Pamies, J. E. Dolbow_. _arXiv preprint_ , .
[![DOI: 10.48550/arXiv.2411.16393](https://img.shields.io/badge/DOI-10.48550/arXiv.2411.16393-blue.svg)](https://doi.org/10.48550/arXiv.2411.16393)

<details>
<summary>Abstract</summary>

Over the past seven years, full-field analyses of a wide range of classical as well as modern quasi-static fracture experiments on nominally elastic brittle materials -- ranging from hard ceramics to soft elastomers -- have repeatedly identified the material strength surface as one of the key material properties that governs not only the nucleation of cracks, but also their propagation. Central to these analyses are the results generated by the Griffith phase-field fracture theory with material strength introduced in [21,23,20]. The first of two objectives of this paper is to extend this theory to account for inertia, this for the basic case of isotropic linear elastic brittle materials. From an applications point of view, the theory amounts to solving an initial-boundary-value problem comprised of a hyperbolic PDE coupled with an elliptic PDE for the displacement field $u(X,t)$ and the phase field $d(X,t)$. A robust scheme is presented to generate solutions for these equations that is based on an adaptive finite-element discretization of space and an implicit finite-difference discretization of time. At every time increment tm, the resulting discretized equations are solved separately in a staggered manner for $u(X,t_m)$ and $d(X,t_m)$ by means of Newton-Raphson schemes. The second objective is to illustrate the descriptive and predictive capabilities of the proposed theory via simulations of benchmark problems and experiments. These include problems involving fracture nucleation from large pre-existing cracks, such as the classical Kalthoff-Winkler experiments, as well as problems involving fracture nucleation within the bulk, such as the dynamic Brazilian fracture experiments.

</details>
        

**Model-based simulations of pulsed laser ablation using an embedded finite element method** (2023). _**Y. Liu**, S. Claus, P. Kerfriden, J. Chen, P. Zhong, J. E. Dolbow_. _International Journal of Heat and Mass Transfer_ 204, 123843.
[![DOI: 10.1016/j.ijheatmasstransfer.2022.123843](https://img.shields.io/badge/DOI-10.1016/j.ijheatmasstransfer.2022.123843-blue.svg)](https://doi.org/10.1016/j.ijheatmasstransfer.2022.123843)

<details>
<summary>Abstract</summary>
A model of thermal ablation with application to multi-pulsed laser lithotripsy is presented. The approach is based on a one-sided Stefan-Signorini model for thermal ablation, and relies on a level-set function to represent the moving interface between the solid phase and a fictitious gas phase (representing the ablated material). The model is discretized with an embedded finite element method, wherein the interface geometry can be arbitrarily located relative to the background mesh. Nitsche's method is adopted to impose the Signorini condition on the moving interface. A bound constraint is also imposed to deal with thermal shocks that can arise during representative simulations of pulsed ablation with high-power lasers. We report simulation results based on experiments for pulsed laser ablation of wet BegoStone samples treated in air, where Begostone has been used as a phantom material for kidney stone. The model is calibrated against experimental measurements by adjusting the percentage of incoming laser energy absorbed at the surface of the stone sample. Simulation results are then validated against experimental observations for the crater area, volume, and geometry as a function of laser pulse energy and duration. Our studies illustrate how the spreading of the laser beam from the laser fiber tip with concomitantly reduced incident laser irradiance on the damaged crater surface explains trends in both the experimental observations and the model-based simulation results.
</details>
        

**Shock waves generated by toroidal bubble collapse are imperative for kidney stone dusting during Holmium:YAG laser lithotripsy** (2023). _G. Xiang, J. Chen, D. Ho, G. Sankin, X. Zhao, **Y. Liu**, K. Wang, J. Dolbow, J. Yao, P. Zhong_. _Ultrasonics Sonochemistry_ 101, 106649.
[![DOI: 10.1016/j.ultsonch.2023.106649](https://img.shields.io/badge/DOI-10.1016/j.ultsonch.2023.106649-blue.svg)](https://doi.org/10.1016/j.ultsonch.2023.106649)

<details>
<summary>Abstract</summary>
Holmium:yttrium-aluminum-garnet (Ho:YAG) laser lithotripsy (LL) has been the treatment of choice for kidney stone disease for more than two decades, yet the mechanisms of action are not completely clear. Besides photothermal ablation, recent evidence suggests that cavitation bubble collapse is pivotal in kidney stone dusting when the Ho:YAG laser operates at low pulse energy (Ep) and high frequency (F). In this work, we perform a comprehensive series of experiments and modelbased simulations to dissect the complex physical processes in LL. Under clinically relevant dusting settings (Ep = 0.2 J, F = 20 Hz), our results suggest that majority of the irradiated laser energy ({\textgreater}90 \%) is dissipated by heat generation in the fluid surrounding the fiber tip and the irradiated stone surface, while only about 1 \% may be consumed for photothermal ablation, and less than 0.7 \% is converted into the potential energy at the maximum bubble expansion. We reveal that photothermal ablation is confined locally to the laser irradiation spot, whereas cavitation erosion is most pronounced at a fiber tip-stone surface distance about 0.5 mm where multi foci ring-like damage outside the thermal ablation zone is observed. The cavitation erosion is caused by the progressively intensified collapse of jetinduced toroidal bubble near the stone surface ({\textless}100 μm), as a result of Raleigh-Taylor and Richtmyer-Meshkov instabilities. The ensuing shock wave-stone interaction and resultant leaky Rayleigh waves on the stone surface may lead to dynamic fatigue and superficial material removal under repeated bombardments of toroidal bubble collapses during dusting procedures in LL.
</details>
        

**Multiresponse shape-memory nanocomposite with a reversible cycle for powerful artificial muscles** (2021). _C. Chen, **Y. Liu**, X. He, H. Li, Y. Chen, Y. Wei, Y. Zhao, Y. Ma, Z. Chen, X. Zheng, H. Liu_. _Chem. Mater._ 33, 987--997.
[![DOI: 10.1021/acs.chemmater.0c04170](https://img.shields.io/badge/DOI-10.1021/acs.chemmater.0c04170-blue.svg)](https://doi.org/10.1021/acs.chemmater.0c04170)

<details>
<summary>Abstract</summary>
In the ﬁeld of bionic soft robots and microrobots, artiﬁcial muscle materials have exhibited unique potential for cutting-edge applications. However, current mainstream thermal-responsive artiﬁcial muscles based on semicrystalline polymers (SCPs), despite their excellent physical properties, suﬀer from the limitation of environmental stimuli in practice, while their photodriven counterparts adopting liquid crystal elastomers (LCEs) lack ductility. Herein, a novel multifunctional programmable artiﬁcial muscle with a unique patch-sewing structure formed by π−π stacking between azobenzene groups was designed, which combined the advantages of SCPs and LCEs. The nanocomposite demonstrated a unique combination between artiﬁcial muscle performance (46.5 times the energy density and 26.6 times the power density of human skeletal muscles) and programmability (274.84\% strain and 100\% shape-memory recovery rate within 1 s). Meanwhile, coupling the photoisomerization of azobenzene and the photothermal conversion of gold nanorods, the cycle of deformation triggered by ultraviolet light and restoring by infrared light could be accomplished rapidly within 30 s. A COMSOL Multiphysics model was established and the corresponding ﬁnite element analysis veriﬁed the photoactuation and captured the general principle of light initiation in elastomers. These demonstrate that the multifunctional programmable elastomer is promising for artiﬁcial muscle applications, especially for photoinduced actuation.
</details>
        

**A micromechanics-informed phase field model for brittle fracture accounting for unilateral constraint** (2020). _**Y. Liu**, C. Cheng, V. Ziaei-Rad, Y. Shen_. _Engineering Fracture Mechanics_ , 107358.
[![DOI: 10.1016/j.engfracmech.2020.107358](https://img.shields.io/badge/DOI-10.1016/j.engfracmech.2020.107358-blue.svg)](https://doi.org/10.1016/j.engfracmech.2020.107358)

<details>
<summary>Abstract</summary>
We propose a new direction-dependent model for the unilateral constraint involved in the phase field approach to fracture and also in the continuous damage mechanics models. The construction of this phase field model is informed by micromechanical modeling through the homogenization theory, where the representative volume element (RVE) has a planar crack in the center. The proposed model is made closely match the response of the RVE, including the frictionless self-contact condition. This homogenization approach allows to identify a direction-dependent phase field model with the tension-compression split obtained from cracked microstructures. One important feature of the proposed model is that unlike most other models, the material degradation is consistently determined without artificial assumptions or ad hoc parameters with no physical interpretation, thus, a more realistic modeling is resulted. With standard tests such as uniaxial loadings, three-point bending, simple shear, and through-crack tests, the proposed model predicts reasonable crack paths. Moreover, with the RVE response as a benchmark, the proposed model gives rise to an accurate stress-strain curve under shear loads, more accurate than most existing models.
</details>
        

**A manifold learning approach to accelerate phase field fracture simulations in the representative volume element** (2020). _**Y. Liu**, K. Weng, Y. Shen_. _SN Applied Sciences_ 2, 1682.

<details>
<summary>Abstract</summary>
The multiscale simulation of heterogeneous materials is a popular and important subject in solid mechanics and materials science due to the wide application of composite materials. However, the classical FE$^2$ (finite element$^2$) scheme can be costly, especially when the microproblem is nonlinear. In this paper, we consider the case when the microproblem is the phase field formulation for fracture. We adopt the locally linear embedding (LLE) manifold learning approach, a method for non-linear dimension reduction, to extract the manifold that contains a collection of phase-field-represented initial microcrack patterns in the representative volume element (RVE). Then the output data corresponding to any other microcrack pattern, e.g., the evolved phase field at a fixed load, can be accurately reconstructed using the learned manifold with minimum computation. The method has two features: a minimum number of parameters for the scheme, and an input-specific error bar. The latter feature enables an adaptive strategy for any new input on whether to use the proposed, less expensive reconstruction, or to use an accurate but costly high-fidelity computation instead.
</details>
        

## Presentations
**Virtual Damage Sensing Digital Twin for Piezocomposites Integrating Neural Operator with Parametrically Upscaled Constitutive Damage Model** (2026). _**Y. Liu**, S. Ghosh_. _[HEMI Day 2026](https://hemi.jhu.edu/event/hemi-day/)_ (Podium presentation), Baltimore, Maryland.

**A phase-field approach for the nucleation and propagation of dynamic cracks** (2024). _**Y. Liu**, O. Lopez-Pamies, J. E. Dolbow_. _The 16th World Congress on Computational Mechanics (WCCM16)_, Vancouver, Canada.

**The revisited phase-field approach to brittle fracture: application to the diametral compression and wing-crack problems** (2024). _A. Kumar, C. Liu, **Y. Liu**, J. Dolbow, O. Lopez-Pamies_. _The 16th World Congress on Computational Mechanics (WCCM16)_, Vancouver, Canada.

**A model-based simulation framework for coupled acoustics, elastodynamics, and damage with application to nano-pulse lithotripsy** (2023). _**Y. Liu**, P. Zhong, O. Lopez-Pamies, J. E. Dolbow_. _the 17th United States National Congress on Computational Mechanics (USNCCM17)_ (Poster and oral presentation), Albuquerque, New Mexico.

**Model-based simulations of pulsed laser ablation using a CutFEM method** (2022). _**Y. Liu**, S. Claus, P. Kerfriden, J. Chen, P. Zhong, J. E. Dolbow_. _The 15th World Congress on Computational Mechanics (WCCM15)_, Yokohama, Japan.

**A micromechanics-based phase field approach to fracture** (2019). _**Y. Liu**, C. Cheng, Y. Shen_. _The 2nd International Conference of Mechanics of Advanced Materials and Structures_, Nanjing, China.

**A manifold learning approach for multiscale phase field evolution for fracture** (2019). _**Y. Liu**, K. Weng, Y. Shen_. _The International Conference on Data Driven Computing and Machine Learning in Engineering_, Shanghai, China.

**A homogenization-based phase field approach to fracture** (2019). _**Y. Liu**, C. Cheng, Y. Shen_. _the 15th United States National Congress on Computational Mechanics (USNCCM15)_ (Poster and oral presentation), Austin, Texas.



