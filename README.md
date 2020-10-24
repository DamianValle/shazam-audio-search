# Shazam-like Audio Search Algorithm

Shazam allows it's users to query a noisy recording made on their phone and output the name of the song along with other metadata such as artist, album or upcoming concerts.
Queries are converted into a fingerprint which is then compared to the database of over 10 million indexed songs.

This notebook explores the algorithm proposed in [An Industrial-Strength Audio Search Algorithm](https://www.ee.columbia.edu/~dpwe/papers/Wang03-shazam.pdf) by A. Wang. 

We provide a simple python implementation as a proof of concept with explanations and visualizations to help understand the underlying concepts behind the algorithm.

The steps followed are:
* Importing audio files and computing their STFT.
* Locate anchors in the STFT as the most energy sample inside a bin.
* Compute hashes from a set of anchors.
* Build a fingerprint comparator and visualize audio matches.
