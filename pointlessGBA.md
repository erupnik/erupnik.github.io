


<h1 style="text-align: center;"> <em>Pointless</em> Global Bundle Adjustment with Relative Motions Hessians </h1>

<img src="/img/pba_toy_v3.png" alt="PBA pipeline" 
        width="400" 
        style="display: block; margin: 0 auto">


Figure. **Pointless BA pipeline**. We refine global camera poses (and thus the 3D structure) in global bundle adjustment by rigorously taking into account the stochastics of the relative motions. Our inputs are S relative motions rk,ck, their initial 3D similarity transformations lambda,alpha,beta relating them to the global frame, and initial global poses R,C^0.

# Abstract
Bundle adjustment (BA) is the standard way to optimise camera poses and to produce sparse representations of a scene. 
However, as the number of camera poses and features grows, refinement through bundle adjustment becomes inefficient. Inspired by global motion averaging methods, we propose a new bundle adjustment objective which does not rely on image features' reprojection errors yet maintains precision on par with classical BA. Our method averages over relative motions while implicitly incorporating the contribution of the structure in the adjustment. To that end, we weight the objective function by local hessian matrices -- a by-product of local bundle adjustments performed on relative motions (e.g., pairs or triplets) during the pose initialisation step. Such hessians are extremely rich as they encapsulate both the features' random errors and the geometric configuration between the cameras. These pieces of information propagated to the global frame help to guide the final optimisation in a more rigorous way.
   We argue that this approach is an upgraded version of the motion averaging approach and demonstrate its effectiveness on both photogrammetric datasets and computer vision benchmarks.

<h3>Code</h3>
[<img src="/img/github-mark.png"  width="50">](https://github.com/erupnik/pointlessGBA)

<h3>BibTeX Citation</h3>
<pre>@article{rupnik2023pgba,
   author = {Ewelina Rupnik and Marc Pierrot-Deseilligny},
   title = {Pointless Global Bundle Adjustment with Relative Motions Hessians},
   journal = {CVPR Photogrammetric Computer Vision Workshop},
   year = {2023}
}
</pre>
