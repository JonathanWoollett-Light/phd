# Questions

1. Are analogue systems intrinsically better at horizontal scaling?
1. Do biological sensors perform sensor fusion? Would losing your sense of smell worsen your sense of touch?
1. \[[2024 Exploring spiking neural networks for deep reinforcement learning in robotic tasks]\] struggled to apply deep SNNs in reinforcement learning, could using new state of the art training (e.g. \[[2023 Learnable Surrogate Gradient for Direct Training Spiking Neural Networks]\]) approaches mitigate this? (possibly avoiding or minimising the surrogate gradient mismatch)
1. \[[2023 Toward robust and scalable deep spiking reinforcement learning]\] highlighted that one key difference between SNNs and biological neural network is unexplored, this is neuron diversity. How would models with differing degrees of neuron diversity perform and could this diversity (or each neurons type and function) be a trainable parameter and would this provide a practical benefit?
1. \[[2023 Toward robust and scalable deep spiking reinforcement learning]\] noted that experimenting with temporal coding mechanisms (spike-latency or inner-spike interval) on continuous control problems could be interesting.
1. Are more bio-plausible models better at embodied intelligence?
1. Do more efficient (e.g. bio-plausible) systems lead to more powerful systems?
1. Does recurrence have extra value over other forms of complexity?
1. How do we measure model intelligence?
1. How to maximise available intelligence?
1. Is recurrent complexity equivalent to architectural complexity?
1. What is reservoir computing better at?
1. What valleys in the optimization landscape of intelligence has evolution been incapable of traversing?
1. What's the best neuron model?
1. Should do more exploration and less exploitation when optimising for intelligence? (We have remained at the same hardware point in the landscape for 50 years and done no serious exploration)
   1. It seems that to effectively explore this space we need to perform exploration of hardware and software and integrate these together quickly (hardware-software co-design).
1. Are systems with multiple models (e.g. a ML model at the sensor, then one for control) more or less efficient with systems with a single model (e.g. a single ML model gets full sensor output potentially supporting better sensor fusion and information compression/processing)
1. Can SNNs with online learning perform better at control tasks than traditional PID controller systems? (e.g. an electric motor degrades, or each robot is simply slightly different as not all components will be identical)
1. What's the optimization algorithm of the brain?
1. Is the fastest way to AGI to copy a biological brain?
1. Can SNNs perform practical online learning in robotics?
   1. . What are real world examples of where such a system could be useful?
      1. The scenarios where this is practical require restricted communication that prevents using ANNs in a datacentre and instead needing in-situ learning:
         1. Exploration vehicles, underground, undersea or extra-terrestrial.
         1. Disaster response vehicles in communication denied environments as a result of infrastructure damage.
         1. Military vehicles in communication denied environments as a result of infrastructure damage or communication jamming.
      1. There are some scenarios where this could be used, but it may be easier to simply connect to a datacentres and use ANNs:
         1. For sensor degradation, highly sensitive systems (a sensor in a particle collider or gravitational wave sensing).
         1. For actuator degradation, unbalanced systems where components are required to maintain high ranges of functionality and degrade quickly (high-speed or maglev rail).
   1. Can SNNs perform online learning to adapt to degradation?
      1. Is online learning viable with practical hardware within an existing drone?
      1. What would be required of an ANN to perform comparatively to an SNN in this context?
      1. How do different neuron types (LIF, Hodgkin-Huxley etc.) perform in this role?
      1. How do different architectures (feedforward, reservoir, etc.) perform in this role?
      1. What types of sensors are relevant to robotics?
      1. Could this sit in-between the sensors and the controller?
         1. How does this compare in performance to having an full SNN controller that performs both roles.
         1. Could it be a specific piece of hardware?
            1. Could this be attached to existing systems?
      1. What would be the additional cost of the hardware required to implement this?
      1. What would be the additional power required to implement this?
      1. Can this adapt to all sensors degrading?
      1. How much can we degrade sensors before the system fails?
      1. Is there a difference in adapting to sensor degradation Vs actuator degradation?
      1. Is sensor degradation or actuator degradation more pronounced in the real world?
      1. Can sensor degradation be used to evaluate the value of sensors?
         1. Could this work as a method to find the cheapest sensor or set of sensors that still complete a given role?
         1. Could this find the best/worst sensors for the task?
