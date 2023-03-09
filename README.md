# How to run?
```shell
# create a venv
$ python3 -m venv venv
# activate env
$ source venv/bin/activate
# install package
$ pip3 install PySide6
# run official example
$ python3 rtg.py run autotrader.py

# run customized example trader-1.py
$ python3 rtg.py run trader-1.py
# run customized example trader-2.py
$ python3 rtg.py run trader-2.py
```

# How to implement?
- First, implement a python file like `autotrader.py/trader-1.py`
- Second, create a `json` file with the same prefix name, like `trader-1.json` for `trader-1.py`
- Third, you might need to change `exchange.json` since it will generate `match_events.csv` and `score_borad.csv` if you want to have a different file name such as `match_events_trader1.csv`
    ```json
    "Engine": {
        "MarketDataFile": "data/market_data1.csv",
        "MarketEventInterval": 0.05,
        "MarketOpenDelay": 5.0,
        "MatchEventsFile": "match_events_trader2.csv",
        "ScoreBoardFile": "score_board.csv",
        "Speed": 1.0,
        "TickInterval": 0.25
    },
    ```
