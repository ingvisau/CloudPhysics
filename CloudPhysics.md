# Cloud Physics

## *Cloud Thermodynamics*

*Clouds are mixtures of vapor, dry air and water/ice. The atmosphere is approximately an ideal gas.*


**Daltons law**: $P=\Sigma p_i$
For each gas $i$, the ideal gas law applies:
$P=p_d + e =nRT$ , 
$n-$ number of moles per unit volume. $n=n_d + n_v$
$p_d-$ partial pressure, dry air
$e-$ partial pressure, vapor

**Mole fraction:** $y_i=\frac{n_i}{n}=\frac{p_i}{p}$ 

**Specific Humidity**
A mass-based expression for the amount of water vapor in the air.

$$q_v=\frac{\rho_v}{\rho_{air}}\approx\epsilon y_v
$$

where $\epsilon=M_v/M_d=0.622$ is the ration of molar masses of water and dry air, and $n_d=n-n_v$.

**Mixing ratio:** $r_v=\frac{\rho_v}{\rho_d}=\frac{q_v}{1-q_v}$

Expressing the equation of state in an alternative, mass-based way:

$$p=\rho_{air}R_d(1+q_v(\frac{1-\epsilon}{\epsilon}))T=\rho_{air}R_dT_v
$$

where $T_v$ is the virtual temperature, and $R_d(=R/M_d)$ is the dry-air gas constant.

#### Adiabatic Isobaric Processes
Many atmospheric processes are well approximated by the adiabatic (q=0) and isobaric (dp/dt=0) reference process, for example:
* Mixing of two air parcels
* Evaporation of rain drops at a fixed height.

The enthalpy $h=u + pv$ is conserved for such process.
:::warning
Recall that:
$\begin{align}
dh &= du+dpv(=0)+pdv\\
&=du+pdv = c_vdT+RdT\\
&=(c_v+R)dT=c_pdT
\end{align}$

:point_right: $dh$ corresponds to the heat required to increase the temperature of a material with $dT$ at constant pressure.
:::

**Multiphase system of dry air, vapor and liquid**
$h=y_dh_d+y_vh_v+y_lh_l$
$\frac{dh}{dt}=0$
 
$y_ddh_d+y_vdh_v+y_ldh_l+h_ddy_d+h_vdy_v+h_ldy_l=0$ **(1)**


No change in amount of dry air => $dy_d$=$0$ ,
Changed amount of liquid water must come from vapor, and vice versa => $dy_v$=$-dy_l$

From yellow box: $dh_d=C_{p,d}dT$ , $dh_l=C_{p,l}dT$

Inserted in **(1)**:
$dh=y_dC_{p,d}dT+d(y_v(h_v-h_l))+(y_v+y_l)c_ldT$

$h_v-h_l=l_v$ : *latent heat of vaporization*
$y_v+y_l=y_w$

:arrow_down: 

$(y_dc_{p,d}+y_wc_l)dT=-d(l_vy_v)$  **(2)**

***Define:*** 
Specific heat of the cloud system: $[c_p]_{cloudsystem}=y_wc_l+y_dc_{p,d}$

We can  now use ***(2)*** to define *wet bulb temperature*:

$$\int_{T}^{T_{wb}}c_pdT=-\int_{y_v}^{y_{vs}}d(l_vy_v)
$$ 
$y_{vs} -$ mole fraction of water vapor at saturation

:arrow_down: 

$c_p(T_{wb}-T)=-l_v(y_{vs}(T_{wb})-y_v)=-l_v(\frac{e_s}{p}(T_{wb})-\frac{e}{p})$

$T_{wb}=T-\frac{l_v}{c_pp}(e_s(T_{wb})-e)$

**Wet Bulb Temperature:** The temperature you get by evaporating water until saturation is reached.

**Equivalent temperature:** If we instead integrate **(2)** from $T$ to $T_e$, and $y_v$ to $0$, we get $T_e$, which is the temperature we would get if all water would condense out (thereby releasing latent heat to the air).

:::info

**$T_v-$ Virtual Temperature:** 
*The temperature a dry air parcel must have to have the same density as a moist air parcel.*
$$T_v=(1+q_v(\frac{1}{\epsilon}-1)\approx (1+0.61q_v)T
$$
$T_v > T$, because most air is lighter than dry air, so a dry air parcel needs to be warmed up to obtain the same density as the moist air parcel.

**$T_{wb}-$ Wet Bulb Temperature:**
The temperature you get by evaporating water until saturation is reached.

**$T_e-$ Equivalent Temperature**
Condensing all vapor, temperature increase give $T_e$.
$$T_e=T+y_v\frac{l_v}{c_p}=T+e\frac{l_v}{c_pp}
$$

**$T_d-$ Dew Point Temperature**
The temperature reached by cooling moist air to saturation, holding $p$ and $r_v constant.$
:::

## *Cloud Microphysics*
*How do cloud particles form, grow and interact with each other?*

> Clouds are the places in the atmosphere where water changes phase. Water vapor enters a cloud and is converted, by one mechanism or another, into liquid and/or solid phases of water. Nucleation is the process by witch these condenced phases are initiated.

## Nucleation

* *"Kjernedannelse"*
* There is an energy barrier to the formation of cloud particles (drops and ice crystals) because the new phase has lower entropy

:::info
$\Delta\phi = \phi_V-\phi_L =\frac{l_v}{T}$
:arrow_down:
$\phi_L-\phi_V=-\frac{l_v}{T}$
:::

HOWEVER, if the thermodynamic driver, supersaturation, is large enough, the phase transition will take place anyway!

* Phase transformations:
 ![](https://hackmd.io/_uploads/Hyl4LC_rh.png)
 
### Formation of cloud drops (liquid phase)
::: success
Homogenous nucleation can be disregarded in the atmosphere.
:::

:::info
**Embryo:** The critical embryo, or germ, is a molecular cluster having critical radius $r_d^*$, where the free energy $\Delta G_h$ has its maximum value. The germ sits on the cusp between evaporation and growth, so it exists in a state of equilibrium with its environment. (see p. 282)
:::
![](https://hackmd.io/_uploads/H1bsU1Yrh.png)
* Fig. 7.4 illustrates the critical droplet size and its relation to clusters, equilibria, embryos and nucleation.
* Imagine...
    * A volume of air with water vapor, with pressure lower than necessary for nucleation.
    * Random merging of water vapor molecules to embryos, but with too low binding energy to be sustained.
* Formation of embryos: a random spontaneous process. Must employ the theory of statistical quantum mechanics to explain the process
    * Use of micro-thermodynamics also reveal correct results... Here we use Gibbs free energy (not pensum in this chapter).

### Effect of substrate to lower the energy barrier:
#### Insoluble surface 

The presence of the insoluble surface aids the nucleation of liquid by lowering the free energy to form liquid at any given saturation ratio.

![](https://hackmd.io/_uploads/BywEdktr3.png)
![](https://hackmd.io/_uploads/ByiOuJYSn.png)
* Fig 7.9: Contact angle for hydrophilic, neutral and hydrophobic particles VS. saturation ratio.
    * Hydrophobic: $\theta$ ~ $150-180^\circ, S_{th}$ ~ $4.3$
    * Neutral: $\theta$ ~ $90^\circ, S_{th}$ ~ $2-3$
    * Hydrophilic: $\theta$ ~ $0-30^\circ, S_{th}$ ~ $1$


#### Nucleation on an insoluble particle
![](https://hackmd.io/_uploads/HJxhqJtHn.png)

Spherical cap of liquid forms on the curved surface of the particle, which acts as a discrete nucleating agent.
* Large particles that are easily wettable (have small $\theta$) serve as better condensation nuclei than do particles composed of hydrophobic substances (which have larger $\theta$)

#### Formation of liquid on a soluble particle
An aerosol particle composed of water-soluble matter (e.g. inorganic salts) can initiate the liquid phase much more effectively than an insoluble particle can.
* Water breaks the ionic bonds of a salt, which otherwise require high temperature to melt.
* The dissolved salt lowers the equilibrium pressure.
* **Deliquescence:** dissolving a solid particle into a liquid solution.
    * Occurs at RH < 100%
    * Water molecules accumulate faster than they leave.
    * The solute ions in effect act as molecular anchors by retarding the evaporation of water molecules.
    * Approximated as an equilibrium process: solid > liquid incrases entropy --> It is not nucleation!
        * Nevertheless, atmospheric particles, because they aid the formation of liquid from water vapor, are CN.
![](https://hackmd.io/_uploads/Hy7eKxYSh.png)

* Fig. 7.11: A particle of NaNO~3~ was exposed to air at different relative humidities and allowed to come to equilibrium and its mass *m* measured relative to that in the dry state, *m~0~*. At humidities below the onset of deliquescence, water vapor adsorbs (hold as film on surface) onto the dry surface, but the amount of water is insufficient to disrupt the crystalline lattice. The water molecules stay on the surface for a while, but then desorb with little effect on the solid. As the humidity rises, the concentration of adsorbed molecules increases, and the accumulated water is eventually sufficient to dissolve the salt. At the deliquescence-point (S~deliq~)the non-linear process of dissolution takes place: The adsorbed water breaks some of the ionic bonds holding the salt together and removes the ions from the solid. These ions that are sequestered (isolated) in the liquid covering the particle hinder the evaporation of the water molecules. The lowered vapor pressure (from the solute effect, as described by Raoult's law) leads to further uptake of water molecules from the vapor phase and new opportunities for further dissolution of the solid. The process of vapor uptake continues until the solid completely disappears and all the ions become part of the liquid solution droplet
    * (NH~4~)~2~ Ammonium sulfate (fully neutralized form of sulfuric acid): $S_{deliq}$=0.79
    * H~2~SO~4~ Pure sulfuric acid: always liquid, just the relative proportions of water and sulfate vary with the humidity.
    * Growth after deliquescence: hygroscopic growth.
    * Hygroscopic growth factor: $GF=\frac{D_p(s)}{D_p(0)}=1 + \frac{A_{hyg}S}{1-S}$ 

![](https://hackmd.io/_uploads/ry6VFm5rh.png)
* Fig. 7.14: $S_{bulk deliquescence} < S_{particle deliquescence}$

### Formation of the solid phase
Ice can in principle form from the vapor phase by either of two pathways:
* **Direct pathway:** Water vapor to particle (deposition) is only possible if an ice nuclei (IN) exists.
* **Indirect pathway:** First condensation to water, then freezing. Homogenous nucleation of liquid phase is possible, i.e. without IN.
    * Energy barrier to the transition from liquid to solid: Large super cooling $\Delta T_s = T_0-T,$ $T_0=0^{\circ}$ is needed.
    * $\Delta T$ has a direct relationship to change in chemical potential (generalized form of Gibbs free energy)
        * $\Delta \mu = \mu_L-\mu_S=RT*ln\frac{e_s}{e_i}=l_f\frac{\Delta T_s}{T_0}$

#### Theory of homogenous freezing -- find the treshold temperature for freezing to occur
*We want to calculate the change in system free energy to form a microscopic embryo of the new phase (ice)in the parent phase (a droplet of supercooled water).*
1) Calculate the free energy to form embryos in the new phase.
    * Consider a microscopic embryo (hexagonal prism)of ice within a droplet. Area of hexagonal prism is larger than a sphere by a factor $\alpha$, and volume factor $\beta$.
        * $V_i=\frac{4}{3} \pi r_i³*\alpha$, $r_i$-- inscribed sphere
        * $A_i=4\pi r_i²*\beta
    * Change in system free energy to form embryo:
    $\Delta G_i=$-- volume contribution + surface contribution
    $=V_i n_i \Delta \mu +A_i*\sigma_{IL}$
    $=-\frac{4}{3} \pi r_i³ \alpha n_i l_f \frac{\Delta T_s}{T_0} + 4 \pi r_i² \beta \sigma_{IL}$
    $n_i-$molar density of ice, $\sigma_{IL}-$interfacial energy between solid and liquid
2) Determine the critical point - the free energy must overcome.
    * $\frac{\delta}{\delta r_i}(\Delta G_i)=0$ --> Gives maximum value of $\Delta G_i$; $\Delta G_i^*$
        * Find expression for $r_i^*$, and put into $\Delta G_i$ =>
    * $\Delta G_i^* = \frac{16\pi \sigma_{IL}³\xi}{3(n_il_f\frac{\Delta T_s}{T_0})²}$, 
        * ($\xi =\frac{\beta ³}{\alpha ²}-$Net geometrical factor accounting for "non-sphere" geometry.)
    * :exclamation: :
        * $\Delta T$ large ->  lower energy barrier.
        * Small $\xi$ (area/volume) -> lower free energy barrier
        * Very sensitive tpo $\sigma_{IL}$, which is difficult to determine.
3) Calculate the rate of nucleation, frequency of new molecules added to the embryo.
    * This applies to the formation of ***one*** embryo, but what is the rate at which molecules are added to the critical embryo per unit volume?
    * $J_i=J_1n(r_i^*)$, volumetric nucleation rate.
    $J_1-$ The rate at which ***one*** critical embryo acquires molecules from the liquid $(s⁻¹)$
    $n(r_i^*)-$ The number of critical embryos (germs) $(m⁻³)$
    * How do we determine J?
        * The mechanism by which new water molecules build into the ice embryo differs from nucleation from the water phase for which the supply of water is limiting. The limiting factor here is the ability of the molecules to leave the liquid and enter the ice.
        * Nota that: in contrast to the nucleation of liquid droplets from vapor phase, the nucleation of ice in supercooled water involves two energy barriers:
            * The activation energy $\Delta g_{act}$: The ability of water molecules to leave the liquid, and enter solid state. The molecules in the liquid are already bonded together, and these bonds need to be broken before the molecules can form new "ice"-bonds. The energy "bump" (see fig. 7.18).
5) Estimate the treshold conditions.


#### Effect of solute (dissolved salt) on freezing (haze)

* Water activity: $a_w=\frac{n_w}{n_w+in_s}$

:::info
**Activity**
High a~w~ -> More dilute solution, and more likely that ice forms
Low a~w~ -> More salt and less likely for ice to form (few "isolated" pockets of water)
:::

* The small size of haze droplets reduces the probability of ice to form (higher supercooling needed)
* *Note: Solute has strong attachments to water molecules, which HINDER the water molecules to arrange into ice lattice structures*

#### Heterogenous nucleation of ice
* Observations show that ice particles are found in clouds for temperatures well above the treshold for homogenous freezing 
--> Ice Nuclei (IN) must be present.

![](https://hackmd.io/_uploads/SJ9TtzMLn.png)

* Fig. 7.23: 
    * Solute lowers the freezing and melting point
    * IN increases the $T_f = T_{f, het}$
    * Freezing (both homogenous and heterogenous) is stochastic processes.
* **Ice Nuclei:**
    *  Insoluble
    * Crystalline structure similar to the hexagonal lattice of ice.
    * Nucleation takes place on the surface of the particles.
    * Concentrations: IN ~ 1/L, CCN ~ 10⁵/L
    * Silver Iodide (AgI) $T_f$ ~ $-4^\circ C$
    * Not all good IN have ice-like crystalline structures.
* Different ice-forming mechanisms:
    * **Deposition nucleation:** The particle causes a transition from vapor to ice at S < 1 < S_i.
    * **Contact nucleation:** Freezing of supercooled drops upon contact with IN, Brownian diffusion.
    * **Condensation freezing:** An IN coated with salts (sulfate) may first serve as CCN then later as IN, when the drop is sufficiently diluted.
    * **Immersion freezing:** Mineral particle, with some hygroscopicity, but not soluble, enters the drop, and then freezes when sufficient $\Delta T_s$



## Growth from the vapor

We have cloud particles, via aerosol activation or nucleation. How rapidly and by what mechanism do the particles grow?

**Growth by:**
* Vapor phase increase molecule by molecule.
* Collection of other particles (Ch.9).

:::info
**Remember**

$S\equiv\frac{e_\infty}{e_s(T_\infty)}=s+1 ,$ (saturation ratio)

$e_\infty -$ vapor pressure in the interstitial air.
$e_s(T_\infty) -$ equilibrium vapor pressure over plane surface.

$s\equiv\frac{e_\infty}{e_s(T_\infty)}-1 ,$ (Supersaturation)


**Köhler function**
Reference supersaturation accounting for solution and curvature.

$s_K=\frac{e_{eq}}{e_s}-1$

$e_{eq}-$ equilibrium vapor pressure of the solution droplet.

When the particle is ice, then $e_eq$ and $e_s$ are replaced by equilibrium vapor pressure of ice, $e_i$ to obtain the supersaturation with respect to ice: $s_i\equiv e_\infty/e_i - 1$

The relative driving factor for the vapor growth of a cloud droplet is the supersaturation difference:

$s-s_K=\frac{e_\infty - e_{eq}}{e_s(T_\infty)}$
:::

**Growth by vapor proceeds in three steps:**
![](https://hackmd.io/_uploads/SkzydSz8h.png)

1) Mass transport from afar (many radii distance away)
2) Surface processes: Removal of vapor by condensation, Gradients in capor, Latent heat release and warming adjacent to particle, Gradients in temperature.
3) Energy transport, Transport of heat away from the particle.

### STEP 1. -- Mass transport onto the particle 

$I_v-$ Total flow of vapor toward the particle (mol/s).

$\frac{dm_p}{dt}= -M_vI_v,$

$M_v-$ molecular mass of water
Positive direction defined as outward from the particle.

The net flux at any point follows ***Fick's first law***:
$$\Phi=-D_v\Delta n
$$

$D_v-$ diffusivity
$n-$ molar concentration, $n=\frac{e}{RT}$

:arrow_down: 

Vapor flow into the particle is the integrated flux of vapor across the particle surface:
$$ \frac{dm_p}{dt}=-M_v \oint\Phi_{v,surf}dA
$$

--> Applies to a particle of any shape.


***Spherical liquid drops -- Maxwell's theory***
Air is treated as a continuum up to the droplet surface, uniform flux of water toward the drop.

*Skip some steps...*

Maxwell's mass growth law:

$$ \frac{dm_d}{dt}=4 \pi r_d \rho_L G*(s-s_K)
$$
$G-$ constant that takes into account diffusivity(D) and latent heat.

The mass of a droplet varies with the radius --> "Linear growth law":
$$r_d\frac{dr_d}{dt}=G*(s-s_K)
$$

:::success
***Notice:***

* $\frac{dm_d}{dt} \propto r_d$ 

    --> Total mass is aquired most rapidly by larger droplets.
    
* $\frac{dr_d}{dt} \propto \frac{1}{r_d}$  

    --> Condensation favor the smaller drops, which lead to a narrowing of droplet size distribution.
:::

:exclamation: See lecture 13 for refinements of the theory

### Limitations of Maxwell's theory

#### Ventilation effects

#### Surface effects 
Mass and energy is not transferred between the phases with 100% efficiency. Despite knowlegde gaps in the how these mechanisms works we still need to take them into account. **The mass accomodation coefficent** $\alpha_m$ is used to represent the actuall fraction of impinging water molecules that acually becomes a part of the droplet. **The termal accommodation coefficent** ($\alpha_T$) represent the efficiency of the air molecules to extract the excess heat from the droplet. 
* Best esitmaes $\alpha_m$ = 0.06,  $\alpha_T$ = 0.7 

Maxwell's theory also assume that equilibrium extends all the way to the surface of the droplet, however the droplet grows only if $e < e_{eq}$, therefore if taken literally, Maxwell's theory does not permit growth or evaporation to occur. The free molecular region starting at a small distance $\Delta$ from the surface. Going from the continuum region to the free molecular region there is a jump in the vapor concentration n. This jump is largest for the small droplets. The vapor jump is the small diviation from equilibrium required for droplet growth to occur. 
![vapor_jump](https://hackmd.io/_uploads/ByGzbFNLh.png)
 
### Vapor growth of ice crystals
The fundemental distinction between the growth of cloud droplets and ice crystals, is the complex shapes of ice crystals. How to best adjusting the growth laws to account for the complex shapes is still debated. 

The most convinent and general approach uses a analogy from electrostatics replacing the radius by the particle capacitance C. This give the follwing compact form for the growth of the ice crystal: 

$$\frac{dm_p}{dt} = 4\pi C\rho_I G'_I s_i
$$

The capacitance represent both the same and size of the particle. The vapor concentration is treated analogous to the electric field. Such as the equation above allow us treat the particle as a point sink of vapor with considering the complex geometrical shapes. 

#### Habit formation

The deposition coeffienct varies a function of temperature for the prism and basal face of the growing ice crystals. This creates prefriential ice crystals shapes at different temperatures. If the enviromental condition changes as the ice crystal grows that would also change the deposition coefficient and thus alter the preferential growth face. Which means the ice crystal can have secondary habits different from the primary habits. The growth ratio of the different faces is described by the follwing equation:

$$
\frac{R_B}{R_P} = \frac{\alpha_B(S_B)S_B}{\alpha_R(S_R)S_R}
$$
Where $S_B$ and $S_R$ is the supersaturation with respect to the basal and prism faces. 
## Growth by collection


* **Collision-coalescence:**
Both particles liquid. The larger "collector" drop collects one or more smaller drops, because of the difference in fallspeeds. Basic mechanism of rain development in warm clouds. The collision coalescence explains why it can start to rain after only 20-30 minutes since the cloud first appeared, despite the decreasing rate of condensational growth for larger droplets. It starts when some droplets in the clouds excced about 15 $\mu m$. 

* **Riming:**
Ice crystal colliding with supercooled cloud droplets, which freeze on impact. Heavy riming lead to graupel and hail (if the conditions are appropriate). Riming can also occur in stratoform cloud if the ambient supersaturation is above that of liquid such that the WBF process does not consume the supercooled droplets.  

* **Capture nucleation:**
Large supercooled drop capture a small ice crystal, and freezes.

* **Aggregation:**
Ice crystals colliding and sticking together. Most effective at higher temperature close to 0 K, e.g big snowflakes.  

--> In every case, the outcome of collisions depends on the relative motions of the particles involved.

#### Not all cloud drops coalesce!
When two droplets collide we have three possibilities:
1.  Collected droplets merges with collector drop
2. Temporarily coalesce and then seperate retaining their original entities 
3. Coalecenes but then the droplets break into many smaller droplets. 


#### Particle fallspeed

*Terminal fallspeed* $v_p$ : Gravitational and drag forces balance, maximum downward speed. A measure of motion relative to the air in which it resides.

* As the particle gains speed, it pushes air out of the way and so experiences air resistance, expressed as the drag force $F_D=F_D(v'_p)$, which increases with the instantaneous (time-dependent) speed $v'_p$ of the particle relative to the air
* We neglect accelleration time, and assume that cloud particles always fall at their terminal speeds.
* NB: terminal fallspeed is relative to air, and must not be confused with the particle's ascent rate $dz_p/dt=w-v_p$, which is the rate of motion relative to the Earth when the air is rising with speed $w$.

:::info
*How can we determine $v_p$?*

Pressure at stagnation point: $p_{stag}=p_{atm}+p_{dyn}$, where $p_{atm}$ is the ambient pressure at this altitude, and $p_{dyn}$ is the dynamic pressure; the additional pressure that arises from the relative motion of the particle.
Pressure as an energy density [Jm⁻³]: $p_{dyn}=\frac{1}{2}\rho_{air}v²_p$  
--> change of kinetic energy of the air from its value at the stagnation point relative to that in the free stream. 

:arrow_down: 

$F_D(v_p)=p_{dyn}A_cC_D=\frac{1}{2}\rho_{air}v_p²A_cC_D$

$A_c-$ drop cross section  
$C_D-$ drag coefficient  

:arrow_down:

$v_p=(\frac{2g\rho_pV_p}{C_D\rho_{air}A_c})^\frac{1}{2}$  

:arrow_down: 

$v_p \propto \frac{\rho_pVp}{C_DA_c}$  

--> Fallspeed ultimately depends on the ratio of particle mass to the effectice cross-sectional area.
:::

Around spherical particles, the flow around is characterized rather well by the dimensionless Reynolds number, the ratio of the inertial and viscous forces:

$N_{Re}=D-pv_p/\nu_{air}$, where $\nu_{air}=\mu_{air}/\rho_{air}$ is the kinematic viscosity of air having dynamic viscosity $\mu_{air}$.
The drag force can be expressed with $N_{Re}$.

The drag coefficient $C_D$ and the Reynolds number $N_{Re}$ vary greatly with particle size and the type of flow around the particle. To handle this complexity, we divide into several regimes:

![](https://hackmd.io/_uploads/rya-4wQ8n.png)

#### Free-molecular regime ($D_p << \lambda_{air} \approx 0.1 \mu m$)
Air must be treated as a collection of molecules, not as a continuum. Drag force dominated by collisions.  
$v_{p,FM} \propto D_p$

#### Transition regime ($D_p \approx \lambda_{air}$)
Complicated physics -- molecular interactions are difficult to calculate, and continuum assumptions are not valid, empirical correction to Stokes drag.

## Evolution of supersaturation

Upward motion of air parcel --> lower p and $\rho$ --> work on environment --> cooling of air parcel --> reduced equilibrium vapor pressure --> RH increase.

Above cloud base: RH=100%. Excess water vapor depleted by condensation.

* From Ch. 6: *Adiabatic supersaturation development equation*:
$$\frac{ds}{dt}=Q_1w-Q_2\frac{dy_L}{dt}
$$
    * $Q_1=\frac{e}{e_s}(\frac{l_v}{c_pT}-1)\frac{M_{air}g}{RT}$  
    * $Q_2=\frac{e}{e_s}\frac{l_v²}{c_pRT²}+\frac{p}{e_s}$  


Now want to introduce the effects of aerosols.
* Express ds/dt in terms of $\omega_L=LWC, (g/m³_{air}$):
$$ \frac{ds}{dt}=Q_1w-Q_2\frac{d\omega_L}{dt},
$$
    * $Q_2=\frac{l_v²}{M_wpc_pT}+\frac{RT}{(M_we_s(T))}$  
    ($\frac{e}{e_s}\approx1$)  
    --> Must be solved numerically to gain the evolution of supersaturation, $s(t)$!
    

**General behaviour of the equation:**
![](https://hackmd.io/_uploads/By8MJ1rL3.png)

* Linear increase of $s$ beyond 0. Activation of CCN -> cloud drops form and start growing from condensation.
* $s$ reaches a peak value $s_{max}$, depletion becomes larger than production. $s$ stays above 0.
* A quasi-stationary value of $s$, $s_{qs}$, is reached as sources and sinks balance.

**Mathematical solution of $\frac{ds}{dt}$; Extended theory:**  
We need to know how $\frac{d\omega_L}{dt}$ changes with time. Two steps: (1) Actvation of CCN and (2) Growth by diffusion.  
(1) Number of cloud drops activated for a change in s from s to s+ds:
$$\frac{dN_d}{ds}=n_{CCN}(s)
$$
$n_{CCN}(s)-$ supersaturation spectrum of CCN, the number of particles that activate in the supersaturation range s to s+ds.  
Accumulated drops is then given by:
$$\int_0^{N_d}dN_d=\int_0^{s(t)}n_{CCN}(s_c)ds_c
$$
where $s_c$ is the critical supersaturation for a particle (Köhler theory).  
New droplets are added to the population only as long as s increases with time and viable CCN remain available in the parcel.  

(2) Activated drops will increase their mass by condensation. Conservation of mass means:  
$\frac{d\omega_V}{dt}=-\frac{d\omega_L}{dt}.$  
The change in mass per volume when drops in the interval $dN_d$ are growing by condensation:  
$\frac{dm_d}{dt}\cdot dN_d$  
The total change in LWC ($\omega_L$):
$$\frac{d\omega_L}{dt}=\int_0^{N_d}\frac{dm_d}{dt}\cdot dN_d=\int_0^{s(t)}\frac{dm_d}{dt}\cdot n_{CCN}(s_c)\cdot ds_c
$$
Now we need an expression for $dm_d/dt$. See lecture notes. In the end, we can have an expression for the evolution of supersaturation that looks like this:
$$\frac{ds}{dt}=Q_1w-A_2sI(s),
$$
where $A_2=2\pi Q_2\rho_L(2G)^{3/2}$ is a factor independent of s, and $I(s)$ is an integral that contains all the information about the formation of new droplets through activation.  

Further calculations require:
1) An assumed CCN spectrum, $n_{CCN}(s_C)$
2) Knowledge of how the updraft speed $w$ varies with time.


**Aerosol influence**  
* Liquid water concentration ($\omega_L$) builds up at a wrate roughly proportional to the integrated concentration of CCN.
    * Low CCN concentration --> low concentration of cloud droplets --> large maximum supersaturation.
    * High CCN concentration --> High $N_D$ --> low $s_{max}$
* Also: $d\omega_L/dt \propto s(t)$ --> the fewer drops in clean air grow faster.
    * Clean air --> few large drops
    * Polluted air --> Many small drops

**Quasi-stationary supersaturation**
Mature stage, rate of depletion of water vapor roughly equals rate of production (by continued uplift). Don't need to account for new activation, because past $s_{max}$, the droplet concentration is fixed.  
LWC depends on the instantaneous droplet size distribution. Product and generation terms equal to each other gives -->
$$s_{QS}=\frac{Aw}{\bar{r_d}N_d}
$$





## Warm Clouds
![](https://hackmd.io/_uploads/By4Rm3NI2.png)

#### Broadening of the cloud drop size spectrum
Often before collisions can occur we need a broadening of the cloud droplet spectrum. This is especially for continetal clouds where the CCN concentrations are high resulting in many small droplets. Processes that can cause broading on the drop sepctrum are entraiment by turbulence. Another factor is the presence of giant CCN, which allow some drops to grow to the size for when collision-coalescence start to take effect. Another part is the lucky drop.    

#### Development of warm rain 
* **Continuous collection**:Assumes that there already exist a few large collector drops created by some of the processes above. The collection kernel of the collector drop is the effective volume swept by the falling drop, which depend on the collector drop size. When the size of the collector drop is much larger than the collected drop r~l~ >> r~s~ Then the collection efficiency is constant. A drop growing be continuous collection increase in size exponentially with time.
    * Continuous collection: $dr_d/dt \sim exp(t)$
    * Growth by condensation: $dr_d/dt \sim t^{1/2}$
* **Stochastic collection**: Takes into account probability for every combination of drops to coalesce. The occurance of a collection event is discreate and each collection event increase the mass of the drop incrementaly. Only a few lucky droplets are need to initiate rain. Stochastic collection shift the drop spectrum from small to larger sizes.  

The size of the rain drops are limited by breakup processes e.g. when a the collector drop and a smaller drop coalesce the energy is transfered from the collected drop to the collector drop causing circulations to occur inside of the collector drop and thus the collector drop will eventually break up. 


## Cold clouds
Are clouds that contain ice. Ice particles are common forms of precipitation in the anvil of deep convective clouds and stratiform clouds. We categorize the origin of ice as either primary (e.g. formed by nucleation) or secondary ice particles (formed by fragmentation and splitnering). Very few IN in the atmopshere concentration around 1 #/L. The range of primary ice formation start around -10 ^o^C. 

![](https://hackmd.io/_uploads/r1biJRVLn.png)


#### Seeder feeder effect
Ice cloud above a stratiform cloud starts precipitating. When the ice particle reach the stratiform cloud they start to grow, by the WBF process. The seeding might be intermittent in nature and thus precipitation generated through by a seeder cloud would be "showery".   

---
#### From the book
* A new phase can form only if that new phase is thermodynamically favored.
    * From 3.2: The molar free energy (chemical potential) of water in the new (daughter) phase must be lower than that of the original (parent) phase for the new phase to have a chance of surviving --> then the parent phase is *metastable* wrt the daughter phase (the molecules will be at a lower potential energy once the new phase has formed).
    * Problem with condenced phase from vapor: entropy is lowered. Entropy does not decrease easily in nature, so metastable phases (e.g. supercooled cloud water) can persist for long times
    * --> A new phase of lower energy can form, however, if the thermodynamic driver (chemical potential difference) is sufficiently large.
* Ways of forming a new phase (of a single compound, e.g. water):
    * **Homogenous nucleation:** uniform parent phase, no external agent.
    * **Heterogenous nucleation:** multiple phases, external agent involved.
* Four steps to calculate conditions under which the new phase is likely to form:
    * a) Calculate the free energy to form embryos of the new phase. 
        * Volume and surface contributions to changes in the system free energy --> Result is an equation expressing the free energy change as a function of embryo size and the magnitude of the thermodynamic driver (chemical potential difference)
    * b) Determine the critical point.
        * Determine the embryo size at which the function from a) attains it maximum value --> critical embryo. The free energy to form the critical embryo is the barrier to make the new phase stable.
    * c) Calculate the rate of nucleation.
        * Thermodynamics of embryo formation + kinetics --> frequency with which molecules are added to the critical embryo. Vary greatly with thermodynamic driver.
    * d) Estimate the threshold conditions.
        * " The onset of nucleation is established by choosing a nucleation rate that the user deems significant, then finding the environmental conditions, expressed in terms of the applicable thermodynamic driver, that give that rate."
        
        
## Questions:
* P.294: Bulk deliquescence?