
#day2 #pt #pt2 

> Topic:
> On Visual Quality: Pictures, Videos, and GenAI
> 
> Speaker:
> Alan C. Bovik
> Professor, University of Texas at Austin

# Intro Problem - go and take img with your device

How many distortions can you find?
1. focus blur
2. under/over exposure
3. Jitter
4. Low light noise
5. ...
6. combination of all these

i.e., it is very difficult to report the quality of a picture..

# Measuring Picture quality is important

### Video quality issues are pervasive:

- today 80% if US internet traffic is Pictures and videos
- Degraded by infinite diversities of distortions and severity
- often in complex combinations = new distortions
- impacts viewing enjoyment and bandwidth use

### Classic Communication Channel

signal in -> tx -> channel -> rec > signal out

### Today's visual communication systems

- Today's transmitter are photons bouncing from everywhere (natural visual transmitter)
- Today's receiver is someone's eyes (natural visual receiver)
- Channel (capture device, display device, streaming services ...) is all sort of things in the internet.

Over the years the brain has adapted to the highly regular statistics of the visual world.
Thereforre the natural transmitter and natural receiver are duals of each other


### Sources of streaming distortions

Everywhere (distortions during bouncing, even noise at neural level)

### Useful for Correcting DIstortions

VQP = Visual quality predictor
used to measure output of every de-distortions model function (which are just approximations)

deblur, denoise, deblock, ...
But it has been FRUITLESS

LET'S SEE DISTORTION AT THE LEVEL OF NEURON (BIOLOGICAL OR EVEN ON GPU)


### Controlling Compression

Modern VQP models reduce visual data traffic by ~25%
Examples:
SSIM, VIF, VMAF, BRISQUE, NIQE

# Ruderman's Walk in the Woods

> take an image f
> Over each window, g = (f - mean) / (std + 1)
> mean = local mean luminance
> std = local luminance contrast

OBSERVATION: The histogram plotted was a gaussian...

In a way (f - mean) was a bandpass function


## The gaussian law of pictures and videos

let m = spatial coordinate

Pass the img f through a bandpass filter
g(m) = f(m) * h(m)