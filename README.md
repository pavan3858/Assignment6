# Assignment6 EE19B010,BADHAVATH PAVAN
## INTRODUCTION
In this assignment,we model a tubelight as aone dimensional space of gas in which electrons are continuously injected at the cathode and are accelerated towards the anode by a constant electric field.
The electrons can ionize material atoms if they achieve a velocity greater than some threshold,leading to an emission of a photon.This ionization is modeled as a random process.The tubelight is simulated for a certain number of turns from an initial state of zero electrons 

### The Parameters
The parameters are :
 n=100,length of the Tubelight.
 M=5,Number of electrons injected per turn.
 nk=500,Number of turns for simulation.
 uO=5,Threshold value of Velocity.
 p=0.25 Probability of Ionization.
 msig=Std-Deviation of M.
 
The above parameters are default values and the user can give his own values via arguments

#### TubeLight Model
A Uniform electric field is present,which accelerates electrons.Electrons are emitted by the cathode with zero energy,and are accelerates due to this field.When the kinetic energy gained is more than the threshold value the collisions will lead to ionisation and the ionized atoms release energy in the form of light.In our model,we will assume that the relaxation is immediate.The electron loses all its energy and the process starts again.electrons reaching the anode are absorbed and lost.Each "time step",an average of M electrons are introduced at the cathode.the actual number of electrons is determined by finding the integer part of a random number that is "normally distributed" with standard deviation of 1 and mean 5.

##### PLOTS
![Figure_6 1](https://user-images.githubusercontent.com/81006760/115153444-8a8c0180-a093-11eb-8eb8-ffa3f2051ef7.png)
Figure1:Histogram of Electron Density

![Figure_6 2](https://user-images.githubusercontent.com/81006760/115153473-b3ac9200-a093-11eb-9ecd-898d257197b0.png)
Figure2:Histogram of Light Intensity

![Figure_6 3](https://user-images.githubusercontent.com/81006760/115153491-d3dc5100-a093-11eb-94c2-75eaff9464c0.png)
Figure3:Electron Phase-space

###### Observations
The electron density is peaked at the initial parts of the tube light as the electrons are gaining speed here and their velocities are not above the threshold. This means that the peaks are the positions of the electrons at the first few time steps they experience

After 10 units the peaks are slowly dying indicating that the electrons have gained enough velocity to participate in collision and ionize an atom. Since collision is inelastic the velocity of
electrons after collisions becomes zero.

The Light intensity also shows peaks which also start to die as x increases. This is due the same reason as above. Most of the electrons reach the threshold at roughly the same positions, leading to peaks in the number of photons emitted there.

This phenomenon can also be seen in the phase space plot.Firstly, the velocities are restricted to discrete values, as the acceleration is set to 1, and we are not yet performing accurate velocity updates after collisions.

One trajectory is separated from the rest of plot. This corresponds to those electrons which travel until the anode without suffering any inelastic collisions with gas atoms. This can be seen by noticing that the trajectory is parabolic. This means that v=kp x , which is precisely the case for a particle moving with constant acceleration.

The rest of the plot corresponds to the trajectories of those electrons which have suffered at least one collision with an atom. Since the collisions can occur over a continuous range of positions, the trajectories encompass all possible positions after x=10.

CONCLUSION

In this assignment we simulated the Light Intensity, Electron Density, Electron Phase Space in a tube light. We observed the dependence of the characteristics of tube light on threshold velocity and probability of ionization.

The Light Intensity is zero initially as the electrons coming from the cathode have zero initial velocity. As the electrons achieve the threshold velocity, they undergo inelastic collision and emit light. For lower threshold velocity, the electrons start emitting light closer to the cathode.

The Light Intensity is very low for low probability of ionization as most of electrons do not undergo collision even after attaining threshold velocity. As the probability of ionization increases the Light Intensity also increases.

In a tube light there exists an initial peak followed by a few dark patches. The position of the initial peak and the dark patches are determined by the initial parameters.
