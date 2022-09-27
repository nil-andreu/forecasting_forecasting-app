# Forecasting App
We will make the forecasts of the companies that we need.
For this, we will make periodically requests to obtain financial information of the public companies.

Based on this information, we will run our model to make the predictions that we want to know:
- Amount of predicted sales
- Prediction of public price
- If the price on the next period will increment/decrement

For this, we are also going to obtain metrics on how well our algorithm is working.

In the requirements file, *requirements.txt*, we have all the requirements needed to run this project.
To run also this project in the terminal, we have to define which is the Python Path (this is defined automatically in PyCharm):
```
    export PYTHONPATH="${PYTHONPATH}:/home/nil/Documents/Projects/forecasting-app"
```

## KafKa
Once we have all those predictions, we will publish them on KafKa, so they can be read by the main application made in Golang.

This way, we aim to provide advanced analytics on the public companies.

We have the following files:
    .
    ├── data                            # data science project
    ├── kafka                           # everything related to KafKa
    |   ├── __init__.py
    │   ├── client                      # definitiion of our KafKa client
    |        ├── Dockerfile             # dockerfile to run the consumer client
    |        ├── env.py                 # environmental variables of the configuration of KafKa client
    |        ├── kafka_consumer         # consumer client of KafKa
    |        ├── kafka_producer         # producer client of KafKa
    |        └── utils                  # utilities for the KafKa client
    │   ├── .env                        # environmental variables for the configuration
    │   ├── .env.example                # show which variables are used as environment
    │   └── docker-copmose-kafka.yml    # to run a local cluster of KafKa
    └── ...
