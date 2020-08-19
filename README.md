# reader_navigation

Collection of different scripts/notebooks to work on reader navigation.

## Overview in different tools

- data/
  - week_session_with_time_*_sample_*  
  contains samples (0.1%) of the reading sessions to analyze in pandas (and not in spark)
- data in hive (not directly visible)
  - /user/piccardi/week_session_with_time.parquet  
  1 week of reading sessions  
  - /user/piccardi/week_session_with_time_geoloc.parquet  
  1 week of enwiki reading sessions with geolocation
- notebooks/
  - r_preprocess_cut-reading-sessions_save-to-parquet_2020-02-18   
  cut original sessions if interevent activity is larger than threshold
  - r_preprocess_embedding-vectors-to-parquet-save_2020-03-12  
  save article-embedding as parquet dataframe for use in spark

  - r_subsample-reading-session_to-csv_2020-03-02  
  subsample parquet tables of reading sessions to analyze with pandas

  - r_analysis_reading_sessions_condition-topic_len-distribution_2020-02-24  
  basic stats on reading sessions conditioned on topic label (length and distribution)
  - r_analysis_reading-sessions_interevent-time-distribution_2020-02-18  
  histogram of interevent times
  - r_analysis_reading-sessions_interevent-time-distribution_per-country_2020-03-12  
  same as previous but conditioning on different countries of access


  - r_analysis_survey-sessions_make-sessions_2020-03-05  
  get reading sessions from survey data
  - r_analysis_survey-sessions_topic-spread-Xu_2020-03-06.ipynb  
  analyse topic-spread for reading sessions from reader survey conditioned on responses

  - r_analysis_reading-sessions_topic-spread-Xu_running-window_compare-null-models_2020-03-19  
  topic-spread over time with running window (U-shape) and comparison to random walk null models


  - r_random-walks_hyperlinks_get-network-save-as-parquet  
  get network of walks_hyperlinks
  - r_random-walks_hyperlinks_get-network-save-as-csv_2020-03-10  
  get network of hyperlinks but save as parquet
  - r_random-walks_hyperlinks_generate-synthetic-data_2020-03-16  
  perform random walk on network of hyperlinks
  - r_random-walks_clickstream_get-network-save-as-parquet_2020-03-17  
  get network from clickstream data
  - r_random-walks_clickstream_generate-synthetic-data_2020-03-17  
  perform the corresponding random walk

  - r_analysis_reading-sessions_subsample_topic-spread-Xu-explore_2020-03-05  
  some exploratory of reading sessions in topic space (Xu) on subsampled data with Pandas
  - r_analysis_reading-sessions_subsample_topic-spread-Xu-null-models_2020-03-09  
  topical spread and step-size distribution in topic space for smaller subsample and comparison to null models
  - r_analysis_reading-sessions_subsample_random-walk-network_2020-03-09  
  perform random walk on subsample

- output/
  - contains some intermediary output used for downstream calculations.
- plots/
- scripts/
# reader_navigation
