# Papers-of-Robust-ML
Related papers for robust machine learning (main focus on the application of computer vision).
 
# Statement
Since there are tens of new papers on adversarial examples in each conference and jounral, we are only able to update those we just read and consider as insightful.

It follows the idea of https://github.com/P2333/Papers-of-Robust-ML 

## Contents 
- <a href="#Adversarial Attack">Adversarial Attack</a><br>
- <a href="#Noisy Label">Noisy Label</a><br>
- <a href="#Transfer Learning">Transfer Learning</a><br>
- <a href="#General_training">General Defenses (training phase)</a><br>
- <a href="#General_inference">General Defenses (inference phase)</a><br>
- <a href="#Detection">Adversarial Detection</a><br>
- <a href="#Certified Defense and Model Verification">Certified Defense and Model Verification</a><br>
- <a href="#Theoretical">Theoretical Analysis</a><br>
- <a href="#Empirical">Empirical Analysis</a><br>
- <a href="#Reinforcement_Learning">Reinforcement Learning</a><br>
- <a href="#Poison_Attack">Poison Attack</a><br>
- <a href="#Federate_Learning">Federate_Learning</a><br>
- <a href="#Beyond_Safety">Beyond Safety (Adversarial for Good)</a><br>
- <a href="#Seminal_work">Seminal Work</a><br>
- <a href="#Benchmark_Datasets">Benchmark Datasets</a><br>

<a id='Adversarial Attack'></a>
* [Intriguing properties of neural networks ](https://arxiv.org/pdf/1312.6199.pdf)(ICLR 2014) <br/> This paper is the first work on adversarial examples with two contributions: 1) L-BFGS attack; 2) Adversarial examples is a phenomenon of "over-fitting".
* [Explaining and harnessing adversarial examples](https://arxiv.org/abs/1412.6572)(ICLR 2015) <br/> This paper is the seminal work on adversairl examples with two contributions: 1) Fast Gradient Sign Method Attack; 2) Adversariall examples is a phenomenon of "linerarity of DNN's decision boundary".
* [Towards Evaluating the Robustness of Neural Networks](https://arxiv.org/pdf/1608.04644.pdf)(IEEE SP 2017) <br/> This paper does some evaluation on robustness and postulates that the defense distillation is useless. Moreover, an optimization-base attack C&W attack method is proposed.
* [Generating Adversarial Examples with Adversarial Networks](https://arxiv.org/pdf/1801.02610)(IJCAI 2018) <br/> This paper proposes a method to generate adversarial examples with the GANs.
* [Wasserstein Adversarial Examples via Projected Sinkhorn Iterations](https://arxiv.org/pdf/1902.07906.pdf)(ICML 2019) <br/> Sinkhorn iteration is a concept of optimal transport theory. This paper is inspired by the concept to propose an adversarial example generation method based on the Wasserstein distance.
* [Robust Physical-World Attacks on Deep Learning Models](https://arxiv.org/abs/1707.08945)(CVPR 2018) <br/> This paper is a first work on the physical attack in autonomous driving. With an optimization scheme considering the lighting and printability change, the stop sign can be attacked as a targeted adversary class.
* [Spatially Transformed Adversarial Examples](https://arxiv.org/pdf/1801.02612)(ICLR 2018) <br/> This paper focuses on the generation of adversarial examples with the the spatial transformation instead of pixel value manipulation.
* [Adversarial Examples for Generative Models](https://arxiv.org/pdf/1702.06832.pdf)(IEEE SP 2018 Workshop) <br/> This paper present three classes of attacks on the VAE and VAE-GAN architectures and demonstrate them against networks trained on MNIST, SVHN and CelebA. Its first attack leverages classification-based adversaries by attaching a classifier to the trained encoder of the target generative model, which can then be used to in- directly manipulate the latent representation. Its second attack directly uses the VAE loss function to generate a target reconstruction image from the adversarial example. Its third attack moves beyond relying on classification or the standard loss for the gradient and directly optimizes against differences in source and target latent representations. 
* [Adversarial Attacks on Neural Network Policies](https://arxiv.org/pdf/1702.02284.pdf)(ICLR 2017 Workshop) <br/> This paper is the first work on the adversarial attack in reinforcement leearning.
* [Adversarial Examples for Semantic Segmentation and Object Detection](https://arxiv.org/pdf/1703.08603)(ICCV 2017) <br/> This paper proposes a method of Dense Adversary Generation (DAG), which generates a large family of adversarial examples, and applies to a wide range of state-of-the-art deep networks for segmentation and detection. 
* [Houdini: Fooling Deep Structured Prediction Models](https://arxiv.org/pdf/1707.05373v1.pdf)(arxiv 2017) <br/>> This paper introduces a novel flexible approach named Houdini for generating adversarial examples specifically tailored for the final performance measure of the task considered, be it combinatorial and non-decomposable.
* [Transferability in Machine Learning: from Phenomena to Black-Box Attacks using Adversarial Samples](https://arxiv.org/abs/1605.07277)(arxiv 2016) <br/> This paper defines intra-technique transferability and cross-technique transferability. It firstly trains a substitute model, and craft adversarial examples against the substitute, and transfer them to a victim model. Then uses the victim model as an oracle to label a synthetic training set for the substitute. It also utilizes an effective data augmentation method with the reservoir sampling.
* [Exploring the Space of Black-box Attacks on Deep Neural Networks](https://arxiv.org/abs/1712.09491)(arxiv 2017) <br/> This paper finds that adversarial subspaces with higher dimensionality are more likely to intersect.
* [Decision-Based Adversarial Attacks: Reliable Attacks Against Black-Box Machine Learning Models](https://arxiv.org/abs/1712.04248)(ICLR 2018) <br/> This paper proposes a method that it would directly attack on the decision of the model which do not depend on the gradient or score.
<a id='Transfer Learning'></a>
## Transfer Learning
* [Do Better ImageNet Models Transfer Better?](https://openaccess.thecvf.com/content_CVPR_2019/papers/Kornblith_Do_Better_ImageNet_Models_Transfer_Better_CVPR_2019_paper.pdf)(CVPR 2019) <br/> This paper inspects the down-stream tasks in the computer vision which is pre-trained on ImageNet and obtains three conclusions: 1) The features learned by ImageNet is beneficial to some other computer vision tasks; 2) The regularization method utilized in the recognition task of ImageNet dataset is not so useful to transfer learning; 3) Fine-tuning on the task of fine-grained recognition does not surpass training from scratch.
* [Do ImageNet Classifiers Generalize to ImageNet?](https://openreview.net/pdf?id=cwj2tCVncS)(ICML 2019) <br/> The empirical result of this paper suggests that the accuracy drop is not caused by the adaptivity, but by the models??? inability to generalize to slightly ???harder??? images than those found in the original test sets.
<a id='Noisy Label'></a>
## Noisy Label
* [Re-Labeling ImageNet: From Single to Multi-Labels, From Global to Localized Labels](https://openaccess.thecvf.com/content/CVPR2021/papers/Yun_Re-Labeling_ImageNet_From_Single_to_Multi-Labels_From_Global_to_Localized_CVPR_2021_paper.pdf)(CVPR 2021) <br/> This paper propose a method to boost the quality of the labelling so that the generalization ability can be improved.
* [Pervasive Label Errors in Test Sets Destabilize Machine Learning Benchmarks](https://openreview.net/pdf?id=XccDXrDNLek)(NeurIPS 2021) <br/> This paper evaluates the labeling qulity of 10 famous datasets and points out the error of dataset.
* [Are we done with ImageNet](https://arxiv.org/pdf/2006.07159)(arxiv) <br/> The authors query the current procedure of the production on the ImageNet dataset and develop a new procedure.
* [Evaluating Machine Accuracy on ImageNet](http://proceedings.mlr.press/v119/shankar20c/shankar20c.pdf)(ICML 2020) <br/> This paper evaluates the machine accuracy on ImageNet and points out several directions including measure multi-label accuracy, the performance evaluaation to the distribution shift, and care on the performance of inanimate object.
* [ConvNets and ImageNet Beyond Accuracy: Understanding Mistakes and Uncovering Biases](https://openaccess.thecvf.com/content_ECCV_2018/papers/Pierre_Stock_ConvNets_and_ImageNet_ECCV_2018_paper.pdf)(ECCV 2018) <br/> This paper proves that the performance of SOTA models on Imagenet is underestimated which leaves little room for improvement and calls for new large-scale benchmarks involving for example multi-label annotations.
* [From ImageNet to Image Classi???cation:Contextualizing Progress on Benchmarks](https://arxiv.org/pdf/2005.11295.pdf)(ICML 2020) <br/> This paper develops a methodology for obtaining ???ne-grained data annotations via large-scale human studies to build data-centric robust system.

<a id='General_training'></a>
## General Defenses (training phase)
* [](https://openreview.net/pdf?id=SkgVRiC9Km)(arxiv 2018) <br/> This paper suggests a method for defending against adversarial examples and out-of-distribution samples via projection onto the data manifold. The paper suggests a new method for detecting when hidden layers are off of the manifold, and uses auto encoders to map them back onto the manifold. 

* [Research on the relationship between prediction uncertainty and adversarial robustness (Chinese)](http://www.jos.org.cn/jos/article/abstract/6163)(Journal of Software 2022) <br/> This paper demonstrates the relationship between uncertainty and robustness. A counter-intuitive conclusion is delivered that the adversarial robustness is positive-correlated with uncertainty. If the information entropy of the model output is maximized while training the model, the classification surface of the model can be more balanced to enhance the adversarial robustness.

* [PeerNets: Exploiting Peer Wisdom Against Adversarial Attacks](https://arxiv.org/abs/1806.00088)(ICLR 2019) <br/> This paper introduces Peer-Regularized networks (PeerNet) to perform non-local forward propagation. The novelty lies in alternating classical Euclidean convolutions with graph convolutions to harness information from a graph of peer samples.

* [Distillation as a Defense to Adversarial Perturbations against Deep Neural Networks](https://arxiv.org/pdf/1511.04508.pdf)(SP 2016) <br/> This paper proposes a defense method based on knowledge distillation which is controversial on the adaptive attack.

* [Stable Neural ODE with Lyapunov-Stable Equilibrium Points for Defending Against Adversarial Attacks](https://openreview.net/pdf?id=9CPc4EIr2t1) (NeurIPS 2021) <br/> This paper combines the stable conditions in control theory into neural ODE to induce locally stable models. 

* [Adversarial Training with Rectified Rejection](https://arxiv.org/pdf/2105.14785.pdf) <br/> This paper proposes a coupling rejection strategy, where two simple but well-designed rejection metrics can be coupled to provabably distinguish any misclassified sample from correclty classified ones.

* [Fixing Data Augmentation to Improve Adversarial Robustness](https://arxiv.org/pdf/2103.01946.pdf) <br/> This paper shows that after applying weight moving average, data augmentation (either by transformatons or generative models) can further improve robustness of adversarial training.

* [Improving Adversarial Robustness Using Proxy Distributions](https://arxiv.org/pdf/2104.09425.pdf) <br/> This paper verifies that leveraging more data sampled from a (high-quality) generative model that was trained on the same dataset (e.g., CIFAR-10) can still improve robustness of adversarially trained models, without using any extra data.

* [Towards Robust Neural Networks via Close-loop Control](https://openreview.net/forum?id=2AL06y9cDE-) (ICLR 2021) <br/> This paper introduce a close-loop control framework to enhance adversarial robustness of trained networks.

* [Understanding and Improving Fast Adversarial Training](https://arxiv.org/pdf/2007.02617.pdf) (NeurIPS 2020) <br/> A systematic study of catastrophic overfitting in adversarial training, its reasons, and ways of resolving it. The proposed regularizer, *GradAlign*, helps to prevent catastrophic overfitting and scale FGSM training to high Linf-perturbations.

* [Confidence-Calibrated Adversarial Training: Generalizing to Unseen Attacks](https://arxiv.org/pdf/1910.06259.pdf) (ICML 2020) <br/> This paper uses a perturbation-dependent label smoothing method to generalize adversarially trained models to unseen attacks.

* [Smooth Adversarial Training](https://arxiv.org/pdf/2006.14536.pdf) <br/> This paper advocate using smooth variants of ReLU during adversarial training, which can achieve state-of-the-art performance on ImageNet.  

* [Rethinking Softmax Cross-Entropy Loss for Adversarial Robustness](https://openreview.net/forum?id=Byg9A24tvB) (ICLR 2020) <br/> This paper rethink the drawbacks of softmax cross-entropy in the adversarial setting, and propose the MMC method to induce high-density regions in the feature space.

* [Jacobian Adversarially Regularized Networks for Robustness](https://openreview.net/pdf?id=Hke0V1rKPS) (ICLR 2020) <br/> This paper propose to show that a generally more interpretable model could potentially be more robust against adversarial attacks.

* [Fast is better than free: Revisiting adversarial training](https://openreview.net/forum?id=BJx040EFvH&noteId=BJx040EFvH) (ICLR 2020) <br/> This paper proposes several tricks to make FGSM-based adversarial training effective.

* [Adversarial Training and Provable Defenses: Bridging the Gap](https://openreview.net/forum?id=SJxSDxrKDr) (ICLR 2020) <br/> This paper proposes the layerwise adversarial training method, which gradually optimizes on the latent adversarial examples from low-level to high-level layers.

* [Improving Adversarial Robustness Requires Revisiting Misclassified Examples](https://openreview.net/forum?id=rklOg6EFwS) (ICLR 2020) <br/> This paper proposes a new method MART, which involves a boosted CE loss to further lower down the second-maximal prediction, and a weighted KL term (similar as a focal loss), compared to the formula of TRADES.

* [Adversarial Interpolation Training: A Simple Approach for Improving Model Robustness](https://openreview.net/forum?id=Syejj0NYvr&noteId=r1e432RzoS) <br/> This paper introduces the mixup method into adversarial training to improve the model performance on clean images.

* [Are labels required for improving adversarial robustness?](https://arxiv.org/pdf/1905.13725.pdf) (NeurIPS 2019) <br/> This paper exploit unlabeled data to better improve adversarial robustness.

* [Adversarial Robustness through Local Linearization](https://arxiv.org/pdf/1907.02610.pdf) (NeurIPS 2019) <br/> This paper introduce local linearization in adversarial training process.

* [Provably Robust Boosted Decision Stumps and Trees against Adversarial Attacks](https://arxiv.org/pdf/1906.03526.pdf) (NeurIPS 2019) <br/> A method to efficiently certify the robustness of GBDTs and to integrate the certificate into training (leads to an upper bound on the worst-case loss). The obtained certified accuracy is higher than for other robust GBDTs and is competitive to provably robust CNNs.

* [You Only Propagate Once: Accelerating Adversarial Training via Maximal Principle](https://arxiv.org/pdf/1905.00877.pdf) (NeurIPS 2019) <br/> This paper provides a fast method for adversarial training from the perspective of optimal control.

* [Adversarial Training for Free!](https://arxiv.org/pdf/1904.12843.pdf) (NeurIPS 2019) <br/> A fast method for adversarial training, which shares the back-propogation gradients of updating weighs and crafting adversarial examples.

* [ME-Net: Towards Effective Adversarial Robustness with Matrix Estimation](https://arxiv.org/abs/1905.11971) (ICML 2019) <br/> This paper demonstrates the global low-rank structures within images, and leverages matrix estimation to exploit such underlying structures for better adversarial robustness.

* [Using Pre-Training Can Improve Model Robustness and Uncertainty](https://arxiv.org/abs/1901.09960) (ICML 2019) <br/>
This paper shows adversarial robustness can transfer and that adversarial pretraining can increase adversarial robustness by ~10% accuracy.

* [Theoretically Principled Trade-off between Robustness and Accuracy](https://arxiv.org/pdf/1901.08573.pdf) (ICML 2019) <br/> A variant of adversarial training: TRADES, which won the defense track of NeurIPS 2018 Adversarial Competation.

* [Robust Decision Trees Against Adversarial Examples](http://web.cs.ucla.edu/~chohsieh/ICML_2019_TreeAdvAttack.pdf) (ICML 2019) <br/> A method to enhance the robustness of tree models, including GBDTs.

* [Improving Adversarial Robustness via Promoting Ensemble Diversity](https://arxiv.org/pdf/1901.08846.pdf) (ICML 2019) <br/> Previous work constructs ensemble defenses by individually enhancing each memeber and then directly average the predictions. In this work, the authors propose the adaptive diversity promoting (ADP) to further improve the robustness by promoting the ensemble diveristy, as an orthogonal methods compared to other defenses.

* [Feature Denoising for Improving Adversarial Robustness](https://arxiv.org/pdf/1812.03411.pdf) (CVPR 2019) <br/> This paper applies non-local neural network and large-scale adversarial training with 128 GPUs (with training trick in 'Accurate, large minibatch SGD: Training ImageNet in 1 hour'), which shows large improvement than previous SOTA trained with 50 GPUs.

* [Improving the Generalization of Adversarial Training with Domain Adaptation](https://arxiv.org/pdf/1810.00740.pdf) (ICLR 2019) <br/> This work proposes to use additional regularization terms to match the domains between clean and adversarial logits in adversarial training.

* [A Spectral View of Adversarially Robust Features](http://papers.nips.cc/paper/8217-a-spectral-view-of-adversarially-robust-features.pdf) (NeurIPS 2018) <br/> Given the entire dataset X, use the eigenvectors of spectral graph as robust features. [[Appendix](http://papers.nips.cc/paper/8217-a-spectral-view-of-adversarially-robust-features-supplemental.zip)]

* [Adversarial Logit Pairing](https://arxiv.org/pdf/1803.06373.pdf) <br/> Adversarial training by pairing the clean and adversarial logits.

* [Deep Defense: Training DNNs with Improved Adversarial Robustness](http://papers.nips.cc/paper/7324-deep-defense-training-dnns-with-improved-adversarial-robustness.pdf) (NeurIPS 2018) <br/> They follow the linear assumption in DeepFool method. DeepDefense pushes decision boundary away from those correctly classified, and pull decision boundary closer to those misclassified.

* [Max-Mahalanobis Linear Discriminant Analysis Networks](http://proceedings.mlr.press/v80/pang18a/pang18a.pdf) (ICML 2018) <br/> This is one of our work. We explicitly model the feature distribution as a Max-Mahalanobis distribution (MMD), which has max margin among classes and can lead to guaranteed robustness.

* [Ensemble Adversarial Training- Attacks and Defenses](https://arxiv.org/pdf/1705.07204.pdf) (ICLR 2018) <br/> Ensemble adversarial training use sevel pre-trained models, and in each training batch, they randomly select one of the currently trained model or pre-trained models to craft adversarial examples.

* [Pixeldefend: Leveraging generative models to understand and defend against adversarial examples](https://arxiv.org/abs/1710.10766) (ICLR 2018) <br/> This paper provided defense by moving adversarial examples back towards the distribution seen in the training data.

<a id='General_inference'></a>
## General Defenses (inference phase)
* [Adversarial Attacks are Reversible with Natural Supervision](https://arxiv.org/abs/2103.14222) (ICCV 2021) <br/> This paper proposes to use contrastive loss to restore the natural structure of attacked images, providing a defense.

* [Adversarial Purification with Score-based Generative Models](https://arxiv.org/pdf/2106.06041.pdf) (ICML 2021) <br/> This paper proposes to use score-based generative models (e.g., NCSN) to purify adversarial examples.

* [Online Adversarial Purification based on Self-Supervision](https://arxiv.org/abs/2101.09387) (ICLR 2021) <br/> This paper proposes to train the network with a label-independent auxiliary task (e.g., rotation prediction), and purify the test inputs dynamically by minimizing the auxiliary loss.

* [Mixup Inference: Better Exploiting Mixup to Defend Adversarial Attacks](https://openreview.net/forum?id=ByxtC2VtPB) (ICLR 2020) <br/> This paper exploit the mixup mechanism in the inference phase to improve robustness.

* [Barrage of Random Transforms for Adversarially Robust Defense](http://openaccess.thecvf.com/content_CVPR_2019/papers/Raff_Barrage_of_Random_Transforms_for_Adversarially_Robust_Defense_CVPR_2019_paper.pdf) (CVPR 2019) <br/> This paper applies a set of different random transformations as an off-the-shelf defense.

* [Mitigating Adversarial Effects Through Randomization](https://arxiv.org/pdf/1711.01991.pdf) (ICLR 2018) <br/> Use random resizing and random padding to disturb adversarial examples, which won the 2nd place in th defense track of NeurIPS 2017 Adversarial Competation.

* [Countering Adversarial Images Using Input Transformations](https://arxiv.org/pdf/1711.00117.pdf) (ICLR 2018) <br/> Apply bit-depth reduction, JPEG compression, total variance minimization and image quilting as input preprocessing to defend adversarial attacks.

<a id='Detection'></a>
## Adversarial Detection
* [Characterizing Adversarial Subspaces Using Local Intrinsic Dimensionality]( https://arxiv.org/abs/1801.02613)(ICLR 2018) <br/> This paper demonstrates that the Local Intrinsic Dimensionalty can help detect the adversarial examples.

* [Characterizing Adversarial Examples Based on Spatial Consistency Information for Semantic Segmentation]()(ECCV 2018) <br/> In the task of semantic segmentation, this paper applies spatial consistency information analysis to recognize adversarial examples in segmentation.

* [SaftyNet: Detecting and Rejecting Adversarial Examples Robustly](https://openaccess.thecvf.com/content_ICCV_2017/papers/Lu_SafetyNet_Detecting_and_ICCV_2017_paper.pdf)(ICCV 2017) <br/> Based on the hypothesis that adversarial attacks work by producing different patterns of activation in late stage ReLUs to those produced by natural examples, this paper quantizes each ReLU at some set of thresholds to generate a discrete code (binarized code in the case of one threshold). This paper also proposes the SceneProof application it is possible to check whether a pair of image and depth map is consistent or not.

* [Class-Disentanglement and Applications in Adversarial Detection and Defense](https://openreview.net/pdf?id=jFMzBeLyTc0) (NeurIPS 2021) <br/> This paper proposes to disentangle the class-dependence and visually reconstruction, and exploit the result as an adversarial detection metric.

* [Adversarial Training with Rectified Rejection](https://arxiv.org/pdf/2105.14785.pdf) <br/> This paper proposes a coupling rejection strategy, where two simple but well-designed rejection metrics can be coupled to provabably distinguish any misclassified sample from correclty classified ones.

* [Towards Robust Detection of Adversarial Examples](http://papers.nips.cc/paper/7709-towards-robust-detection-of-adversarial-examples.pdf) (NeurIPS 2018) <br/> This is one of our work. We train the networks with reverse cross-entropy (RCE), which can map normal features to low-dimensional manifolds, and then detectors can better separate between adversarial examples and normal ones.

* [A Simple Unified Framework for Detecting Out-of-Distribution Samples and Adversarial Attacks](http://papers.nips.cc/paper/7947-a-simple-unified-framework-for-detecting-out-of-distribution-samples-and-adversarial-attacks.pdf) (NeurIPS 2018) <br/> Fit a GDA on learned features, and use Mahalanobis distance as the detection metric.

* [Robust Detection of Adversarial Attacks by Modeling the Intrinsic Properties of Deep Neural Networks](http://papers.nips.cc/paper/8016-robust-detection-of-adversarial-attacks-by-modeling-the-intrinsic-properties-of-deep-neural-networks.pdf) (NeurIPS 2018) <br/> They fit a GMM on learned features, and use the probability as the detection metric.

* [Detecting adversarial samples from artifacts](https://arxiv.org/abs/1703.00410) <br/> This paper proposed the kernel density (K-density) metric on the learned features to detect adversarial examples.

<a id='Certified Defense and Model Verification'></a>
## Certified Defense and Model Verification
* [Certi???ed Adversarial Robustness via Randomized Smoothing](https://arxiv.org/abs/1902.02918)(ICML 2019) <br/> This paper utilizes randomized smoothing to train state-of-the-art certi???ably L2-robust ImageNet classi???ers.

* [Towards Better Understanding of Training Certifiably Robust Models against Adversarial Examples](https://openreview.net/pdf?id=b18Az57ioHn) (NeurIPS 2021) <br/>  This paper generally study the effciency of different certified defenses, and find that the smoothness of loss landscape matters.

* [Towards Verifying Robustness of Neural Networks against Semantic Perturbations](https://arxiv.org/abs/1912.09533) (CVPR 2020) <br/> This paper generalize the pixel-wise verification methods into the semantic transformation space.

* [Neural Network Branching for Neural Network Verification](https://arxiv.org/abs/1912.01329) (ICLR 2020) <br/> This paper use GNN to adaptively construct branching strategy for model verification.

* [Towards Stable and Efficient Training of Verifiably Robust Neural Networks](https://openreview.net/forum?id=Skxuk1rFwB) (ICLR 2020) <br/> This paper combines the previous IBP and CROWN methods.

* [A Convex Relaxation Barrier to Tight Robustness Verification of Neural Networks](http://papers.nips.cc/paper/9176-a-convex-relaxation-barrier-to-tight-robustness-verification-of-neural-networks.pdf) (NeurIPS 2019) <br/> This paper makes a conprehensive studies on existing robustness verification methods based on convex relaxation.

* [Tight Certificates of Adversarial Robustness for Randomly Smoothed Classifiers](https://guanghelee.github.io/pub/Lee_etal_neurips19.pdf) (NeurIPS 2019) <br/> This word extends the robustness certificate of random smoothing from L2 to L0 norm bound.

* [On the Effectiveness of Interval Bound Propagation for Training Verifiably Robust Models](https://arxiv.org/pdf/1810.12715.pdf) (ICCV 2019) <br/> This paper proposes the scalable verificatin method with interval bound propagation (IBP).

* [Evaluating Robustness of Neural Networks with Mixed Integer Programming](https://arxiv.org/abs/1711.07356) (ICLR 2019) <br/> This paper use mixed integer programming (MIP) method to solve the verification problem.

* [Efficient Neural Network Robustness Certification with General Activation Functions](https://arxiv.org/abs/1811.00866) (NeurIPS 2018) <br/> This paper proposes the verification method CROWN for general activation with locally linear or quadratic approximation.

* [A Unified View of Piecewise Linear Neural Network Verification](https://arxiv.org/abs/1711.00455) (NeurIPS 2018) <br/> This paper presents a unified framework and an empirical benchmark on previous verification methods

* [Scaling Provable Adversarial Defenses](http://papers.nips.cc/paper/8060-scaling-provable-adversarial-defenses.pdf) (NeurIPS 2018) <br/> They add three tricks to improve the scalability (to CIFAR-10) of previously proposed method in ICML.

* [Provable Defenses against Adversarial Examples via the Convex Outer Adversarial Polytope](https://arxiv.org/pdf/1711.00851.pdf) (ICML 2018) <br/> By robust optimization (via a linear program of convex outer approximation), they can get a point-wise bound of robustness, where no adversarial example exists in the bound. Experiments are done on MNIST, Fashion-MNIST, HAR, and SVHN.

* [Towards Fast Computation of Certified Robustness for ReLU Networks](https://arxiv.org/abs/1804.09699) (ICML 2018) <br/> This paper proposes the Fast-Lin and Fast-Lip methods.

* [Evaluating the Robustness of Neural Networks: An Extreme Value Theory Approach](https://arxiv.org/abs/1801.10578) (ICLR 2018) <br/> This paper proposes the CLEVER method to estimate the upper bound of specification.

* [Certified Defenses against Adversarial Examples](https://arxiv.org/abs/1801.09344) (ICLR 2018) <br/> This paper proposes the certified training with semidefinite relaxation to realize the boosting of robustness on the adaptive regularization.

* [A Dual Approach to Scalable Verification of Deep Networks](https://arxiv.org/abs/1803.06567) (UAI 2018) <br/> This paper solves the dual problem to provide an upper bound of the primary specification problem for verification.

* [Reluplex: An efficient SMT solver for verifying deep neural networks](https://arxiv.org/pdf/1702.01135.pdf) (CAV 2017) <br/> This paper use satisfiability modulo theory (SMT) solvers for the verification problem.

* [Automated Verification of Neural Networks: Advances, Challenges and Perspectives](https://arxiv.org/pdf/1805.09938.pdf) <br/> This paper provides an overview of main verification methods, and introduces previous work on combining automated verification with machine learning. They also give some insights on future tendency of the combination between these two domains.

<a id='Theoretical'></a>
## Theoretical Analysis
* [Unlabeled Data Improves Adversarial Robustness](https://arxiv.org/abs/1905.13736)(NeurIPS 2019) <br/> This is a seminal theoretical work led by Percy to prove that semi-supervised learning is effective to promote the adversarial robustness. 

* [Are Labels Required for Improving Adversarial Robustness?]()(NeurIPS 2019)

* [Parseval Networks: Improving Robustness to Adversarial Examples](http://proceedings.mlr.press/v70/cisse17a/cisse17a.pdf)(ICML 2017) <br/> This paper proposes a method to boost the robustness with L2 regularization and deliver a layer-wise theoretical analysis.

* [Lower bounds on the robustness to adversarial perturbations](https://papers.nips.cc/paper/2017/file/298f95e1bf9136124592c8d4825a06fc-Paper.pdf)(NeurIPS 2017) <br/> This paper demonstrates a methodd to limit the possible layer-wise norm expansions in a variety of different layer types. It is a seminal work on the robustness analysis of convolutional neural network. 

* [Towards Deep Learning Models Resistant to Large Perturbations](https://arxiv.org/pdf/2003.13370.pdf) <br/> This paper prove that the weight initialization of a already robust model on small perturbation can be helpful for training on large perturbations.

* [Improved Sample Complexities for Deep Neural Networks and Robust Classification via an All-Layer Margin](https://openreview.net/forum?id=HJe_yR4Fwr) (ICLR 2020) <br/> This paper connect the generalization gap w.r.t all-layer margin, and propose a variant of adversarial training, where the perturbations can be imposed on each layer in network.

* [Adversarial Examples Are Not Bugs, They Are Features](https://arxiv.org/pdf/1905.02175.pdf) (NeurIPS 2019) <br/> They claim that adversarial examples can be directly attributed to the presence of non-robust features, which are highly predictive but locally quite sensitive.

* [First-order Adversarial Vulnerability of Neural Networks and Input Dimension](https://arxiv.org/pdf/1802.01421.pdf) (ICML 2019) <br/> This paper demonsrate the relations among adversarial vulnerability and gradient norm and input dimension with comprehensive empirical experiments.

* [Adversarial Examples from Computational Constraints](https://arxiv.org/pdf/1805.10204.pdf) (ICML 2019) <br/> The authors argue that the exsitence of adversarial examples could stem from computational constrations.

* [Adversarial Examples Are a Natural Consequence of Test Error in Noise](https://arxiv.org/pdf/1901.10513.pdf) (ICML 2019) <br/> This paper connects the relation between the general corruption robustness and the adversarial robustness, and recommand the adversarial defenses methods to be also tested on general-purpose noises.

* [PAC-learning in the presence of evasion adversaries](https://arxiv.org/pdf/1806.01471.pdf) (NeurIPS 2018) <br/> The authors analyze the adversarial attacks from the PAC-learning framework.

* [Adversarial Vulnerability for Any Classifier](http://papers.nips.cc/paper/7394-adversarial-vulnerability-for-any-classifier.pdf) (NeurIPS 2018) <br/> Uniform upper bound of robustness for any classifier on the data sampled from smooth genertive models.

* [Adversarially Robust Generalization Requires More Data](http://papers.nips.cc/paper/7749-adversarially-robust-generalization-requires-more-data.pdf) (NeurIPS 2018) <br/> The setting of this paper is choosen to model the empirical observation that adversarial generalization may require more data than natural generalization. 

* [Are Labels Required for Improving Adversarial Robustness?](https://arxiv.org/pdf/1905.13725.pdf)(NeurIPS 2019) <br> This is the argumentative work of the work "Adversarially Robust Generalization Requires More Data" to save the economical cost of semi-supervised learning for the robustness improvement.

* [Robustness of Classifiers:from Adversarial to Random Noise](http://papers.nips.cc/paper/6331-robustness-of-classifiers-from-adversarial-to-random-noise.pdf) (NeurIPS 2016)

<a id='Empirical'></a>
## Empirical Analysis
* [How Benign is Benign Overfitting](https://openreview.net/pdf?id=g-wu9TMPODo) (ICLR 2021) <br/> This paper shows that adversarial vulnerability may come from bad
data and (poorly) trained models, namely, learned representations.

* [Uncovering the Limits of Adversarial Training against Norm-Bounded Adversarial Examples](https://arxiv.org/abs/2010.03593) <br/> This paper explores the limits of adversarial training on CIFAR-10 by applying large model architecture, weight moving average, smooth activation and more training data to achieve SOTA robustness under norm-bounded constraints.

* [Bag of Tricks for Adversarial Training](https://openreview.net/forum?id=Xb8xvrtB8Ce) (ICLR 2021) <br/> This paper provides an empirical study on the usually overlooked hyperparameters used in adversarial training, and show that inappropriate settings can largely affect the performance of adversarially trained models.

* [Neural Anisotropy Directions](https://arxiv.org/pdf/2006.09717.pdf) (NeurIPS 2020) <br/> This paper shows that there exist directional inductive biases of model architectures, which can explain the model reaction against certain adversarial perturbation.

* [Hold me tight! Influence of discriminative features on deep network boundaries](https://arxiv.org/abs/2002.06349) (NeurIPS 2020) <br/> This paper empirically shows that decision boundaries are constructed along discriminative features, and explain the mechanism of adversarial training.

* [Reliable evaluation of adversarial robustness with an ensemble of diverse parameter-free attacks](https://arxiv.org/abs/2003.01690) (ICML 2020) <br/> An comprehensive empirical evaluations on some of the existing defense methods. 

* [Attacks Which Do Not Kill Training Make Adversarial Learning Stronger](https://arxiv.org/pdf/2002.11242.pdf) (ICML 2020) <br/> This paper also advovate for early-stop during adversarial training.

* [Overfitting in adversarially robust deep learning](https://arxiv.org/pdf/2002.11569.pdf) (ICML 2020) <br/> This paper shows the phenomena of overfitting when training robust models with sufficient empirical experiments (codes provided in paper).

* [When NAS Meets Robustness: In Search of Robust Architectures against Adversarial Attacks](https://arxiv.org/abs/1911.10695) <br/> This paper leverages NAS to understand the influence of network architectures against adversarial attacks. It reveals several useful observations on designing robust network architectures.

* [Adversarial Examples Improve Image Recognition](https://arxiv.org/pdf/1911.09665.pdf) <br/> This paper shows that an auxiliary BN for adversarial examples can improve generalization performance.

* [Intriguing Properties of Adversarial Training at Scale](https://openreview.net/forum?id=HyxJhCEFDS&noteId=rJxeamAAKB) (ICLR 2020) <br/> This paper investigates the effects of BN and deeper models for adversarial training on ImageNet.

* [A Fourier Perspective on Model Robustness in Computer Vision](https://papers.nips.cc/paper/9483-a-fourier-perspective-on-model-robustness-in-computer-vision.pdf) (NeurIPS 2019) <br/> This paper analyzes different types of noises (including adversarial ones) from the Fourier perspective, and observes some relationship between the robustness and the Fourier frequency. 

* [Interpreting Adversarially Trained Convolutional Neural Networks](https://arxiv.org/pdf/1905.09797.pdf) (ICML 2019) <br/> This paper show that adversarial trained models can alleviate the texture bias and learn a more shape-biased representation.

* [On Evaluating Adversarial Robustness](https://arxiv.org/pdf/1902.06705.pdf) <br/> Some analyses on how to correctly evaluate the robustness of adversarial defenses.

* [Is Robustness the Cost of Accuracy? -- A Comprehensive Study on the Robustness of 18 Deep Image Classification Models](https://openaccess.thecvf.com/content_ECCV_2018/html/Dong_Su_Is_Robustness_the_ECCV_2018_paper.html) <br/> This paper empirically studies the effects of model architectures (trained on ImageNet) on robustness and accuracy.

* [Adversarial Example Defenses: Ensembles of Weak Defenses are not Strong](https://arxiv.org/pdf/1706.04701.pdf) <br/> This paper tests some ensemble of existing detection-based defenses, and claim that these ensemble defenses could still be evaded by white-box attacks.

<a id='Reinforcement_Learning'></a>
## Reinforcement Learning
* [Certifiable Robustness to Adversarial State Uncertainty in Deep Reinforcement Learning](https://ieeexplore.ieee.org/document/9354500)(TNNLLS 2021) <br/> This paper leverages research on certified adversarial robustness to develop an online certifiably robust for deep reinforcement learning algorithms. The proposed defense computes guaranteed lower bounds on state-action values during execution to identify and choose a robust action under a worst case deviation in input space due to possible adversaries or noise.

* [Adversarially Robust Policy Learning: Active Construction of Physically-Plausible Perturbations](http://vision.stanford.edu/pdf/mandlekar2017iros.pdf)(IROS 2017) <br/> This paper introduces Adversarially Robust Policy Learning (ARPL), an algorithm that leverages active computation of physically-plausible adversarial examples during training to enable robust policy learning in the source domain and robust performance under both random and adversarial input perturbations.

* [Robust Adversarial Reinforcement Learning](https://arxiv.org/pdf/1703.02702.pdf)(ICML 2017) <br/> This paper advocates a two-pronged approach with adversarial agents for modeling disturbances and adversaries with the incorporation of the domain knowledge to deliver the policy robust to uncertainties and model initializations.

<a id='Poison_Attack'></a>
## Poison Attack
* [Poisoning Attacks against Support Vector Machines](https://arxiv.org/abs/1206.6389)(ICML 2012) <br/> This paper investigates a family of poisoning attacks against Support Vector Machines (SVM).

* [Data Poisoning Attacks on Factorization-Based Collaborative Filtering](https://arxiv.org/pdf/1608.08182.pdf)(NeurIPS 2016) <br/> This paper demonstrates how a powerful attacker with full knowledge of the learner can generate malicious data so as to maximize his/her malicious objectives, while at the same time mimicking normal user behavior to avoid being detected. It presents efficient solutions for two popular factorization- based collaborative filtering algorithms: the alternative minimization formulation and the nuclear norm minimization method.

* [Using Machine Teaching to Identify Optimal Training-Set Attacks on Machine Learners](https://pages.cs.wisc.edu/~jerryzhu/pub/Mei2015Machine.pdf)(AAAI 2015) <br/> This paper utilizes the certain Karush-Kuhn-Tucker conditions to identify optimal training-set attacks on machine learners.

* [Universal Multi-Party Poisoning Attacks](http://proceedings.mlr.press/v97/mahloujifar19a/mahloujifar19a.pdf)(ICML 2019) <br/> In this work, the universal multi-party poison attacks is adapted.

* [Trojaning Attack on Neural Networks](https://weihang-wang.github.io/papers/tnn_ndss18.pdf)(NDSS 2018) <br/> In this paper, the trojan attack is proposed.

* [Neural Cleanse: Identifying and Mitigating Backdoor Attacks in Neural Networks](http://people.cs.uchicago.edu/~ravenben/publications/pdf/backdoor-sp19.pdf)(SP 2019) <br/> This paper proposes a novel and generalizable technique for detecting and reverse engineering hidden triggers embedded inside deep neural networks.

* [Data Poisoning Attack against Knowledge Graph Embedding](https://www.ijcai.org/proceedings/2019/0674.pdf)(IJCAI 2019) <br/> In this paper, a data poison attack against knowledge graph embeddding is proposed.

* [Manipulating Machine Learning: Poisoning Attacks and Countermeasures for Regression Learning](https://arxiv.org/pdf/1804.00308.pdf)(SP 2018) <br/> This paper proposes a theoretically-grounded optimization framework for the poison attack of regression task, and discuss its potential handle methods.

* [Certified Defenses for Data Poisoning Attacks](https://arxiv.org/pdf/1706.03691)(NeurIPS 2018) <br/> This paper address the certified robustness under the poison attack by constructing approximate upper bounds on the loss across a broad family of attacks, for defenders that first perform outlier removal followed by empirical risk minimization.

* [Robust Logistic Regression and Classification](https://proceedings.neurips.cc/paper/2014/file/6cdd60ea0045eb7a6ec44c54d29ed402-Paper.pdf)(NeurIPS 2014) <br/> It is a seminal work of logistic regression and logistic classification that can defend the constant fraction of adversarial outliers.

* [Robust High-Dimensional Linear Regression](https://arxiv.org/pdf/1608.02257.pdf)(arxiv 2016) <br/> This paper discusses the poison attack of linear regression.

<a id='Federate_Learning'></a>
##Federate Learning
* [CRFL: Certifiably Robust Federated Learning against Backdoor Attacks](https://arxiv.org/pdf/2106.08283.pdf)(ICML 2021) <br/> This paper proposes Certifiably Robust Federated Learning (CRFL), to train certifiably robust FL models against backdoors.

* [DBA: DISTRIBUTED BACKDOOR ATTACKS AGAINST FEDERATED LEARNING](https://openreview.net/pdf?id=rkgyS0VFvr)(ICLR 2020) <br/> This paper proposes the distributed backdoor attack (DBA) which decomposes a global trigger pattern into separate local patterns and embed them into the training set of different adversarial parties respectively.


<a id='Beyond_Safety'></a>
## Beyond Safety
* [Improved Autoregressive Modeling with Distribution Smoothing](https://openreview.net/forum?id=rJA5Pz7lHKb) (ICLR 2021) <br/> This paper apply similar idea of randomized smoothing into autoregressive generative modeling, which first modeling a smoothed data distribution and then denoise the sampled data.

* [Defending Against Image Corruptions Through Adversarial Augmentations](https://arxiv.org/pdf/2104.01086.pdf) <br/> This paper proposes AdversarialAugment method to adversarially craft corrupted augmented images during training.

* [On the effectiveness of adversarial training against common corruptions](https://arxiv.org/pdf/2103.02325.pdf) <br/> This paper studies how to use adversarial training (both Lp and a relaxation of perceptual adversarial training) to improve the performance on common image corruptions (CIFAR-10-C / ImageNet-100-C).


* [Unadversarial Examples: Designing Objects for Robust Vision](https://arxiv.org/pdf/2012.12235.pdf) (NeurIPS 2021) <br/> This paper turns the weakness of adversarial examples into strength, and proposes to use unadversarial examples to enhance model performance and robustness.

* [Self-supervised Learning with Adversarial Training](https://github.com/P2333/Papers-of-Robust-ML) ([1](https://proceedings.neurips.cc/paper/2020/hash/1f1baa5b8edac74eb4eaa329f14a0361-Abstract.html), [2](https://proceedings.neurips.cc/paper/2020/hash/c68c9c8258ea7d85472dd6fd0015f047-Abstract.html), [3](https://proceedings.neurips.cc/paper/2020/hash/ba7e36c43aff315c00ec2b8625e3b719-Abstract.html)) (NeurIPS 2020) <br/> These three papers work on embedding adversarial training mechanism into contrastive-based self-supervised learning. They show that AT mechanism can promote the learned representations.

* [Do Adversarially Robust ImageNet Models Transfer Better?](https://proceedings.neurips.cc/paper/2020/hash/24357dd085d2c4b1a88a7e0692e60294-Abstract.html) (NeurIPS 2020) <br/> This paper show that an adversarially robust model can work better for transfer learning, which encourage the learning process to focus on semantic features.

* [Adversarial Examples Improve Image Recognition](https://cs.jhu.edu/~alanlab/Pubs20/xie2020adversarial.pdf) (CVPR 2020) <br/> This paper treat adversarial training as a regularization strategy for traditional classification task, and achieve SOTA clean performance on ImageNet without extra data.

<a id='Seminal_work'></a>
## Seminal Work
* [Unsolved Problems in ML Safety](https://arxiv.org/pdf/2109.13916.pdf) <br/> A comprehensive roadmap for future researches in Trustworthy ML. 

* [Towards Deep Learning Models Resistant to Adversarial Attacks](https://arxiv.org/pdf/1706.06083.pdf) (ICLR 2018) <br/> This paper proposed projected gradient descent (PGD) attack, and provide a theoretical and empirical proof that adversarial training based on min-max optimization with PGD attack can boost robustness.

* [Adversarial examples are not easily detected: Bypassing ten detection methods](https://dl.acm.org/citation.cfm?Id=3140444) (AISec 17) <br/> This paper first desgined different adaptive attacks for detection-based methods.

* [Explaining and Harnessing Adversarial Examples](https://arxiv.org/abs/1412.6572) (ICLR 2015) <br/> This paper proposed fast gradient sign method (FGSM), and the framework of adversarial training.

* [Intriguing properties of neural networks](https://arxiv.org/abs/1312.6199) (ICLR 2014) <br/> This paper first introduced the concept of adversarial examples in deep learning, and provided a L-BFGS based attack method.

<a id='Benchmark_Datasets'></a>
## Benchmark Datasets
* [RobustBench: a standardized adversarial robustness benchmark](https://arxiv.org/pdf/2010.09670.pdf) <br/> A standardized robustness benchmark with 50+ models together with the [Model Zoo](https://github.com/RobustBench/robustbench). 

* [Natural adversarial examples](https://arxiv.org/pdf/1907.07174.pdf) <br/> ImageNet-A dataset.

* [Benchmarking Neural Network Robustness to Common Corruptions and Perturbations](https://arxiv.org/pdf/1903.12261.pdf) (ICLR 2019) <br/> ImageNet-C dataset.

* [Imagenet-trained cnns are biased towards texture; increasing shape bias improves accuracy and robustness](https://arxiv.org/pdf/1811.12231.pdf) (ICLR 2018) <br/> This paper empirically demonstrate that shape-based features lead to more robust models. They also provide the Styled-ImageNet dataset.
