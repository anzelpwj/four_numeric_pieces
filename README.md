# Four Numeric Pieces

This is my effort to try doing numerical programming in a few different languages as I gain a feel for them.

The four routines are as follows:

- Hertz_Chain:
  Simulating the interaction of a Hertzian chain as described in V. Nesterenko's "Propagation of Nonlinear Compression Pulses in Granular Media" (1983) (link [here](http://link.springer.com/article/10.1007%2FBF00905892?LI=true)). A simple spring-mass ODE system but with nonlinear interactions (0 tensional forces, $F = k x^{3/2}$ compressional forces). Using a Runge-Kutta-4 solver as I've found that to actually work decently well (despite the system being stiff).
- Emperical_Mode_Decomposition:
  A technique based on Norden Huang's extension of the Hilbert Transform (original paper [here](http://rspa.royalsocietypublishing.org/content/454/1971/903)), which serves as an alternative method to wavelets for dealing with non-stationary systems. Naively applying the Hilbert Transform to Intrinsic Mode Functions is still problematic, so we'll follow the techniques listed in "On Instantaneous Frequency" ([link](http://www.worldscientific.com/doi/abs/10.1142/S1793536909000096))
- HL_and_Pn:
  Calculating the Hodges-Lehmann operator ([link](https://projecteuclid.org/euclid.aoms/1177704172)) and Tarr's P_n ([link](http://www.tandfonline.com/doi/abs/10.1080/10485252.2011.621424)). An $O(n \log (n))$ algorithm for calculating these values can be found at [this link](http://epubs.siam.org/doi/abs/10.1137/0207013).
- HOT_SAX:
  Hueristic Ordered Tsearch(?) Symbolic Aggregate Approximation (look, the authors never explained what the HOT stood for...). An $O(n)$ method of discord discovery, following the work of Eamonn Keogh ([link](http://www.cs.ucr.edu/~eamonn/discords/)). Method uses a trie.

Languages:
- Python
- Matlab
- More to come... (working on R)
