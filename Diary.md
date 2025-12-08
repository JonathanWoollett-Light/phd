# Diary

### 08/12/2025

- progression meeting can be technical but will mostly relate to research direction, acquiantance with subject area and ethical considerarions (includes data safety and privacy considerations) will also be looking for risks (what is doing experiment takes ages? what if experimenrs are too expensive or take ages? what if experiments doesnt give conclusive result? maybe have milestones or secondary research questions)
- bring more visualizations, try more
- look at gradient issue aswell, look at the difference, maybe plot against to see if its linear quadratic or exponential (this is example of a risk, should have good reasoning why im doing it. tooling risk)
- strategy for benchmarks and experiment design, more I can scope this down and limit thw scope the better. Can results be benchmarked against other work? Dont just hope the more conservative experiment dimensions will provide good results but build a meaningful case to yourself and others that the conservative small case is good enough. show sketches of what i imagine experiment might be like, like i could draw the results i expect to discuss before implementing an experiment

### thoughts

- progression meeting stuff
  ```txt
  For progression into year 2 of a full-time PhD/EngD or MPhil programme (or equivalent stage of a part-time PhD or MPhil programme), a PGR must demonstrate that they: 
  have completed any required training (as set in their PGR handbook);
  are in good standing in terms of responsible research (this includes having completed the Research Integrity Tutorial, obtaining any required ethical approval, and having a data management plan (if relevant));
  have planned in a realistic fashion the second year (or equivalent) of their research, indicating any risks and how these will be mitigated;
  have begun to articulate the direction their research is taking and the research questions it addresses;
  have sufficient acquaintance with the relevant field of knowledge to place their research into context;
  have sufficient proficiency in the relevant research methods, techniques and theoretical approaches to move their research to the next stage;
  have started to develop the ability to write in an appropriate academic format, commensurate with the discipline.
  ```

### 27/11/2025

- make sure when plotting to avoid hidden steps like image interpolation which can distort data.
- it is interesting to see both complex plots (spikes over time for all samples) and simpler plots (spikes over time for 1 sample, or spikes over time for 1 class).

### thoughts

- focus on bringing plot next thursday
- error legit might just be that i run snnTorch for all timesteps but only run spiky for one
- all the charts except 0 and 8 are bad, why would this even be? maybe also post the code i use to do that analysis to see if anyone can spot my error.
  https://drive.google.com/drive/folders/1jN7cuut96oDSlxz88D5sSUOOLKAKyNfA?usp=sharing
- need to submit formal supervision meeting thing
- need to pull together docs for progression meeting
- need to re-write lit review to fit martins suggestions

### 13/11/2025

- be aware of york uni phd conference wheres other present their work 1st 3 min talk, 2nd poster, 3rd presentation
- some headings should be reduced in significance or merged (e.g. metric headings)
- referencing is bit chaotic, references should be right next to statements, try to make sure in later half references are also thorough
- for places where i talk about research gaps or areas of interest if i dont or cant reference it should be framed as such "there is potential" rather than making a statement, for opionated sections these can be highlighted with statements like "it appears that..."
- in categorizing errors categories can be more humble if i say "in the context of this work I will group errors like this"
- neural network section of background is quite good
- if i have a few seminal papers in mind that are interesting or counter to the overall narrative, i could highlight them, if i can extract some commonality and commentary that would be good, could use some of these to highlight inflection points or evolution of the field
- putting tables landscape might help making them more readable
- can have more explicit summary and conclusion at the end of the various sections (anns, hardware, etc.)
- for progression meeting training, can put tutorials i followed and discissions and discord etc.
- for formal review progress report should have question, gap and planned experiment
- that my writing has become less terse and more narrative is good, but it still being concise is good, current tone is fine

### thoughts

- got email about progression meeting
- DVS Cifar is a dataset worth looking at
- look up papers if having a synapse delay is really fundementally different to having weight
- look into triton
- look into spiking jelly
- is it worth being a volunteer writer for open neuromorphic, I should probably introduce this discord to other people in bist
- my nn gradient issues, debugging tracing pytorch computational graph
- seems like SNNs can be trained very deeply (despite surrogate gradient error among other things) if trained correctly (read "Rethinking residual connection in training large-scale spiking neural networks")
- am I working hard enough? What are some examples or benchmarks I could use to reality test this.
- look into openzl
- are there any woring qauntam ml models? what similarities might these have to analogue compute in snn
- extropic AI looks interesting, maybe could run SNN on it https://www.youtube.com/watch?v=Y28JQzS6TlE
- why is delayed reset good? read papers on this "AR-LIF: ADAPTIVE RESET LEAKY INTEGRATE-AND-FIRE NEURON FOR SPIKING NEURAL NETWORKS" and commit a PR to snnTorch to add more documentation
- have different optimizers been tested with SNNs do they have the same effectiveness as with anns (e.g. is adam still generally one of the best).

### 23/10/2025

- would be worth checking snntorch spiky issue with single neuron
- for a summer internship, a project could be to figure out how to scale maybe some work I have (e.g. network simulation they can then scale it to run on aws).
- martin wants to have people present a couple slides of their work in future group meetings (maybe i can go through my diary bullet points and describe them).

### Thoughts

- literature review should be spring board for research not just surgery (and discussion sections should create this spring)
- in discussion should I re-reference specific studies to critique them or to backup my discussion? I feel like I dont want to do this, should them being referenced previously in a descriptive way be enough? I mean im not discussing specific papers but rather the field (and it seems just doing "e.g. these few papers agrees with me or shows this" is not a strong argument)
- more explicitly design experiment that is more concrete to make assumptions clear, there is both external noise that is perceived by sensors and noise that might change the network values themselves, this helps counter balance the more exploratory thoughts and conversations 
- striking a balance between something more tangible and something more ethereal or crazy
- foundation model or world model needs lots of data but then special models need small amount of data
- when we dream are we really learning more deeply or simply teaching different parts of us
- linear regressions is very powerful, look up hypervectors
- models introspection and world models is interesting, like
- gus iben did robot evolution work, evaluating the learning process as it occurs to avoid catastrophic events is interesting
- how can I set up my qualitative ideas in a qauntative way
- Cellular Automata graph for reservoir computing thesis might be interesting read martin will forward me
- need to look into review supervision meeting and what's up with that, can email uni (pet pgr admin is best contact) form for meeting will be on york wiki school of pet postgraduate,  staff and pgr, postgraduate researchers, review of supervision form
- look into if tap meeting are at weird times 2nd tap should be 6 months after 1st, maybe they think I started earlier
- Mention the dimensions of the experiments but also evaluate them, this evaluation is somewhat missing from the literature currently or atleast it should be improved/expanded
- It will be very important to differentiate my work from other papers which apply SNNs jn a similar context (e.g. SpikeGym). Keep strong focus on degredation angle and the performance analysis of the internal dynamics of SNNs models in their learning process.
- The evaluation of the model as it learns is important, a robot learning online or in-situ cannot tolerate catastrophic failures and thus learning must be constrained or guided within safe bounds.

# 16/09/2025

- Need polish
- Need restructuring
- Highlight gap related to research question
- reshape this to martin
- analysis of spike and spike interval and neuroacience style metrics and analysis could also be interesting
- graphs can be useful for getting a feel for a system if even not quantifying
- on discussion section vs throughout, it would be good to have a discussion section for each subsection (e.g. discussion hardware section etc.)
- maybe flatten document 1 layer (so paragraph bold heading aren't normal for having another layer)
- instead of analytical dimensions vs experimental context headers this difference could be highlighted jn the introduction with a brief statement or discussion
- typical thesis has 9 to 10 chapters
- can use a little qualifying statement to help describe structure and tables can be useful (but not needed for every header/section)
- things should be included in the literature review if they are necessary to understand/appreciate the experiments
- start with simple datasets/benchmarks before growing the dimensions
- can mentioned things why I choose given simulator (e.g. isaac)
- setup review supervision meeting with babar

### Thoughts

- look into "large behaviour models"

### TAP

- Don't say dont need laptop, but rather that can use it differently 
- maybe add sections to literature describing simulators (isaac sim, mujocu, etc.)
- can discuss sim2real transfer and this stuff, although Babar isn't excellent
- are simulators good enough to justify conclusions? need specific simulators and evaluating these simulators, these give estimations.
- should start on isaac soon, it has steep learning curve (other simulators are pybullet (very simplified)) gazeboo is other low-level sim, although more difficult and fundemental althouughtraditionally very strong. Isaac is mainstream, and mlittle easiers than gazeboo. MuJuCo is another but probably doesn't work for this case as not low level enough.
- might be difficult to do comparison with sims since it will take long time to learn them.
- vrap probably not good, is weird, he notes again he prefers gazeboo or isaac sim.
- there are simulators which have noise and degredation, isaac and gazeboo and vrap support noise features
- martin: dont need novel real worldness, novelty can be model
- important to consider papers in field outside pure SNNs
- martin: usually gaps very specific, good strategy is publishing research in conference along the way, reviews can then help thesis development
- novelty doesn't come from application or specific robotics model but instead the underlying system
- **make slides on core concepts e.g. "what is an SNN?" and introduce the field a little and the aspects and points to where novelty should be "here are 3 aspects, novelty will be in this aspect"** big difference between modifying simulatyors and modifiying the model
- try to make a bit of a story with what exists and what is current and what I want to do, "what", "why", "how" this should be explained in slides (should be general audience (academics but those relatively near in field)) this is important for an external examiners and community feedback. If argument is made about perceived gap, people will give benefit of the doubt.
- Even if overlap with existing paper, should have good story to justify novelty and have appropriate due-diligence
- when writing thesis and telling the story of novelty, timeline and causality can often be re-arranged, sometimes manipulate that things I did later, I tell as happening earlier, so thesis isn't a telling of the real world, rather a logical mapping of researching findings and questions into a narrative (literature has same affect)
- **need to do review supervision form, with babar if issue with supervision, more if I don't want martin to know**
- martin: can email him on holiday if specific question/concern
- with internship if I do this, can end up adding time at end of phd to compensate while taking break out
- should build slides to ease TAP advisor into project, like conference but bit more generic and en-compensating,
- should look at reality gaps for different simulators and talk about this, they will have done sensor failures and faults/drift/noise. adding to state of art can't be "here is another sensor that's novel" more like apply method in specific novel cases, the nature is different

### Thoughts

- i should have CPU implementations of all the algorithms I want to implement to make sure I understand them
- look into "Multilayer Feedforward Small-World Networks"
- look into "Graph Reservoir Architecture"
- look into metrics to compare models:
  - Effective FLOPs (EFLOPS): Accounts for hardware which can operate more sparsely and avoid multiplying zeros in matrix multiplication.
  - Synaptic Operations Per Second (SOPS): Measures specific neurmorphic operations but maybe not so useful for comparing SNNs to ANNs.
- It would be useful to reproduce the results of **Memristive Field-Programmable Analog Arrays for Analog Computing** to better understand memFPAAs.
- are there any datasets like st-mnist but instead of giving a trace of spikes drawing a digit give a trace of non-binary floating point values (like voltages from a touchpad)
- if I read about a result in a review (or newer paper) which references the original paper which produced the result how do I credit both the review and the original paper the review references when referencing this result? It seems unfair to not credit the review and the review author/s from which I discovered the result.
- it would be good to collect a list of online platforms that allow renting accelerators for development or deployment (FPGAs, FPAAs and specialist cards like Loihi)

#### Experiment dimensions

I think the hardware platform is just another categorical dimension for experimentation

Some charts that might be cool to have at the end of my thesis might be:

- having a scatterplot where the x axis is real-time, the y axis is ops, the points are the models labelled with their categorical data (e.g. `CPU-BPTT-LIF..` or `FPGA-STDP`.., `memFPAA-RES..` etc.) (e.g. circle->CPU, square->GPU, triangle->FPGA) from this we can see:
  - the models in the upper half represent models which have potential for further hardware optimization
  - the models in right half represent models which can be used today
- a bar chart with the x axis being models labelled with their categorical data, grouped and coloured by their hardware platform and the y axis being power consumption, from this we can see:
  - the power efficiency of different hardware platforms and the models that take advantage of this

#### Writing models

For the most idealistic benchmarks it would be good to see each model as if it where implemented on custom hardware that allows it to be efficient. GPUs contain custom hardware for ANNs so it seems unfair to compare SNNs in this context without their custom hardware. In this context I beleive real-time efficiency is less important than the operational efficiency (FLOPs, eFLOPs, SOPS, etc.) as the fundemental operational efficiency can give a better indication of potential future performance for models which don't currently have optimized or optimal hardware (e.g. most neurmorphic models). Admittedly I might just be thinking this as it would more likely lead to an outcome that shows neurmrohpic models as better (if its harder to make optimal hardware maybe its unfair to assume optimal hardware, given this also worth considering real-time with current hardware).

An interesting approach might be writing models in whichever formats offers the best ability to estimate their optimal performance.

This may be a HDL or an asyncrhonsous HDL for an FPGA or FPAA. I like this since it seems software-hardware co-design are fundamental to neuromorphic systems and really optimizing systems (does this count as mono-design or something?)
It would also be interesting to see if I can use a memFPAA to test memristive functionality.

FPAA for £3,356 (https://okikadevices.com/collections/socfpaa, https://okikadevices.com/collections/otc2902k-soc-fpaa-development-board/products/otc2902k-development-board-for-polymorphic-fpaa-with-56-cabs-42-clbs-and-msp430-microcontroller) maybe get access on loan or through uni

> For lower university and student pricing, please contact Okika Devices sales team at sales@okikadevices.com

a table on asynchronous HDLs:

|Layer|Typical user|Example tools / languages|How it reaches silicon|
|---|---|---|---|
|**Graphical block level**|Algorithm or ML researcher|- Scilab/Xcos palette in the open-source _OpenFPAA_ VM[4](https://hasler.ece.gatech.edu/FPAAtool/index.html) - AnadigmDesigner 2 CAM drag-and-drop environment for Anadigm chips[5](https://anadigm.com/_doc/UM020800-U001.pdf)[6](https://www.electronicdesign.com/news/article/21186889/programmable-analog-design-software)|GUI → modified VPR place-&-route → _.swcs_ switch-list loaded over USB[3](https://hasler.ece.gatech.edu/SoCFPAA/Remote_system_paper.pdf)|
|**High-level script / DSL**|Embedded & ML engineer|- Python-based _ASHES_ and RASP30 text flow (Python → Verilog → BLIF)[7](https://afolabiige.me/assets/ORS_2023_2024.pdf) - MATLAB/Simulink export to Xcos for legacy flows[4](https://hasler.ece.gatech.edu/FPAAtool/index.html)|Script generates BLIF netlist → router → programming file|
|**Analog HDLs**|Mixed-signal designer|- **VHDL-AMS** behavioural blocks automatically decomposed and synthesised to FPAA macrocells[8](https://dl.acm.org/doi/10.1145/605440.605445)[9](https://eprints.soton.ac.uk/465792/1/996904.pdf) - **Verilog-A / Verilog-AMS** models; open compilers such as _OpenVAF_ exist[10](https://github.com/pascalkuthe/OpenVAF)|HDL → behavioural synthesis (function decomposition, macrocell selection, placement & routing)[8](https://dl.acm.org/doi/10.1145/605440.605445)|
|**Spice-level netlist**|Circuit specialist|Any SPICE dialect exported by the above tools or hand-written|Direct mapping into CAB primitives by the compiler|

### Meeting 01/07/2027

- Likely literature review submission will be in
- December and progression meeting will be in January.
- Share some notes
- check I have permissions in the GitHub group
- using overleaf with uni allows github sync and offline
- HPC resources for York https://vikingdocs.york.ac.uk/. Your Viking project code is "elec-apnn-2019". Please forward the code to members of your group/project, and ask them to complete the user account application form: https://goo.gl/forms/0Uhl5sIOhFlYtZc63 Please make sure you are logged into Google with your University account before trying to complete this form. You will also need to complete the form if you intend to use Viking yourself. The documentation for Viking can be found at: https://wiki.york.ac.uk/display/RHPC/VK1%29+How+to+access+Viking

### Thoughts

- Justify questions in literature review and link to papers
- Can draw from error checking
- Chip vs monolithic for detecting just sensor vs actuator degradation
- Neuronal diversity fitting or optimization might take inspiration from KANs
- The thesis guides the reader to the point they can appreciate and understand the results
- Background describes methods so someone not in the specific field would understand
- Literature report builds up to this maybe only doing 1/3 page
- Think about initial experiments
- Noise/degradation is a dimension (it can be random or a dropout or an adversarial network)
- Should talk about risks and ethnical considerations in viva
- He's away next week
- Can have longer meeting if I have something specific to discuss
- lookup on policy vs off policy and more reinforcement learning stuff

### 10/06/2025

- How to balance using frameworks vs writing from scratch?
- Did he read the paper on reinforcement learning I asked him about?
- Best way to avoid slowdown is to just write each SNN in Rust from scratch but as a `main.rs` and just copy and pasting stuff but not over designing some shared functionality
- martin recommended sensor fusion as interesting area, like blending accelerometer with DVS to detect movement in background from camera movement "filtering sensors (e.g. DVS)" can also investigate where in a network sensors begin to merge or interfere with each other
- martin said create hierarchy of questions to figure out experiments, chapters and overall thesis and wider field questions like "can SNNs go further than DNNs"
- delay/feedback/attention mechanisms are interesting, what are the different affects, is more recurrence better? Does this just count as more memory? Is the implications recurrence of SNNs a key advantage over DNNs. If all are turing complete whats the most efficient model for a given substrate, a map of neural compute models over substrates is interesting, "pushing as much computation into the physics"
- getting metrics for how complex or recurrent a model is is difficult

### 20/05/2025

The paper I asked for feedback on seems to make a bold and overly confident conclusion upon something that is difficult to justify, it would better to explore this topic in more depth both in terms of complexity and in terms of doing a more thorough exploration of the parameter space to make conclusions more fairly.

- PhD needs to be "novel" (cover something people haven't covered enough etc.)
- look more into evolving spiking neural networks: and dynamic evolving spiking neural networks
- an idea is looking at simpler vs complex sensors and less vs more biologically plausible sensors and how they interact with models. power, complexity, bandwidth
- an interesting idea is that data penetrates the network different amounts
- a fun idea is a force-feedback but not based on physical feedback but based on a model feedback
- include in notes thoughts on quality of the paper

### 06/05/2025

- what does he think of the 2024 paper on IsaacGym DRL since my thesis could end up looking like this. Send him paper https://www.nature.com/articles/s41598-024-77779-8. Recommendation create separately smaller things that are foundational components. Use small experiments to look at how to analyse data (e.g. confusion matrix).
- writing from scratch using cross-link exhibition inhibition neurons, sometimes spontaneous spike rate to give constant excitation to mimic bias in DNNs. A morse code would be a more complex interesting example. Maybe greycode might be better/easier but less interesting. Dive bit deeper on XOR maybe from scratch maybe manually maybe different Encoding, different learnings with basic spikeprop.
- play either robot simulator doing basic algorithm (maze following/obstacle avoidance) some are playerstage, gazebo, vrep, mujocu, isaacsim
- formal supervision is just uni check that supervision is happening so just log meeting that was closest to date in email, formal is just regular bussiness, TAP are more serious after 3 then every 6, progression meetings are most serious every year
- experimentation could a SNN learn more human-like (e.g. mnist example that humans can't identify)
- during my thesis would I publish multiple papers, does the whole thesis get published? Think of questions and experiments, with conferences and sub-questions and sub-experiments. You don't need papers to pass PhD but they derisk thesis, demonstrating value and a way to hedge against examiner having a negative view or lack of novelty
- literature review would involve a appraisal and reading paper and clustering (e.g. why do 1 out of 20 use transfer learning is this a gap or a difficult problem, is this under-explored)
- what does the academic career path look like are there any resources he recommends that cover this and stuff to do to set myself up for it if I want

### 29/04/2025

- Controller problem Vs control problem
- Don't need novel idea but idea of where to drive to find novel problems
- EB sensors vs classical sensors or their combination and integration into some kind of sensor matrix l, object detection is less investigated with EB cameras
- you could construct an environment that favors EB sensors and handicaps frame based sensors
- picking wider benchmark thing this should be fine as long as constantly asking why, emotion of thinking this sort of benchmark/comparison is bit si interesting can be a little ignored for now
- things to explore, EB sensors uses cases and why, wider computer vision with SNNs, computer vision field is too vast to cover
- look at YOLO thing, see if hyst having spiking version is good

### 22/04/2025

Maybe an approach to handling learning things of greater complexity is a cost function that grows in complexity over time

This adaptive/evolving cost function could be intrinsically tied to our imagination, giving us a way to both accelerate and reinforce learning while maybe helping repeat the memory to redistribute learning to areas that are slower to adapt. You can imagine we can consciously very quickly understand how we need to move our hands to play a piece of music, but it takes time for us to subconsciously learn how to move our hands to actually play the music.

This could also indicate different parts have different learning rates, possibly there is a foundation part with zero learning rate.

There is also an idea that as we learn things and integrate these into our memory our brain adjusts these memories when it learns related things, could we have memory of similar things differently encoded at the same time?

There is an idea of "generate memory" which actually reimagines our memories using our new sub-systems to re-encode or adjust older memories. Does this happen only when they are access or is our brain constantly shuffling around our memories? (possibly to optimize space)

### 08/04/2025

- Nnmnist data set
- Data fusion
- Encoding
- Try looking into sensors and interfacing micro circuits
- How do different sensors and circuits compete with each other
- How would reflexes compete with consciousness (sub circuit with main circuit)
- Would a drone get phantom limb syndrome
- Look at typical nn transformers

### 01/04/2025

phd papers may be easier

- look at where it's useful why it's useful and what field it's useful
- neuromorphic workshop at end of may he will send link
- do shortlist based on phd objectives and what fits
- look at difference between having separate chips for training and learning vs online
- dendritic computing
- rewrite proposal into abstract for event
