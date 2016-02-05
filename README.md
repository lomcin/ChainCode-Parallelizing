# Concurrent Chain Code Extraction

### OverView 
* A chain code is a way to represent shapes in a binary (black and white) image. 
* The Freeman code encodes a movement as an integer number between 0 and 7. 

#### Scheffler and Greiner Algorithm
![](https://s3.amazonaws.com/f.cl.ly/items/3P3s083s3e1S1Q2V331O/D64DBF97-6256-459A-B26B-F7D3F16D2CC7.png?v=d040714d)

* Scheffler and Greiner Algorithm provides a representation of both the outer contours of a shape and inner holes within a shape. 
* The output of their algorithm is a tree where any path through the tree alternates between outer-shape contours and holes.

#### This project
* Although the Scheffler-Greiener extraction algorithm is efficient,
It would be better to increase performance by parallelizing the algorithm. 
* This algorithm can be broken into small tiles such that the outputs of each tile can be stitched together 
(something like a map-reduce) to generate a solution for the entire image. 

#### How To do
1.Divide the image into some pieces according the rows and cols.
2.Implement the Scheffler and Greiner Algorithm according to the papers. And use that to  parallel get chain-code of each piece. 
3.Develop an approach to merge the chain-code of each piece together. 
4.Test and fixed those two algorithms.
