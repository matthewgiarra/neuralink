# neuralink
Codes for working on the Neuralink compression challenge (https://content.neuralink.com/compression-challenge/README.html)

# Approach
Compressing a signal requires the existence of a basis in which its representation is sparse, or mostly sparse, compared to its dimensionality in the uncompressed basis. For lossless compression, the total energy of the signal must be contained in a finite number of dimensions in this *compression basis,* from which the signal can be reconstructed with no loss of information. For lossy compression, *most* of the signal's energy must be restricted to a few components in the compression basis, so that the less energetic components can be thrown away (set to zero) without sacrificing the information required for the target application.

The achievable lossless compression of a signal is therefore governed by the ratio of the number of nonzero elements in its compression basis representation to the number of elements in its original representation. Similarly, lossy compressibility is determined by the number of elements in the compressed representation that must be preserved to acceptably reconstruct the original signal. 

Some signals, like natural images and audio recordings, are amenable to compression because they are known to be mostly sparse in certain bases (e.g., Fourier or wavelet bases). 

However, not all types of signals have obvious compression bases, and it is often not known whether they are sparse in any particular basis. Neural activity recordings apparently fall into this category. Because the compression basis must be known at compression time, these signals are not straightforward to compress efficiently, and standard algorithms often fail to achieve high compression ratios.

The problem of efficiently compressing neural signals therefore boils down to finding a basis in which they are sparse or mostly sparse, presuming one exists.

Our approach adapts conventional and learning-based approaches to find candidate compression bases, and compares bases according to peak signal-to-noise ratio (PSNR) and compression ratio (CR) achieved on the [Neuralink compression challenge dataset](https://content.neuralink.com/compression-challenge/README.html).

Stay tuned for results. 