# Sharp-PC1211-RE
Reverse Engineering of the SC43153/177/178 uProcessors

The SC43153 (seen in the early EL-5150 Programmable Calculators), and SC43177/178 (seen in the Sharp PC-1211 Pocket Basic Computers, also known as TRS-80 PC-1 in the US) are total mysteries. 

Those chips, most certainly designed & fabricated before the year 1979, belong to a particular variant of one of Sharp's early 4-bit microprocessor architectures. Unfortunetaly today there's absolutely zero information about them can be found on the internet, no ISA info, not a single piece of assembly.

Today, most of Sharp's pocket computer products are immortalized in the form of software emulators, enabled by the PEEK & POKE commands provided by the basic interpreter and the trememdous effort from the Pokecom community around the world. However, this particular model PC-1211 is the only one that doesn't offer this functionality and thus becomes the only one un-dumped. I'm personally a fan of the formfactor, so I became determined to dump it at all costs.

## Difficulties

Those processors seems to have a special kind of ROM where the information is stored in the doping regions. It makes it impossible to see the bits directly from optical analysis.

There're some potential solutions, one is to exploit the difference in oxidation speed of doped regions to create optical interference, this technique is explained quite well in the [REcon 2015 presentation by Mike Ryan, John McMasterm and marshallh](https://recon.cx/2015/slides/recon2015-19-mike-ryan-john-mcmaster-marshallh-Reversing-the-Nintendo-64-CIC.pdf)
 I've got to try this out ! but before that, I need to buy more PC-1211 to practice this technique until I get desireable results.

Another thing I have in mind is: To ensure correctness, there has to be a hidden "debug mode" in the processor to dump out its ROM content. This is also a way to get the ROM of the CIC chip by the Nintendo hacking community. It's described in great detail in this [technical report by Sergei P. Skorobogatov](https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-630.pdf)

