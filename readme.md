Model files in the NEURON simulation environment from the paper

"Effects of synapse location, delay and background stochastic activity on synchronising
hippocampal CA1 neurons"

by Alessandro Fiasconaro and Michele Migliore

Chaos Solitons and Fractals X 2024


Usage:
 
Auto-launch from ModelDB or:

Compile the mod files with `mknrndll` (mswin or graphical mac) or
`nrnivmodl` (windows/mac/unix/linux)). Start the simulation by (windows/mac/unix/linux) typing
on the command line:

```
nrngui mosinit.hoc
```

or (mac os x) drag and dropping the `mosinit.hoc` file on the nrngui
icon or (mswin) double clicking on the `mosinit.hoc` file.


After selecting the e-type and the corresponding input current, simulation will run a typical simulation as calculated in the paper. The main parameters of the simulation can be changed inside the `mosinit.hoc` file:

```
  Nexp    = 1    // Nr of simulations
  wi      = 0.05 // synapse inhibition weight 
  ws      = 5e-4 // synapse excitatory weight
  Nsyn    = 20   // Nr of synapses in each soma  
  ds[0]   = 100  // proximal synapse distance (fixed in the paper)
  ds[1]   = 150  // distal   synapse distance (variable) 
  Dsd     = 20   // width of the synapse distribution aroud their mean values ds[0] and ds[1]
  chnoise = 1    // 1=Poisson distributed pulsed synaptic inputs
  FreqInp = 60   // mean input frequency of the pulsed inputs 
  del     = 2    // delay on the activation of the inhibitory response
```