# Optimized AlphaColorToScanline/ScanlineToAlphaColor

While developing a small game using Delphi 10.2 (Tokyo), I experienced several performance bottlenecks.

One of the biggest was the default implementation of the color-space conversion functions "AlphaColorToScanline" and "ScanlineToAlphaColor".  I have no idea why, but the original implementation called (depending on the color-space) multiple functions per-pixel.

To speed things up, I reduced the number of function calls for the two most widely used color-spaces, RGBA for Android and BGRA for Windows.

This resulted in a significant speed-up, enjoy.
