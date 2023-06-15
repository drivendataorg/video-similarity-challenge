[<img src='https://s3.amazonaws.com/drivendata-public-assets/logo-white-blue.png' height='70'>](https://www.drivendata.org/)
<br>
[<img src='https://drivendata-public-assets.s3.amazonaws.com/meta-ai-logo.png' height='70'>](https://ai.facebook.com/)
<br>
<img alt="A side-by-side comparison of two videos showing a frame from a video on the left and the same frame manipulated with emojis on the right." src="https://drivendata-public-assets.s3.amazonaws.com/meta-vsc-hero.png" style="
    object-fit: scale-down;
    max-height: 150px;
    width: 100%;
">
<sub>Credit: [BrentOzar](http://www.flickr.com/videos/56756426@N00/5139755631)</sub>

# Video Similarity Challenge

## Goal of the Competition
Competitors built models to help detect whether a given query video is derived from any of the videos in a large reference set.

The ability to identify and track content on social media platforms, called content tracing, is crucial to the experience of users on these platforms. Previously, Meta AI and DrivenData hosted the [Image Similarity Challenge](https://www.drivendata.org/competitions/80/competition-image-similarity-2-dev/page/378/) in which participants [developed](https://drivendata.co/blog/image-similarity-winners/) state-of-the-art models capable of accurately detecting when an image was derived from a known image. The motivation for detecting copies and manipulations with videos is similar — enforcing copyright protections, identifying misinformation, and removing violent or objectionable content. 

This competition allowed users to test their skills in building a key part of that content tracing system, and in so doing contribute to making social media more trustworthy and safe for the people who use it.

***

There were two tracks to this challenge:

* For the **[Descriptor Track](https://www.drivendata.org/competitions/101/meta-video-similarity-descriptor/)**, the goal was to generate useful vector representations of videos for this video similarity task. Competitors generated descriptors for both query and reference set videos, and a standardized similarity search using pair-wise [inner-product similarity](https://en.wikipedia.org/wiki/Dot_product) was used to generate ranked video match predictions.
* For the **[Matching Track](https://www.drivendata.org/competitions/106/meta-video-similarity-matching/)**, the goal was to create a model that directly detects clips of a query video that correspond to clips in one or more videos in a large corpus of reference videos. 
## Winning Submissions

See below for links to winning submissions' arXiv papers and code.

### Descriptor Track

Place | Team or User | Code	| Paper | Score | Summary of Model
--- | --- | ---  | --- | ---  | ---
1   | do something | [GitHub repository](https://github.com/FeipengMa6/VSC22-Submission) | [A Dual-level Detection Method for Video Copy Detection](https://github.com/FeipengMa6/VSC22-Submission/blob/main/VSC22-Descriptor-Track-1st/documents/VSC22-Descriptor-Track-Solutions.pdf)  | 0.0000 | Uses a model derived from the provided baseline with an edit detection model and a video decomposition model to separate stacked videos.   
2   | FriendshipFirst | [GitHub repository](https://github.com/WangWenhao0716/VSC-DescriptorTrack-Submission) | [Feature-compatible Progressive Learning for Video Copy Detection](https://arxiv.org/abs/2304.10305)  | 0.0000 | Utilizes feature-compatible progressive learning, with a model ensemble that generates comparable (compatible) similarity feature vectors. 
3   | cvl-descriptor | [GitHub repository](https://github.com/line/Meta-AI-Video-Similarity-Challenge-3rd-Place-Solution) | 3rd Place Solution to Meta AI Video Similarity Challenge](https://arxiv.org/abs/2304.11964) | 0.0000 | Leverages previous winning image similarity challenge model with test-time augmentation and edit prediction models to generate descriptors.

### Matching Track

Place | Team or User | Code	| Paper | Score | Summary of Model
--- | --- | --- | --- | --- | ---
1   | do something more | [GitHub repository](https://github.com/FeipengMa6/VSC22-Submission) | [A Similarity Alignment Model for Video Copy Segment Matching](https://github.com/FeipengMa6/VSC22-Submission/blob/main/VSC22-Matching-Track-1st/documents/VSC22-Matching-Track-Solutions.pdf) | 0.0000 | Uses an align-refine pipeline for aligning video copy segments.
2   | CompetitionSecond | [GitHub repository](https://github.com/WangWenhao0716/VSC-MatchingTrack-Submission) | [Feature-compatible Progressive Learning for Video Copy Detection](https://arxiv.org/abs/2304.10305) | 0.0000 | Builds on feature-compatible progressive learning approach and uses a temporal network approach to localize copied segments.
3   | cvl-matching | [GitHub repository](https://github.com/line/Meta-AI-Video-Similarity-Challenge-3rd-Place-Solution) | [3rd Place Solution to Meta AI Video Similarity Challenge](https://arxiv.org/abs/2304.11964) | 0.0000 | Uses descriptor track model with temporal network localization to localize copied segments.