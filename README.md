# Weather_LSTM_overlapping_sequences

How to do training, validating, and testing on weather dataset?

1. Download the dataset at https://paperswithcode.com/dataset/weather-ltsf or https://drive.google.com/file/d/1Tc7GeVN7DLEl-RAs-JVwG9yFMf--S8dy/view?usp=share_link

2. In the weather dataset, there are date column and 21 feature columns.

3. The data are of 10 second intervals from 1/1/2020 0:10 to 1/1/2021 0:00 with 52696 rows of data.

4. I split the dataset into train : validate : test ratio of 8 : 1 : 1.

5. The input sequence length is 5.

6. The output target sequence length is 1.

If input_len = 5 and output_len = 1, and your data is like:

data = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

Then, the first input-output pair will be:

X[0] = [0, 1, 2, 3, 4]

y[0] = [5]

Next:

X[1] = [1, 2, 3, 4, 5]

y[1] = [6]

And so on.
