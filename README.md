# YouTube Networks

Testing some approaches for building YouTube channel networks.

## Japanese Conspirarcy Channel Network

This network is based on YouTube video recommendation. Starting with a specific channel ("Naokiman Show") we collected the first 20 recommended videos (right side on the frontend) of the latest 30 videos. We removed all videos tagged as "Recommended for you", as they are based on user information and not their relation to the video. This process was repeated three times in order to get a larger array of recommended videos. Each channel in the pool of recommended videos was then also used as the starting point for another round of data collection.

From this dataset we built a network file, where the nodes represent the channels and the edges their closeness based on video recommendations. We then filtered out all channels which were only linked to once, in order to make the final network visualization more readable. The node size represents the number of incoming links from other channels, the size of the edges the number of videos  number of video recommendation from one channel to another.

[Visualization of the results](gexf-viewer/)

The results are rendered here using the [GEXF Viewer](https://github.com/raphv/gexf-js).