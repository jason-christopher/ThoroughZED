![](https://cdn.discordapp.com/attachments/1064590416575483936/1065768313617121341/10ItB7Xx2_Ctl_76P0qTxSt331y-2Z5avZYtoeVBzRdkxG9ikiw.png)  
*Image credit: zed.run*

# ThoroughZED

Never overpay for a [ZED RUN](https://zed.run/) digital racehorse again.

## Our Team

- [Harper Foley](https://github.com/hfoley2013)
- [Jason Christopher](https://github.com/jason-christopher)
- [Oliver Speir](https://github.com/OliverSpeir)
- [Dennis Nichols](https://github.com/dennis-nichols)

## Mission Statement

To empower ZED Run gamers to make informed financial decisions and maximize their returns in the marketplace.

## What is ZED RUN?

ZED RUN launched in January 2019 as one of the first Non-Fungible Token (NFT) projects that enabled users to become stable owners who could buy, breed and race their very own digital racehorses through an Ethereum-based platform ([ZED RUN](https://zed.run/)). 

## Application Features

- Intrinsic value estimation of horses based on their previous race performances.
- Horse sale price estimation (ZEDstimate) using a machine learning model trained on ZED RUN market data.
- Provision of a data dashboard of individual horse race statistics along with broader market trends.

## Use Cases

- Find undervalued horses on the market and paying for horses that are unlikely to make a return.
- Compare your horse's performance to that of other similar horses on the market.
- Estimate a fair asking price when you choose to sell horses from your stable.

## Set-up

1. Clone the repository from [GitHub](https://github.com/jason-christopher/ThoroughZED) to your local machine.
2. From the command line inside the cloned folder, create a virtual environment by running: `python3.11 -m venv .venv` (or the desired version of Python).
3. Activate the virtual environment by running: `source .venv/bin/activate`
4. Install the requirements needed to run the app by running: `pip install -r requirements.txt`
5. You must train the machine learning regression model before the first use:
   * This can be done by running: `python -m app.model_predict`
   * It may take up to a minute to run this file, but this only needs to be accomplished once.
   * This will create the `rfr_model.pkl` file that needs to be moved to the `app` folder
   * Now you won't have to train your regression model each time the app is run!

## Using ThoroughZED

1. Launch the app from your command line by running: `python -m app.thoroughzed_cli`
2. You will be asked to enter a ***Horse/NFT ID***. This input only accepts integers.
   * The app will tell you if that particular horse has not been raced, if it isn't a valid horse on the ZED RUN platform, or if your input was invalid.
3. If the horse is a valid horse on the ZED RUN platform and has race statistics associated with it, you will have the option to get the ***intrinsic value*** by typing `i`, the ***relative value*** (ZEDstimate) by typing `r`, or displaying the ***dashboard*** by typing `d`.
   * Both the intrinsic value and relative value (ZEDstimate) can be found on the dashboard, so we recommend typing `d`.
4. If `i` is selected, you will be prompted to enter the listing price of the horse you're interested in buying. This value should be in USD and does not require a `$` sign (only input an integer).
5. If `d` is selected, an online will dashboard will load after a few seconds in a browser window. 
   * To exit the dashboard, type `CTRL + C` in the command line.
6. A help menu can be accessed by typing 'h' if you need more information on intrinsic and relative value.
7. You may quit the app by typing `q`.

### Disclaimer

***This model is a decision-making tool to assist in the evaluation of a given listing price or a bid you expect to put on a horse. It is to be used to gauge the feasibility of making your money back on your investment given the price of the horse; however, this does not constitute financial advice nor guarantee the performance of the horse.***
