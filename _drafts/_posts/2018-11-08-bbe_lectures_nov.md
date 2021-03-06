---
title: 'Caltech BBE Lectures Nov'
date: 2018-11-08
permalink: /posts/2018/11/bbe_lectures_nov/
tags:
  - notes
---

After starting to make notes on math lectures, I feel it unfair if I didn't give the same respect to my own field. So here it is, lecture notes in computational biology and neuroscience. 

# Lecture Notes

## Population Coding of Hand Movements in the Primate Brain

### Hans Scherberger, OPT German Primate Center	11/08/2018

#### Introduction 

Sensorimotor transformation for grasping   
Coding; decoding; neural  networks  
The fronto-pariental grasping circult: AIP; F5; M1 

#### Methods

Baseline; power grip; precision grip; delayed grasping task  
Different neural action potential with different task type and oriantaion & position of handle  
Cue; memory; movement  
Activities are also mudulated by reward (small, large)  
Hand movement: different objects  
Hand traker 27 degree of freedom; reconstruct the whole trajectories  
Classify different grip types  
AIP: visual feature of objects, shape is more important than size; F5: grasp properties

Decoding; Use Bayesian decoder to infer the object based on neural activities   
Use Kalman filter to predict hand kinetics 

Neural networks; visual freature to muscle dynamics   
Similar behaviours are identified from the neural activities and artificial NN

Hypothesis of neuron coding  
Optimal one-dimensional projections based on different functions  
Neural properties are isotorpic on after the projection   

#### Summary 

AIP: object information; F5: grip type information; M1: movement execution: mixed coding  
Decode from activity: grip type and hand kinematics  
RNN reconstruct the circuit  
Population processing: mixed selectivity; dynamic population code  

Many information can be obtained by recording neural activity while performing tasks. Then these signal can be classified and processed with different conditions. However, actually only a small portion of neurons were recorded from the experiment limitation (possiblely less than 1%). Then the large amount of information retrieved from the small population seems amazing. This property is still under debate. 

## On the Rational Boundedness of Cognitive Control

### Jonathan Cohen, Princeton	11/08/2018

#### Introduction 

Control, repress some movement: Example. scratches; only in human   
Parallel tasks  
Control theory; cybernetics; TOKE model  
Congnitive psychological tradition; qualititive description; limited capacity  
Rescent formalism: expected value; rational meta reasoning; cost-benefit analysis  
Why the capacity is limited? Energy? Structure?   
Multitask: crosstalk; interference  
How do make parallelize and scale with network size   

#### Models

Control over different channels; optimal strategy when nodes have overlap  
Graph with shared representation radically restricts independent parallelism (almost exponential decay)   
Why shared representation: learn faster; generalization  
Color name task: shared representations  
Network representation of multiple tasks  
Single task vs. Multi task leanring: the learning try to capture more dominate representation  
Interactive vs. independent parallelism 

#### Summary

The speaker propose that the difficulty of doing parallel tasks mainly come from the shared representation, which can cause interference. The shared representation come from the basic learning process. The network choose shared representation to capture the dominant features and improve the abality to generalize. However, this causes the network cannot make paraelleize the tasks sharing the representation. When trained to do multiple tasks together, tensor product representation is acquired rather than the shared one as before. 

Comments: what is the trade-off relation between the preformance over multiple tasks and the number of representation allowed?

## Emergent Elasticity in the Neuro Code for Space

### Surya Ganguli, Stanford	11/12/2018

#### Introduction

How to know the position and establish a map  
Different cell types: border, speed, grid, head direction  
Extrection of spatial position from periphery: landmark and velocity 

#### Results

Consistency of landmark activation with regard to paths

Does error accumulate  
Conditioned on last border touch, the error grows, while conditioned on other point doesn't  
Firing field expansion; firing field drift    
Experiment of homogeneousity showed firing field drift 

1D attactor model: circular neuron chain, local excitation, long-range inhibition; localized activation wave packets  
East/west velocity cells  
Landmark cell: pinning phase; learn average by Hebbian learning   
2D landmark cells  

Topological defects of landscape   
VR test of differrent gain rate of distance   
Attractor-landmark model: the phase advance and the pinning effect of landmark should agree   
Weak change: phase shift; strong change: remapping and rescaling 

#### Summary

The identification of self-position requires both the information of motion and landmark. Self-motion acts like a path-integration, while landmarks help to celebrate. This mechanism is confirmed by the perturbation experiment. Mild discrepancy makes a phase shift, and large difference with cause a remapping. This effect may not be restricted to the model proposed by the author. Also, the physical entity of such a circular wave has not been identified. 

## Architechture, Design, and Tradeoffs in Biomolecular Feedback Systems

### Noah Olsman, thesis defense, John Doyle group	11/16/2018

#### Introduction

Consider biological system as functional systems; architechtural thinking; funtional modules; abstract away details under given constraints  

#### Systems biology

sensory systems: sensitive responses; broad range; photon detection and adaptation   
Tradeoff between sensitive and broad; logarithmic sensing; contrast  
Chemotaxis; osillating stimuli with different magnitude, same response; cell-cell signaling; vision   
Logarithmic sensing by IFF & NIF (nonlinear integral feedforward)  
Or with log sensor: allosteric regulation  
MWC model; log sensing in the sensitive region   
Free energy tuning response range  
Example: hemoglobin 

#### Synthetic Biology 

Robust performance; robust perfect adaption   
Sequestration feedback system [Cell Systems, 2016]  
Stable states; control dynamics stabilities  
Stable if production is slower than degradation  
Performance metric: overshoot, noise, response time, error  
Sensitivity function: error / reference with different frequency; Bodes's integral theorem, trade-off under different frequency  
Fragility and speed  
Estimation of the largest sensitivity; controller degradation reduces fragility but introduces error  
Waterbed effect; reduce error, inefficiency  
Design of syntheic bacterial growth control circuit; quorom sensing  
population control; long-term osillation, first saturation  
Fast sequestration can be ignored  

#### Summary 

The control theory can help our understanding of biological circuits, and design new circurits with desired functions. The rich phenomena in biology can also motivate theorical discoveries. 

## The Bayesian Brain: From Predictive Coding to Decision Making

### Rajesh Rao, UW Seattle	11/19/2018

### Introcution

Computational neuroscience; neurally-inspired AI; brain-computer interface  
Cortical puzzle: diverse function, common organizatio principles; remarkable flexibility  
Massive feedback and hierarchical structure; Abstruction of representation  
Visual receptive field; Endstopping  
Predictive coding; center activation and surrounding repression; response is the difference between the center and surrounding    
Orientation contrast: why; Natural images statistics  
Predictive coding theory of cortical function: prediction, error, update iternal representation  
Implements Bayesian inference 

#### Bayesian inference

Probabilistic models of the brain   
Learn a generative model to estimate the proability distribution  
VR mouse fun landmarks; audio recognition;  
Does predictive coding have a future; Predictive processing: a conical cortical computation  
Inference of probabilistic beliefs: both the nean and variance   
Predictive coding to actions, rewards, and decision making; indirected observation of the world  

#### POMDPs

Partially observable Markov decision processes (POMDPs): world action agent reward / observation  
Agent: belief, policy, value function. Maximize the expected future reward; learn from the beliefs  
Input: belief state; output: value of belief state; Train by temporal difference error (TD)   
Random dots motion task; cortical response neuron recording; belief; collapsing decision boundary  
Effect of changing prior probability; reward prediction error: hard trial have higher reward prediction error, but lower on error trials  
Confidence of decision making; social decisions in group decision making task   

#### Summary

Bayesian approach offers nomative models for perception, action, reward optimization, and decision making  
Neocortex modeled as a Bayesian estimator that maintains a probabilistic internal model of the world  
The basal ganglia hypothesized to learn values and policies for cortical beliefs  
Bayesian models provide functional explanations  

Bayesian inference is a fundamental rule for constructing the understanding the external world. Various experiments have shown that the brain actively explores the Bayesian rule, and both the mean and uncertainty play roles in the decision process. However, it is still uncler whether brain implement the Bayesian inference explicitly or is using other similar approaches. 

## Bidirectional Brain-Computer Interfaces for Restoration and Augmentation of Brain Function

### Rajesh Rao, UW Seattle	11/20/2018

Sorry I missed the introduction part...

#### ECoG Signals

ECoG phenomena; Imagined movements have similar activation as actual ones  
Use imagery to control a cursor; how brain change during learning to control the cursor  
BCI learning is similar to motor skill learning    
ECoG stimulation for sensory feedback; closed-loop control 

#### Non-invasive BCIs

EEG: noisy, correlation with brain activity  
Beta wave, visually evoked potential (P300)  
Control robots; motor imagery to navigate virutal world   
Brain-to-brain interface  
BrainNet: bollabrative problem solving by networks of brains  

#### Summary

Applications: medical; non-medical   
Ethical issues: healthy and safety; legal issues; security and pravicy; social impact   

Brain-machine interface provided a fancinating possibliity of understanding neuron fanctons and design engineering systems. 

