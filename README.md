# Nifty and Bank Nifty Intraday Data for Backtesting

This repository contains intraday data for Nifty and Bank Nifty at a one-minute timeframe, organized by year, month, and day. The data is intended for use in backtesting trading strategies.

## About Unofficed Community

This tool has been developed to cater to the needs of the [Unofficed](https://www.unofficed.com/)  community. Unofficed is a vibrant community of traders, developers, and enthusiasts passionate about financial markets and trading strategies.

Visit the [Unofficed Community Chat](https://www.unofficed.com/chat/) to engage in discussions, share insights, and collaborate with fellow members. Join the community to explore a wealth of knowledge and resources related to trading and financial markets.


## Clone 

Use the git clone command followed by your repository's URL to clone the entire repository, including all files and directories:
git clone https://github.com/aeron7/nifty-banknifty-intraday-data.git

After cloning the repository, you can read the text file using the pandas library in Python. Here's an example of how to do it:

Assuming you've already cloned the repository to a local directory, you can use the following Python code to read the BANKNIFTY.txt file into a Pandas DataFrame:

```python
import pandas as pd

# Specify the path to the cloned repository and the file you want to read
file_path = "path/to/cloned/repository/nifty-banknifty-intraday-data/main/2012/DEC2012/BANKNIFTY.txt"

# Read the file into a Pandas DataFrame
df = pd.read_csv(file_path, header=None, names=["Symbol", "Date", "Time", "Open", "High", "Low", "Close", "Volume", "Open Interest"])

# Display the first few rows of the DataFrame
print(df.head())
```

Replace `path/to/cloned/repository` with the actual path to the directory where you cloned the repository. This code assumes that the data in the text file is in CSV format with the specified column names. Adjust the read_csv parameters as needed based on the actual format of your data.

This code will read the data from BANKNIFTY.txt into a Pandas DataFrame, making it easy to analyze and manipulate the data in Python.

## Folder Structure

The data is organized in the following folder structure:

- **nifty-banknifty-intraday-data/**
  - **Year/**
    - **Month/**
      - **Day/**
        - `Symbol.txt`

Each folder represents a year, and within each year folder, data is further divided into month and day folders. Each day folder contains text files with intraday data for specific stocks or symbols.

For example `nifty-banknifty-intraday-data/2021/FEB/01FEB/01FEB/ACC.txt` contains data in a structure like - 

```
ACC,20210201,09:08,1625.00,1625.00,1625.00,1625.00,1386,0
ACC,20210201,09:16,1626.00,1626.00,1611.20,1616.55,7796,0
ACC,20210201,09:17,1618.20,1618.20,1611.05,1614.60,5360,0
ACC,20210201,09:18,1613.70,1617.85,1612.40,1615.00,6614,0
ACC,20210201,09:19,1615.90,1616.95,1613.65,1614.90,5041,0
ACC,20210201,09:20,1615.15,1616.45,1606.95,1608.90,5505,0
ACC,20210201,09:21,1607.80,1611.45,1603.55,1610.40,5250,0
ACC,20210201,09:22,1611.35,1611.90,1608.75,1609.30,677,0
ACC,20210201,09:23,1609.50,1609.85,1606.10,1608.90,1420,0
ACC,20210201,09:24,1608.65,1614.10,1608.65,1613.10,1612,0
```

## Data Format

The data files follow a specific format, with each line representing an intraday data point:


- `Symbol`: The stock or symbol being tracked.
- `Date`: The date in YYYYMMDD format.
- `Time`: The time in HH:MM format.
- `Open`, `High`, `Low`, `Close`: Price information for that specific time.
- `Volume`: The trading volume at that time.
- `Open Interest`: Open interest data (if available).

## Usage

You can use this intraday data for backtesting your trading strategies. Import the data into your trading analysis tools or platforms to perform historical analysis and test your strategies.

Feel free to explore and utilize the data for your trading research and analysis.

## License

This repository is provided under the MIT License. Please refer to the [LICENSE](LICENSE) file for more details.

Happy trading and backtesting!
