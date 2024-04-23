This repository contains the relevant code for my final year project, as part of my MEng degree in Computer Science at UCL. The project is titled 'Influenza-Like-Illness Rate Surveillance Using Web Search Queries'.

The repository is split into 2 folders:

- Notebooks: Contains the data preprocessing, data analysis, and model training for the various models trained in both the nowcasting and forecasting tasks.
- Results: Contains the corresponding performance results of each model trained in both the nowcasting and forecasting tasks.

NOTE: Due to privacy concerns, the data used for this project is not available in the repository and so the source code cannot be run. All results, graphs and notebook outputs that reveal any information regarding the data have been omitted.

Below is the abstract of my dissertation, providing greater context on what this project was about.

'In the field of epidemiological surveillance, the use of user-generated content has become increasingly prevalent in the early detection and estimation of infectious diseases, such as Influenza. Specifically, prior research has demonstrated the effectiveness of utilizing online web search queries for both nowcasting and forecasting Influenza-Like Illness (ILI) rates in different geographical locations. Google Flu Trends represents the first real-time Influenza surveillance system utilizing such methodologies. Subsequent studies have built upon their efforts, suggesting improvements in experimental design and models for the prediction tasks.

In our study, we build on this existing work through exploring the predictive capabilities of deep learning models, addressing the task of nowcasting and forecasting ILI rates in England using online web search queries. We evaluate the predictive performance of our models over five consecutive flu seasons from 2014-15 to 2018-19, using the Mean Absolute Error (MAE), Mean Absolute Percentage Error (MAPE), and Bivariate Correlation (\textit{r}).

Initially, we conduct a replication study of a proposed baseline Elastic Net model \cite{Lampos3}, in conjunction with exploring various feature selection methods for the nowcasting task. This encompasses a correlation-based approach, directly measuring data correlations between queries and ILI rates; using sentence embeddings to capture the textual semantics of the queries; and a hybrid method combining the two. Building upon these preliminary models and retaining the optimal hybrid features, we present a novel, minimal Feed Forward Neural Network (MFFNN) model that surpasses the Elastic Net in the predictive performance with an improvement of 10.56% in MAE, 13.86% in MAPE, and 2.1% in Bivariate Correlation. This effectively introduces a new baseline model for the nowcasting task.

This is then further succeeded by an exploration of deeper neural network architectures, including the incorporation of historical lagged features. Specifically, we propose a deeper FFNN (DFFNN) model, incorporating 14 historical lagged features, that achieves a highly competitive nowcasting performance of 1.25 MAE, 22.36% lower than our newly introduced baseline (MFFNN) and surpassing performances of more traditional machine learning methods, reported in similar studies \cite{Lampos3, Lampos4}.

Continuing our analysis, we apply our neural network models in the forecasting task, at different horizons ($\gamma$), predicting ILI rates for $7, 14, 21,$ and $28$ days ahead. We observe that our DFFNN nowcasting architecture consistently demonstrates strong and competitive forecasting performance across flu seasons. It notably outperforms both our MFFNN and a baseline persistence model, particularly for longer forecasting horizons. These results once again surpass forecasting performances reported in similar studies \cite{Morris1}, which employ more intricate neural network architectures, albeit on three flu season compared to our five.

These findings not only underscore the competitive performance achieved by our DFFNN model, outperforming our linear baseline in both nowcasting and forecasting tasks, but also establish a benchmark against which more complex deep neural network architectures can be compared against, validating their performance and necessity over our simpler architectures.'
