# Approximate-Nearest-Neighbor-Search

The following techniques are implemented for searching the nearest neighbors in the Python Notebook
 - Exhaustive search
 
     Comparing each point to every other point, which will require Linear query time (the size of the dataset).

     The only available method for guaranteed retrieval of the exact nearest neighbor is exhaustive search (due to the curse of dimensionality.)
     
 - Locality Sensitive Hashing
     
     LSH refers to a family of functions (known as LSH families) to hash data points into buckets so that data points near each other are located in the same buckets with high        probability, while data points far from each other are likely to be in different buckets.

     This makes it easier to identify observations with various degrees of similarity.

     LSH has many applications, including:

     - Near-duplicate detection:
     
       LSH is commonly used to deduplicate large quantities of documents, webpages, and other files.

     - Genome-wide association study:
     
       Biologists often use LSH to identify similar gene expressions in genome databases.

     - Large-scale image search:

       Google used LSH along with PageRank to build their image search technology VisualRank.

     - Audio/video fingerprinting:

       In multimedia technologies, LSH is widely used as a fingerprinting technique A/V data.
 - Product Quantization
 
      - Product quantization is an effective vector quantization approach to compactly encode high-dimensional vectors for fast approximate nearest neighbor (ANN) search.

      -  The essence of product quantization is to decompose the original high-dimensional space into the Cartesian product of a finite number of low-dimensional subspaces that          are then quantized separately.

      - Optimal space decomposition is important for the performance of ANN search, but still remains unaddressed. In this paper, we optimize product quantization by minimizing          quantization distortions w.r.t. the space decomposition and the quantization codebooks.
 - Trees and Graphs
      - Tree-based algorithms are one of the most common strategies when it comes to ANN. They construct forests (collection of trees) as their data structure by splitting the dataset into subsets.

      - One of the most prominent solutions out there is Annoy, which uses trees (more accurately forests) to enable Spotify’ music recommendations.

      - In Annoy, in order to construct the index we create a forest (aka many trees) Each tree is constructed in the following way, we pick two points at random and split the space into two by their hyperplane, we keep splitting into the subspaces recursively until the points associated with a node is small enough.
 - HNSW
      - An HNSW index consists of navigable small world graphs in a hierarchy. Each document in the index is represented by a single graph node. 
      - Each node has an array of levels, from level 0 to n. The number of levels is constant during the lifetime of the node and is drawn randomly when the node is created. All nodes have at least level 0. 
      - At each level there is a link array which contains the document ids of the nodes it is connected to at that level.

## Dataset Used
  Stack Exchange dataset is used and the questions similar to a given question is searched and the question titles are printed for each method.

  The following datasets from the StackExchange network are available:

  CrossValidated: From stats.stackexchange.com. Approximately 9000 users, 72000 questions, and 70000 answers.
  StackOverflow: From stackoverflow.stackexchange.com. Approximately 1.3M users, 11M questions, and 18M answers.
  
  I have used the CrossValidated Dataset for analysis here.
  
  
Refer the Notebook (.ipynb file) in the repository for detailed Implementation and Visualization.   
