# PoissonLikelihood

### *class* deepinv.optim.PoissonLikelihood(gain=1.0, bkg=0, denormalize=True)

Bases: [`DataFidelity`](https://deepinv.org/api/stubs/deepinv.optim.DataFidelity.html.md#deepinv.optim.DataFidelity)

Poisson negative log-likelihood.

$$
\datafid{z}{y} =  -y^{\top} \log(z+\beta)+1^{\top}z
$$

where $y$ are the measurements, $z$ is the estimated (positive) density and $\beta\geq 0$ is
an optional background level.

#### NOTE
The function is not Lipschitz smooth w.r.t. $z$ in the absence of background ($\beta=0$).

* **Parameters:**
  * **gain** ([*float*](https://docs.python.org/3.9/library/functions.html#float)) – gain of the measurement $y$. Default: 1.0.
  * **bkg** ([*float*](https://docs.python.org/3.9/library/functions.html#float)) – background level $\beta$. Default: 0.
  * **denormalize** ([*bool*](https://docs.python.org/3.9/library/functions.html#bool)) – if True, the measurement is multiplied by the gain. Default: True.

<a id="sphx-glr-backref-deepinv-optim-poissonlikelihood"></a>

## Examples using `PoissonLikelihood`:

<div class="sphx-glr-thumbnails">
<!-- thumbnail-parent-div-open --><div class="sphx-glr-thumbcontainer" tooltip="This example introduces the Richardson-Lucy algorithm for deconvolution in the blind setting, where both the underlying clean image and the blur kernel are unknown.">  <div class="sphx-glr-thumbnail-title">Blind Richardson-Lucy deconvolution</div>
</div><div class="sphx-glr-thumbcontainer" tooltip="This example demonstrates how to solve Poisson inverse problems using the Maximum-Likelihood Expectation-Maximization (MLEM) algorithm sheppMaximumLikelihoodReconstruction1982, also known as the Richardson-Lucy algorithm in the deconvolution setting richardsonBayesianBasedIterativeMethod1972,lucyIterativeTechniqueRectification1974.">  <div class="sphx-glr-thumbnail-title">Poisson Inverse Problems with Maximum-Likelihood Expectation-Maximization (MLEM)</div>
</div><div class="sphx-glr-thumbcontainer" tooltip="This demo shows how to define a non time-of-flight PET scanner, simulate measurements and reconstruct an image from them.">  <div class="sphx-glr-thumbnail-title">Positron emission tomography (PET) in 2D</div>
</div><div class="sphx-glr-thumbcontainer" tooltip="This demo shows how to define a non time-of-flight PET scanner, simulate measurements and reconstruct a volume from them.">  <div class="sphx-glr-thumbnail-title">Positron emission tomography (PET) in 3D</div>
</div><div class="sphx-glr-thumbcontainer" tooltip="This example reconstructs a 2D slice from the BrainWeb \`&lt;https://github.com/casperdcl/brainweb&gt;\`_ positron emission tomography (PET) dataset. The slice contains five hot lesions, we simulate a sinogram with deepinv.physics.PET and we compare standard PET reconstruction algorithms with methods that support penalized objective functions.">  <div class="sphx-glr-thumbnail-title">OSEM, BSREM and gradient descent for 2D BrainWeb PET</div>
</div><div class="sphx-glr-thumbcontainer" tooltip="This example reconstructs a volume from the BrainWeb \`&lt;https://github.com/casperdcl/brainweb&gt;\`_ positron emission tomography (PET) dataset. We compare standard PET reconstruction algorithms with methods that support penalized objective functions.">  <div class="sphx-glr-thumbnail-title">3D PET reconstruction with the Brainweb dataset</div>
</div><div class="sphx-glr-thumbcontainer" tooltip="This is a simple example to show how to use a mirror descent algorithm for solving an inverse problem with Poisson noise. See hurault2023convergent for more details.">  <div class="sphx-glr-thumbnail-title">Plug-and-Play algorithm with Mirror Descent for Poisson noise inverse problems.</div>
</div><div class="sphx-glr-thumbcontainer" tooltip="In this tutorial, we revisit the implementation of the DiffPIR diffusion algorithm for image reconstruction from zhu2023denoising. The full algorithm is implemented in deepinv.sampling.DiffPIR.">  <div class="sphx-glr-thumbnail-title">Implementing DiffPIR</div>
</div>
<!-- thumbnail-parent-div-close --></div>
