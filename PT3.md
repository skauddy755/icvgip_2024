> Topic: \
> Towards a real conversation between vision in brains and machines
> 
> Speaker: \
> SP Arun, Centre for Neuroscience, Indian Institute of Science, Bangalore

I think most of his talk is based on this paper: [Brain-like emergent properties in deep networks: Impact of network architecture, datasets and training](https://arxiv.org/pdf/2411.16326)

# Central Philosophy, Efforts and Findings

- Despite the rapid pace at which deep networks are improving on standardized vision benchmarks, they are still outperformed
by humans on real-world vision tasks. This paradoxical lack of generalization could be addressed by making deep networks more brain-like. Although several benchmarks have compared the ability of deep networks to predict brain responses to natural images, they do not capture subtle but important brainlike emergent properties. 
- To resolve this issue, we report several well-known perceptual and neural emergent properties that can be tested on deep networks. 
- Our main findings are as follows.
    1. network architecture (among Architecture, Datasets, Training Scheme) had the strongest impact on brain-like properties compared to dataset and training regime variations.
    2. networks varied widely in their alignment to the brain with no single network outperforming all others.
- Taken together, our results complement existing benchmarks by revealing brain-like properties that are either emergent or lacking in state-of-the-art deep networks.


### Markovec's Paradox

- Tasks that are difficult for humans, such as mathematical calculations, data analysis, and playing chess, are relatively easy for machines to perform.
- Tasks that are easy for humans, such as motor or social skills, are difficult for machines to replicate. For example, it's difficult for machines to recognize faces or move through an environment.


### How to understand the Brain Functions

Its not sufficient to just test input stimuli and behavioural outputs and make hypothesis based on that. We need to see deeper and use measurable parameters like MRI etc. So, we also experiment on monkeys since they are our closest relatives.

### The Hard Problem of AI

- What is 'A' ?
- What is 'I' (consciousness)?

### How does the Brain solves Vision Problems?

- Neuroscience studies reveal that there are a huge number of regions in the brain dedicated specially to solve vision.

### How do we quantify brain responses?

Take for example: Identifying how hard it is to find the odd one out in a picture (say a camouflaged tiger in bush)
- For AI, we might measure the similarity scores between the embeddings of various image components.
- For Human, we might measure the time taken to repond. This time will be proportional to how hard it is for the brain to identify the odd one out.

And then we can make a plot distances of various objects with respect to each other in both of AI space versus Human space.
This will give us insights about the how AI and Brain encode the visual informations and whether some brain-like properties/biases are present in AI models or not. (SPOILER: Some are and some aren't)

### Are some process-modelings of brains obeyed my AI as well?

Take for example: Reading distorted characters (say Captcha)
- Conside two tasks (1) reading single letter (2) reading a string of letters. Let:
    - L = time taken to recognize a given letter/character without distortion
    - D = magnitude of distortion
    - TL = time taken to recognise the letter/character with distortion
    - TS = time taken to recognize the string made up of some characters

- For Task-1 we can have two models:
    - Multiplicative Model: TL = (S + D)
    - Additive Model: TL = (S * D)
- For Task-2 we can again have two models:
    - Multiplicative Model: TS = PIE(TL for each character)
    - Additive Model: TS = SIGMA(TL for each character)

It is found that:
1. Brain obeys Multiplicative Model for Task-1 but Additive Model for Task-2. These verifications are based on reponse time (common measure of brain processes in neruroscience and cognitive psychology)
2. Seems like these rules are also found in some DNNs (even though the engineers were unaware of it, yet the architecture, training strategy, dataset and learning objectives might have forced the network to learn these modelings implicitely) 
3. There is correlation between "Presence of these rules" in the network and its "Performance"

# Brain-like properties in DNNs

For each DNN models, training scheme and dataset the authors tested a total of 15 brain-like properties, as summarized below and detailed in Supplementary Section of the paper:

1. Object Normalization-pairs: The neural response to two objects is the average of the response to the individual objects.
2. Object Normalization-triplets: The neural response to three objects is the average of the response to the individual objects.
3. Scene Incongruence: Object categorization is more accurate when objects are presented in congruent compared to incongruent scenes.
4. Mirror Confusion: Images reflected about the vertical axis are more similar than when reflected about the horizontal axis.
5. Correlated Sparseness-morphlines: Selective neurons are selective for both distinct objects as well as along arbitrary morphlines.
6. Correlated Sparseness-shape/texture: Selective neurons are selective for shape and texture.
7. Weber’s Law: Perceptual distances are proportional to relative rather than absolute changes in magnitude.
8. Basic Occlusions: Likely completions of an occluded display are more similar than mosaic completions.
9. Depth Occlusions: Depth ordering changes are more similar than equivalent feature changes.
10. Relative Size: A minority of neurons are sensitive to relative size of features.
11. Surface Invariance: A minority of neurons decouple pattern changes from surface changes.
12. 3D Processing-1: Changes in 3D shape are more noticeable than equivalent 2D changes.
13. 3D Processing-2: Changes in 3D shape are more noticeable than equivalent 2D changes even after controlling for feature clutter.
14. Global Advantage: Perceptual distances are more sensitive to global compared to local shape.
15. Thatcher Effect: Perceptual distances are more sensitive for upright compared to inverted faces.

> Among these, (4), (7), (10), (14) and (15) were discussed in the talk

## 1. Effect of Network Architure

![alt text](archive/image_16.png)

### Brain-like properties present in all architectures



### Brain-like properties unique to specific architectures



### Brain-like properties absent in all architectures



### Embedding of effect strength across all properties


## 2. Effect of Training Dataset

![alt text](archive/image_17.png)

### Brain-like properties present in all architectures



### Brain-like properties unique to specific architectures



### Brain-like properties absent in all architectures



### Embedding of effect strength across all properties


## 3. Effect of Training Regime

![alt text](archive/image_18.png)

### Brain-like properties present in all architectures



### Brain-like properties unique to specific architectures



### Brain-like properties absent in all architectures



### Embedding of effect strength across all properties


