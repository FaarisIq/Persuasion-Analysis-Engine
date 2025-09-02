Persuasion Analysis Engine - Faaris Iqbal

**In the output, there is a warning explaining to use Async PRAW 
instead of regular PRAW upon running the engine. 
Ignore this, as it doesn't change the results.**

This engine analyzes persuasiveness in the subreddit r/ChangeMyView by
collecting the top posts and then scoring them based off of different
factors.

Main Features Include:
- Data collection of top 100 posts and their comments using Reddit API
- Analyzing the argument's structure, evidence quality, and persuasive techniques
- Detects deltas awarded (gift awarded to OP when one's view is changed)
- Scores persuasiveness from 0-1 using weights
- Exports clean datasets for further research

The persuasion factors analyzed are:
1. Argument Length/Depth (25% weight) - Detailed vs surface level arguments
2. Evidence quality (20% weight) - Academic sources vs blogs
3. Argument sophistication (20% weight) - Logical structure
4. Delta Awards (15% weight) - Proof of persuasion
5. Comment Engagement (10% weight) - Quality of responses and discussion
6) Emotional appeal (10% weight) - Emotional connection and language used


The persuasive techniques detected are:
- Analogies
- Rhetorical questions and direct questions
- Stats and data
- Personal experience
- Moral/ethical appeals
- Authority citations
- Concessions
- Counterargument acknowledgement
- Logical connectors

It outputs:
- 'cmv_posts_analysis.csv' - Main post data with all metrics
- 'cmv_comments_analysis.csv' - Individual comment analysis
- 'cmv_summary_stats.csv' - Aggregated statistics
- Summary stats of most/least persuasive posts

To use it:
You run the script and it automatically collects data and generates CSV files
You can also adjust the limit parameter in collect_cmv_data() and in the main
function at the bottom in order to change the amount of posts being analyzed
