1.First, our imports/globals and includes/defines



2.Then we are importing the video:
	

3.Then creating necessary empty matrices to store image frames
	

4.Converting each image into three different planes(RGB)
 		
5.Now we start configuring the histograms. Since we are working with the R, G and B planes, we know that our values will range in the interval [0,255]

int histSize = 256;

		
6.Calculating Histograms
The arguments represent:

&bgr_planes[0]: The source array(s)
1 : The number of source arrays (in this case we are using 1. We can enter here also a list of arrays )
0 : The channel (dim) to be measured. In this case it is just the intensity (each array is single-channel) so we just write 0.
Mat() : A mask to be used on the source array ( zeros indicating pixels to be ignored ). If not defined it is not used
b_hist : The Mat object where the histogram will be stored
1 : The histogram dimensionality.
histSize: The number of bins per each used dimension
histRange: The range of values to be measured per each dimension
uniform and accumulate : The bin sizes are the same and the histogram is cleared at the beginning.

7.Displaying created histograms:

	8. Normalizing Histograms		

		
9.Shows the variation of pixels :

10.Displaying imported video with a delay of 15 milliseconds between each frames:

