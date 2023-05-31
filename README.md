# yachay.ai_project

datasets: 
grouped_data_w_text_features: this csv file contains the modified dataset with additional time and user_id total tweetcount text features
ungrouped_data: this csv file is an unmodified dataset with cluster_ids

electra_class_grouped: this notebook runs an electra classification model on the modified data 
electra_class_ungrouped: this notebook runs the same electra model but on data that is not modified
electra_reg: this is a modified regression electra model that predicts lat lng coordinates