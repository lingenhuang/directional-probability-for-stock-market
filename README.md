# Stock market forcasting using deep learning

The summer project that uses deep learning to predict the next time slot's price goes up or down.

#### Folder
    -autoregressive_model
        -timegpt.ipynb: using timegpt tutorial.
        -transformer88.ipynb: transformer to predict 60 steps ahead of exact price, still need some solve on normalization.
        -transformer89.ipynb: transformer to predict exact price, still need some solve on normalization.
        -transformer_mse_0step_model: model for the 0 step transformer.
        -transformer_mse_10step_model: model for the 10 step transformer


    -data_preprocessing
        -labeling_data.ipynb: how to label the data and visualize it.
        -stock_price_fetch,ipynb: fetch stock price using yfinance/alpha vantage.
        -vix_chart.ipynb: used for testing data sampling, draw chart of the vix and categorize the high, mid, low vix.

    -ES_data
        E-mini S&P 500 Index Futures data from 2021 to 2022

    -LSTM
        -LSTM.ipynb: LSTM model that implement the directional probability of the SPY 5 min candle.
        -test_indices.npy: The testing data indices for the experience.
        -with_mask
            -LSTM models of training data with masks.
            -best or last means the training process saves the best test loss model and the last epoch's model.
            -20 to 60 is the sequence length, 
            -x10 means the difference times 10, 
            -minmax or standard means the different normalization method, 
            -5 features means including the 5th feature of volumns.
        -without_mask
            -LSTM models of training data without masks.
            -best or last means the training process saves the best test loss model and the last epoch's model.
            -20 to 60 is the sequence length, 
            -x10 means the difference times 10.
    
    -spy_data
        SPY 5 min data from 2008 to 2024

    -spy_data_1min
        spy_1 min data from 2014 to 2024

    -transformer
        -test_indices.npy: The testing data indices for the experience.
        -ensemble.ipynb: use ensemble method from differnet sequence's probability to predict the direction.
        -transformer_spy_mse: transformer model with the MSE for autoregressive model.
        -transformer_spy.ipynb: Transformer model that implement the directional probability of the SPY 5 min candle.
        -18-21_transformer
        2018 to 2021 for training
            -with_mask
                -Transfomer models of training data with masks.
                -best or last means the training process saves the best test loss model and the last epoch's model.
                -20 to 60 is the sequence length, 
            -without_mask
                -Transfomer models of training data without masks and with positional encoding.
                -best or last means the training process saves the best test loss model and the last epoch's model.
                -20 to 60 is the sequence length,
        20-21_transformer
        2020 to 2021 for traing
            -with_mask
                -Transfomer models of training data with masks.
                -best or last means the training process saves the best test loss model and the last epoch's model.
                -20 to 60 is the sequence length, 
                -flatten_2layers means different model design for transformer.
            -without_mask
                -Transfomer models of training data without masks and with positional encoding.
                -best or last means the training process saves the best test loss model and the last epoch's model.
                -20 to 60 is the sequence length,

            -mse
                MSE model of transformer

More details can refer to the slides.
            
            

                



