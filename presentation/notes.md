# BioMath Presentation - Population Genetics

## Introduction

* Hello class, my name is Nathan Laundry and today I'll be guiding
  you through a cursory look at Population and Evolutionary genetics
  and how we can represent them with discrete time systems. 
* we'll be exploring the following topics today:
    1. The goals of population genetics and why one would study it
    2. The Hardy-Weinberg law, it's assumptions and equations
    3. Examples of systems where key assumptions are violated
       and how these violations produce more interesting systems to analyze.
* Just prior to delving into these topics, I'll do a brief summary of some
  key defintions.
* My goal here will not be to do deep analysis as I am not an expert in the field,
  but instead will be to impart upon you an intuition
  about how these laws, and the violation of their fundamental assumptions
  create rich systems which can be analyzed to produce predictions.

## Key Definitions

* Gene:  A hereditary unit consisting of a sequence of DNA 
        that occupies a specific location on a chromosome
* Chromosome: A molecule that houses the genetic material of an organism
* Allele: a variant form of a given gene
* Locus: fixed position on a chromosome where a gene is located
* Genotype: We will use this to refer to the combination of alleles at one locus
* Homozygous: identical pair of alleles at one locus
    * Dominant: two capital As
    * Recessive: two lower case as
* Heterozygous: oppposing pair of alleles at one locus

## Goals of Population Genetics

* Describe frequency of an allele in a population
* Make predictions about allelic frequency as a population evolves
* Analyze factors leading to changes in allele frequency

* This allows us to predict how a species in an environmment evolves
  Which characteristics and properties become dominant, and which ones
  fade away.
* Characterize a population based on it's genetics.
* allowing us to differentiate mulitple populations of the same species.

## Hardy-Weinberg - Genotypic frequencies

* The Hardy-Weingberg law predicts how gene frequencies will be 
  transmitted from generation to geqtneration (given some assumptions)
  TODO: CITE THIS
  * One key assumption is that there is no overlap in generations
    making it perfect for discrete time systems

* For Hardy-Weinberg we assume the following:
    * An infinitely large population (this eliminates genetic drift)
    * Random mating 
    * No evolutionary forces - these would be:
        * Mutation - the random changing of genetic structure 
            (could introduce a new allele) 
        * Migration - Populations moving or new populations being introduced 
            (diversifying the gene pool)
        * Selection - One allele being more successful at reproducing
            (creates bias towards one allele over another)

* The reason we make these assumptions is to force an equilibrium
* I'll demonstrate this with an example and the famous Hardy-Weinberg equation

### Hardy-Weinberg Equation

* let p equal the frequency of allele A
* let q equal the frequency of allele a

* We can then predict the frequencies of both A and a in the next generation given
  this simple table.
![](Hardy-Weinberg-Table.png)

* This table can be further distilled into our first major equation,
  one that ties it back to the discrete time equations we explored in 
  the first half of the course.

* p^2 +2pq + q^2 = 1 (Genotypic frequencies of all zygotes sum to 1)
* More importantly for our inquiry since we'll be looking at allelic frequency
  are the following:
    * pt+1 = p^2 + pq = p( p + q ) = p
    * qt+1 = q^ + pq = q( q + p ) = q

* Evidently we've found an equilibrium
* Meaning, whenever we have the assumptions we discussed earlier satisfied
  there should be no change in allelic frequency from generation to generation.
* This is an important thing to note, but not a particularly interesting system.

### Hardy-Weinberg with selection

* To explore some systems with more depth, we'll begin by violating one assumption.
* This will push our system away from equilibrium and give us new and intriguing
  factors to consider.
* The system we will consider is that of the peppered moth in England.
* Specifically we will analyze at a time during which it's environment was rapidly changing
  pushing selection as an evolutionary force to the foreground.
* Thus our violation is that we have evolutionary forces acting on the population.

* In England, prior to the start of the industrial revolution the white allele was extremely
  dominant amongst peppered moths. The alternative being the much less common dark grey or
  black allele.
* The dominance of this allele was likely due to ubiquity of birch trees in the environment,
  making moths with a white appearance camouflage with their surroundings.
* This is key to altering our system.
* Because the genotype that results in fairer wings, was more able to evade predators it is
  considered more fit - that is more likely to reproduce and pass on it's genetics.
* During the industrial revolution however, birch trees would become covered in soot/pollution.
* This darkening of the environment made it so dark coloured moths became camouflaged and thusly
  more fit.
* Within just 50 years the dominant allele for peppered moths in England was dark allele.

* So then, how do we adjust our model to take into account fitness?
* Earlier, with our assumptions in tact we saw that allelic frequencies don't change over time
* But with selection as an evolutionary pressure we can see great change happen rapidly.
* How can we make effective predictions when our assumptions are violated?

* As we discussed earlier, fitness can be reduced to two major components:
    1. Probability of surviving.
    2. and fecundity - or ability to reproduce.
* We can then introduce these variables as weights into our initial equations.
* In this specific example, we will assume there is no change to fecundity based on the
  the allele related to colour, and thus we can simplify to one new weight factor for
  survivability.
* We will refer to this weight as W and a subscript for their respective genotype

* We then arrive at the altered equations for pt+1 and qt+1. They are as follows:
    * pt+1 = (wAA p2 + wAa pq)/(wAA p2 + wAa 2pq + waa q2)
    * qt+1 = (waa q2 + wAa pq)/(wAA p2 + wAa 2pq + waa q2)
* so we see the application of the fitness factor for the homogeneous A genotype applied to p2
* the heterozygous fitness factor applied to pq - the frequency of A and a
    * This is to include the number of A alleles in heterozygous group
* The same is then performed for q, the frequency of a alleles in the next generation.
* So essentially what we've done is modify our original equations to favour more fit genotypes
* By favouring these more fit genotypes, we skew the equations such that at the next generation
  we see a greater frequency for the successful or fit allele.
* This is one of the backbones of population genetics. 
* How fitness affects traits in populations over time.

* Returning to our example - the peppered moth - we can deduce that the fitness of the white
  allele prior to the industrial revolution must have been vastly greater than that of the dark
  allele. This is made evident by the incredible dominance of it in the population - nearly 99%.
* Assuming AA and Aa are the genotypes resulting in dark coloured moths
* This would be reflected in our system with a vastly greater weight factor for the AA genotype
  than the aa genotype.
* To perform some qualitative analysis based on our discrete time system
* The incredibly rapid change in allelic frequency 
    * (50 years on an evolutionary scale is barely the blink of an eye)
    * indicates to us that the fitness of moth's with the dark allele must have vastly surpassed
      that of the moth's with the light allele.
* To continue our qualitative analysis we can infer 
  that the ability to evade predators in the peppered moth's environment must have been 
  absolutely paramount to survival.
* More than fecundity, or other survival tactics camouflage had the most immediate and powerful
  impact on fitness of this population.

### Hardy-Weinberg with selection continued

* Furthermore we can explore a fitness that is composed of fecundity and survivability.
* For example, if we have a hypothetical species of moths that is more likely to survive 
  based on having neutral colours - lets say grey - similar to the peppered moth.
* But is more likely to reproduce by attracting a mate with vibrant colours we've created
  a more interesting system again.

* This time we may split the fitness weight into two components
    * s - for survivability
    * f - for fecundity
* We also introduce two new variables:
    * D - population of predators
    * M - population of available mates
* This modifies our fitness weight
    * Wii = (Sii * D + Fii / M ) 

* With this system there would see more fluctiation
* in an environment where predators are scarce it is likely that vibrant colours
  would become dominant, and the contribution to fitness that survivability generates
  would become negligible.
* in contrast, an environment where predators are plentiful, neutral colours would become
  dominant, as a creature that doesn't survive has no chance of passing on it's genes.
* As you can see, by violating just one assumption we've created a much more complex system.
* In practice, these assumptions very rarely hold, and the complexity of allelic frequency
  equations increase dramatically.

## Conclusion

* So to recap, today we've covered:
    * The goals of population genetics
        essentially determining patterns in genotypic frequency in populations.
    * The Hardy-Weinberg law
        * how genes will be passed on from generation to generation
        * The Hardy-Weinberg equation and it's respective equilibrium
    * An example of how selection and fitness can add complexity to Hardy-Weinberg
    * And an example of how further commplexity can be introduced as more assumptions are violated
* Thank you for your time and I hope you learned something interesting. Cheers.

## Citation

Steward, R. C. (1977). "Industrial and non-industrial melanism in the peppered moth Biston betularia (L.)". Ecological Entomology. 2 (3): 231–243. doi:10.1111/j.1365-2311.1977.tb00886.x.
Sheehy. (n.d.). RABLE Links for Web PopGen Lab. Retrieved from https://www.radford.edu/~rsheehy/Gen_flash/ABLE_Workshop/Popgen_Equations.pdf
Introduction to Population and Evolutionary Genetics. (n.d.). Retrieved from https://www.ndsu.edu/pubweb/~mcclean/plsc431/overheads/popgen/popgen13.htm
INTRODUCTION TO POPULATION GENETICS. (n.d.). Retrieved from https://biomed.brown.edu/Courses/BIO48/6.PopGen1.HW.drift.HTML
