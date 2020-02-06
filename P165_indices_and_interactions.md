# Indices and Interactions

Flip Tanedo
Physics 165, Fall 2020

## Background: The Game

Thus far we have introduced the *Feynman Game*. We start with a **theory of particle dynamics**:

* a list of particles (represented as lines)
* a list of allowed vertices for how to connect those lines.

The Feynman Game is a way to determine what kinds of quantum mechanical processes are possible. This involved the following steps:

1. Start with some initial state particles (lines coming in from the left), and some final state particles (lines leaving to the right).
2. The initial state may turn into the final state if you can draw a connected graph using only the lines and vertices in your theory. 
   - You can rotate lines and vertices however you need to, all that matters is the *topology*. 
   - You can use as many lines and vertices as necessary to draw a diagram. 
   - You may *not* make up vertices that are not in your theory. 
3. The *order* of a diagram is the number of vertices used. We typically care about *all* diagrams with the lowest order. These diagrams represent complex numbers that are the leading contributions to $\langle\text{out}|\text{in}\rangle$. The rate for this process to happen goes like $|\langle\text{out}|\text{in}\rangle|^2$. 
4. Just because a process is *dynamically* possible (quantum mechanics allows it), it does not necessarily happen. It must also be *kinematically* possible. To check this we use the following rules:
   - *Each* initial and final state particle is **on shell**, this means that the (special relativistic) square of their four-momentum is their mass: $p^2 = E^2 - \mathbf{p}^2 = m^2$. 
   - Four-momentum is conserved at every vertex. You can draw the four-momentum flow however you want (like electric current), but you have to make sure that that it is conserved everywhere. One consequence of this is that total four-momentum is conserved.
   - Internal lines (lines that begin and end on vertices) do *not* have to be on shell. They are typically **virtual**, so that their energy and momenta are *not* connected by $p^2 = m^2$. 

## The Game Behind the game

Perhaps the bigger question we'd like to answer is this: 

> Where did all of these Feynman Rules (a "theory of particle dynamics") come from?

Are we allowed to just make up anything? We could already see certain patterns in the way that Feynman rules are written. Arrows on electrons, for example, look like they're indicating the flow of electric charge. 

It seems that all of the "physics" of particle physics boils down to figuring out where these Feynman Rules came from. What we call *indexology* is the game-behind-the-Feynman Game. It tells us how to build a particle theory. 

### Anything does *not* go

You may think that we can just make up anything and see what works. It turns out that we are mathematically very constrained with how we build theories of particles. The constraints come from **symmetries** that we expect our theory to respect. This means that particles need to be able to *transform* in certain ways that leave the theory (the vertices) intact. 

In order to keep track of this, we need a way to describe how particles transform. This is a generalization of the conservation of charge in Feynman rules. In fact, for the simplest symmetries, called U(1) symmetries by the cognoscenti, boil down to making sure that all the charge flowing into a vertex sums to zero. For more complicated symmetries, we introduce indices that dictate how particles transform into one another. 

If you want to be fancy, the mathematics behind this is called **group theory** or **representation theory**. In particular, it is the representation theory of *continuous* groups, or Lie (pronounced *lee*) groups. Everything you're doing in quantum mechanics with Pauli matrices, spin, and addition of angular momentum is secretly representation theory.

### Symmetry and Forces

It turns out that there are two kinds of symmetry. Global symmetries are "ordinary" symmetries where you transform everything the same way. Local symmetries, or *gauge symmetries*, are a little more subtle and have to do with redundancies in our mathematical description of a theory. 

As far as we are concerned, both types of symmetries require charges to be conserved/indices to contract in a vertex. However, gauge symmetries have an additional twist that they require a **force particle**. These force particles can also carry charges/indices. In this class, they will always be spin-1. 

### Broken symmetry

It turns out that our universe is not actually very symmetric. However, it's not symmetric in a very particular way: some symmetries are *spontaneously broken*. This is the analog of a ferromagnet: the dynamics of the ferromagnet has no preferred direction and so has a rotational symmetry. However, in its ground state, the ferromagnet has spins that all align and the material is very asymmetric.

In the Standard Model, a phenomenon called *electroweak symmetry breaking* is responsible for (1) giving masses to the other particles in the Standard Model, (2) explaining why certain particles mix quantum mechanically. Like a ferromagnet, this boils down to the Higgs boson having a *vacuum expectation value* that identifies a preferred direction in some vector space.

## U(1) symmetry

U(1) symmetry has to do with "charges" in the sense we're most familiar with. Each particle has some charge under the symmetry. Suppose a particle $\psi$ has charge $q_\psi$. Then we say that the particle transforms under a U(1) symmetry transformation by parameter $\theta$ according to:

$$\psi \to e^{iq_\psi\theta}\psi$$

Anti-particles (or lines with an arrow coming *out* of a vertex) have negative charge:

$\psi^\dagger \to (e^{iq_\psi\theta}\psi)^\dagger = e^{i(-q_\psi)\theta}\psi^\dagger$

We say that a vertex is invariant under U(1) symmetry if all of the charges coming into the vertex sum to zero so that the product of all of the transformations vanishes. 







We first met a global U(1) symmetry when we talked about "muon number" or "electron number" in our theory of QED + $\mu$ + $Z$. The muon has muon number charge +1, the anti-muon has muon number charge -1. Because every vertex in the theory preserved muon number, then any process must preserve net muon number.



### Gauged U(1) Symmetry (QED / Hypercharge)

When U(1) symmetry is gauged, the force particle is a spin-1 field that is not charged under the symmetry. This means that the force particle does not talk to itself. It will, however, talk to *currents* with respect to the U(1) symmetry: these are lines of charged particles coming in and then coming out of a vertex. 

This is how we understood the fundamental QED vertex: the photon talks to any particle with electric charge. It talks to such particles with a very specific vertex: for a given matter particle $f$ with electric charge, you take one line of $f$ with the arrow going into the vertex with the photon, and one line of $f$ with the arrow going *out* of the vertex. 



##SU(2) Symmetry

SU(2) is the first example of a symmetry with indices. Particles that are charged under SU(2) come as two-component vectors called **doublets**. We write them as:









The indices mean that the components of an SU(2) doublet can get "rotated" into one another under.

_Remark_: the mathematical structure of SU(2) symmetry is nearly identical to that of the spinors that you're learning about in quantum mechanics. This is neither a coincidence nor obvious.

### Index contraction

1. If a particle $\psi$ has an upper index, then its anti-particle $\psi^\dagger$ has a lower index:
   $$\psi^i \Rightarrow (\psi^i)^\dagger = (\psi^\dagger)_i$$

2. Upper and lower indices can contract. If you have particles $\psi^i$ and $\chi_j$, then you can *contract* the indices to form an object with no indices:
   $$\psi^i\chi_j \equiv \sum_{i=1}^2 \psi^i\chi_i = (\psi\chi)$$

   Combinations with no SU(2) indices are invariant under SU(2).

   ... you still have to check that the combination is invariant under every other symmetry.

### Swept under the rug

We're sweeping a lot under the rug. In principle there are other types of objects that transform under SU(2). Things that have more than one index, for example. There's also another kind of index that the gauge bosons carry, but we can convert that into the usual upper/lower indices of the doublets. 

### Gauged SU(2): The Weak Force

When SU(2) is gauged, as is the case for the *weak force*, then you have one force particle per rotation axis. It turns out that SU(2) has three different kinds of rotations. This is analogous to how you can rotate in real space with respect to the x, y, or z axis. 

We call the three force particles $W^1, W^2, W^3$. In fact, we can give them indices as follows:

$$\displaystyle (W)^i_{\phantom i j} = \frac{1}{2}\sum_{a=1}^3(\sigma^a)^i_{\phantom i j} W^a$$

This gives a matrix:







We have identified the linear combinations $W^\pm$ for future convenience in anticipation of electroweak symmetry breaking. Yes, these are *the* $W^\pm$ bosons of the Standard Model. 

One tricky point that we won't make too big a deal about: It turns out that there is a way to write down invariants of three and four $W$s. This means that you have vertices with three $W$s and four $W$s coming together. We won't use those too much. It's worth remarking, though, that this implies that the $W$s carry charge under the weak force: the force particles are charged under themselves!

### Forming invariants with the weak force









### Examples in the Standard Model

There are two matter doublets: the quark doublet, $Q^i$ and the lepton doublet, $L^i$. There's also a spin-0 doublet, the Higgs, $H^i$. 

## Spin symmetry

Lorentz symmetry turns out to be really tricky. Spin is the intrinsic angular momentum carried by a particle. What may not be obvious---but is true none-the-less---is that the spin of the particle also determines how it transforms under rotations. 

Let's be very clear: spin is totally weird. It's seems to be about rotations, but rotations act on things like three-vectors. Spin includes slightly more exotic things, like four-vectors, and very exotic things like spinors (two-component complex vectors). This has to do with something called a projective representations and the best explanation I have found is in an advanced quantum field theory textbook (Weinberg, *Quantum Theory of Fields*, Volume I). 

Spin is also represented by an index, though the kind of index depends on the spin of the particle. 

### Spin-0

A particle with no spin carries no angular momentum. It does not transform under Lorentz transformation. 

Notable example: the Higgs boson. 

### Spin-1

These particles carry a $\mu$ index. Fortunately, you know all about this index from kinematics. You can convert between upper and lower indices using the metric. Under a Lorentz transformation, upper indices are rotated/boosted according to $\Lambda^\mu_{\phantom\mu \nu}$. Lower indices are rotated/boosted according to the inverse matrix.

Force particles are spin-1. (Notable exception: the graviton, but that's not part of the theory of the Standard Model.)

### Spin-1/2

Spin-1/2 particles have two components. You can think of these as "spin up" and "spin down," which should  be familiar from quantum mechanics. In fact, there are *two* kinds of spin-1/2 index that *cannot* contract with each other. 

#### Left-handed chirality

These particles have an index $\alpha$ that runs from 1 to 2. 

#### Right-handed chirality

These particles have an index $\dot{\alpha}$ that runs from 1 to 2. This dotted index is a completely different type of alphabet than the undotted index for left-chiral particles. It has nothing to do with time derivative. It's a weird notation; you can blame Bartel Leendert Van Der Waerden. 

#### Antiparticles

The conjugate (anti-particle) of a left-chiral particle is a right-chiral particle, and vice versa. Thus for a left-handed spin-1/2 particle $\psi^\alpha$, the anti-particle has index $(\psi^\dagger)_{\dot\alpha}$. This is kind of weird, it looks like the particle and the anti-particle cannot contract by themselves.

#### Invariant Tensors

The two-component Levi-Civita tensor can raise or lower spin-indices. For example, $\psi_\alpha = \varepsilon_{\alpha\beta}\psi^\beta$. It cannot mix dotted and undotted indices. 

This means that you can take two spinors with the same spin index structure and dot them together: $\psi^\alpha\chi_\alpha$ is invariant. For quantum mechanics afficionados, this is like parapositronium, where two spin 1/2 states combine into a spin-0 state.

You can also construct the analog of orthopositronium: two spin 1/2 states can come together to form a spin-1 state. This uses an invariant tensor that can convert one undotted index, one dotted index, and one spin-1 index into one another. This tensor is a cousin of the Pauli matrices: $(\sigma^\mu)^{\dot\alpha}_{\phantom\alpha \alpha}$. There's also a version with an upper $\alpha$ and a lower $\dot\alpha$, $(\bar\sigma^\mu)^{\alpha}_{\phantom\alpha\dot\alpha}$ Then you can form:

$$\chi_{\dot\alpha}(\sigma^\mu)^{\dot\alpha}_{\phantom\alpha \alpha} \psi^\alpha = (\chi\sigma^\mu\psi)$$

This has one uncontracted spin-1 index, so it transforms as a spin-1 state under Lorentz transformations. This is also something that you can conveniently contract with spin-1 particles: $\chi\sigma^\mu\psi Z_\mu$. 

#### Convention for writing particles

Matter particles are spin-1/2. For convenience, we write all of the Standard Model particles with respect to left-handed chiralities. This means that some of the things that we call "particles" are actually the "anti-particles," like the $\bar e$, $\bar u$, and $\bar d$ particles which had the "wrong" hypercharge. 

From this perspective, the $\bar e$ is a left-handed positron. It's antiparticle is a right-handed electron. Do not confuse this with the left-handed electron $e$ that lives in the lepton doublet $L^i$ or the right-handed positron $e^\dagger$ that is its anti-particle. (I know: I said "do not confused this," but it's *totally* confusing.)

The upshot is that there's a nice mnemonic for the matter particles of the Standard Model: $Q,\bar u, \bar d, L, \bar e$: or "cuddly."

## SU(3)

This is the symmetry of quantum chromodynamics (QCD), the theory of the color force. It is also the basis of "flavor symmetry," which relates the up quark to its heavier siblings (charm, top) and so forth. 

Particles transforming under SU(3) have an index that runs from 1 to 3. That is to say, they come in **triplets**. For quantum chromodynamics, we call these colors: red, blue, green (instead of 1, 2, 3). 

There are eight "rotation axes" for SU(3). This means that QCD has eight gluons. These are roughly "color--anti-color" combinations. 

