# SPEAKER TYPE I
## 3-way Bookshelf Speaker

I started all of this to give myself a project to make, and it turned out to be a super fun project! Below, I outline my design process and building process of a pair of 3-way speakers.

Contents:
1. Driver Selection
2. Single Amp vs. Tri-Amp
3. Box Design
4. Building the Thing
5. Final Product

![Final](/0readmepics/1.jpg)

### Step 1: Driver Selection

Choosing drivers that work well together is an art, in my opinion. The first thing that I decided were my crossover frequencies: 300 Hz and 3kHz. I chose these so that my midrange driver would cover most of the important audible frequencies (2k-4kHz) and would be supported by the tweeter. Then, the woofer would come in around the low frequencies from around 150-300Hz. The remaining low frequency components would be covered by the subwoofer that I would eventually add to the system.

Once my crossover frequencies were chosen, it wasn't too hard to find some not-too-expensive quality drivers. I ended up choosing these:


This one is a 1" dome tweeter with a damped silk diaphragm (soft). I chose a soft diaphragm dome tweeter over a metal dome tweeter to try to make the higher frequencies sound smoother. Some people think that 1" tweeters are too big, but since I'm bringing the tweeter all the way down to 3kHz, I think it'll do just great.

The frequency response graph is important: it is a measure of how well the driver will perform at various frequencies. For our purposes, we are going to look at the frequency band from 2kHz-20kHz (typical maximum audible frequency). If we look at the red curve, we see that it is relatively flat over the 2-20kHz range. That is what we are looking for: a flat frequency response. This means that the driver isn't supposed to do anything erratic over its operating frequency range and will have the same gain for all operating frequencies. 

Also, the blue curve shows impedance as a function of frequency. The driver's nominal impedance is 4ohms, but we can see a peak at about 800Hz. This peak is to be avoided to avoid a current spike in the previous circuitry (amps, XOs, pre-amps, etc).

I got a pair of these tweeters for around 10$CAD each at Solen Electronique (https://solen.ca/products/speakers/home-speakers/tweeters/dx20bf0004/).

The datasheet for it can be found here: https://solen.ca/wp-content/uploads/dx20bf0004.pdf
Mid-Range Woofer: Tangband W3-593SF

This is a 3" mid-range woofer that is designed for an under-surface mount application. If you don't want to have to build a cover to surface mount these, you should get something that looks nicer. I got these for free from a friend so the entire design is pretty much based on these.

The frequency response of these mids is pretty decent: flat from around 200Hz to 5kHz. However, the impedance is the limiting factor is the XO frequencies: anything below 300Hz or above 2kHz is going to raise impedance a lot. 

This driver's nominal impedance is 8ohms, so an impedance matching network would have to be used on either the mid or the tweeter. I will talk about this later.
Woofer: Dayton Audio DC1608

This driver is a 6.5" 8ohm sealed paper cone woofer. I was looking for something to cover the lower frequencies at a low price, with a good frequency response.

From the frequency response of the woofer, we can it starts to wobble and degrade starting at around 1kHz, and starts being not as strong below 100Hz. That being said, the impedance is also constrained to those same numbers since impedance increases when frequencies beyond 100Hz-1kHz around put through the woofer.

This will be perfect for what I intend to use it for.

### Step 2: Single Amp vs. Tri-Amp
Here comes an important decision: do you want one amplifier for all three drivers or three different amplifiers for each driver?

Single Amp:

This is what most people (and companies) do for home audio. This type of amplification takes the line-level signal in its entirety and amplifies it to the speaker-level signal. Then, the signal goes through the crossover, and finally to the drivers. This uses a passive crossover made of inductors and capacitors inside the speaker box. 

This method is definitely the cheapest to make, but it does have its limitations and drawbacks. 

Advantages:
- only 1 amp
- only 1 pair of wires to each speaker
- ower cost

Disadvantages:
- possibility for more noise (from crossover)
- power loss


Tri-Amp:
This is what the high-end audio community do. This type of amplification puts the line-level signal through an active crossover (aiming to keep the gain to 0dB). This splits the signal into the 3 different frequency ranges for each driver. These 3 signals then go to their respective amplifiers and finally to the drivers.


Advantages:
- better sound quality
- less noise

Disadvantages:
- way more expensive
- 3 pairs of wires for each speaker
- 3 amps

(What I just covered was mostly my opinion on the topic, but more information can be found on google and of course, Wikipedia: https://en.wikipedia.org/wiki/Bi-amping_and_tri-amping.)

As someone who just loves projects and dumping money into them, I chose to tri-amp my speakers. What this entails:
- possibility for a smaller speaker box (since the XO isn't inside it)
- design of a 3-way stereo crossover (extremely hard to find online)
- either 3 amps or a single 3ch stereo amp
- more wires
- more moneys

On to the design of the speaker box.

### Step 3: Box Design
This step turned out to be a lot harder than I thought it would be. I mostly followed the tutorial on DIY audio and video (https://www.diyaudioandvideo.com/Guide/BuildSpeaker/). This tutorial outlines every step of the process, even giving volume calculators and ported vs sealed calculators. 

Given the specs on the woofer, the ported vs sealed calculator did give a 91 Efficiency Bandwidth Product(EBP). Now, while this specific website gives 90 EBP as a cutoff for either or ported, I decided to go for a sealed enclosure for the woofer. This let me build a smaller enclosure and not have to worry about building a port into my box.

The mid gave an EBP of around 130, but I decided to ignore it and make that enclosure sealed as well. 

Sealed enclosures are always smaller than ported enclosures. 

The tweeter is sealed in its own enclosure and doesn't need an additional enclosure.


To make my design process simpler and to limit power loss, I put the mid and the woofer in their own sealed enclosures. 

I decided to add a support in the middle of the woofer enclosure. Below are the drawings of the box: 

### Step 4: Building the Thing
This part wasn't all that hard with access to a woodworking shop. The process kind of goes like this: cutting all the pieces, assembly, testing, final touches, and sanding, then primer and paint. Typically, DIY speakers are made of MDF due to its good density, weight, and strength. I decided to use Russian birch plywood in 1/2" panels. This type of wood is still very strong since it is a type of plywood, but is a lot easier to work with compared to MDF. 

1. Cutting the pieces: I chose to make the front panel the one that covered all the others, to make the front look as smooth as possible. The front has three holes, one for each driver. The mid and the woofer are close together to eliminate any delay the signal might have. (Also, the two front panels are mirrored, to not have 2 right speakers). This led me to make the top and bottom panels, then the sides, then the inside separator and support, and finally the back panel. Kind of last minute, I decided to make the back panel removable in case I wanted to tweak something on the inside later on.

2. Assembly: Once all the pieces for both speakers were made, the assembly was next. Each piece was glued on with wood glue and nailed in with a nailgun. The nail holes were then covered up with wood putty to make the surfaces as smooth as possible.  

3. Testing: After assembly, I decided to test the enclosure, with the drivers installed to see how it sounded. I didn't have the equipment I needed to test it out, so I brought it to the lab, where I hooked it up to 3 lab filters, then 3 amps, and a computer. The connection went: computer >> lowpass filter, bandpass filter, highpass filter >> each of these outputs was connected to their respective amps, then finally to the drivers. It sounded decent with a song as complex as "bury a friend" by Billie Eilish.                                                                                                                       

4. Making the product ready to paint: After testing, all the corners and edges were rounded off with a 1/4" fillet on a router. This not only makes the speaker box look good, but it reduces echo from the baffle(front panel) edges. Each surface was then sanded with 100 grit then 180 grit sandpaper. I also received the banana plug terminal boxes after testing them, so the back panel needed to be modified to fit these terminal boxes. (Also, since I am tri-amping these speakers, each driver will have a pair of terminals going to it).

5. Painting: (All paint was applied by spray) Once all ready to paint, I put on 2 or 3 layers of white primer directly on the wood, letting each layer dry before applying the next. After the primer, I sanded the whole box by hand using 600 grit sandpaper. Then came the time to paint them, I decided on a neutral gray. 2 layers of paint did the job, making an even color everywhere on the box. Once the paint was dry, I applied a high gloss finish on the enclosures.

### Final Product
 
Once both enclosures were painted and finished, the drivers with soldered wires were mounted into their respective holes. Some black carpet was shoved into the back of the enclosures to dampen the sound. Next, the wires were soldered onto the screw terminals and the screw terminals were pressed into the back cover. Felt pads were stuck to the underside of the speakers so that the paint wouldn't get scratched and the decrease vibrations on the surface where the speakers are mounted.

Below is a picture of the finished left speaker.
