# Monte-Carlo-Simulations

Monte Carlo Simulation using Historical Data to Predict Portfolio Returns over a Given Period of time. 

#The Model 
This model uses Monte Carlo Simulations (basically, running a large number of "random walks") to predict portfolio returns. Our Monte Carlo model assumes the distribution of daily returns of a portfolio to be a MultiVariate Normal Distribution. Hence, with historical data, we can calculate covariance of each stock with respect to one another and thereby create such a multivariate distribution. This enables us to perform a random walk through our distribution i.e picking daily stock price movements on the basis of their relative probability and run simulations accordingly

The mechanism through which this is accomplished is slightly more complex but boils down to performing something called a Cholesky Decomposition on our Covariance Matrix which gives us a Lower Triangular Matrix that then enables us to extract probabilities from our MultiVariate Distribution.

#VaR and CVaR

Value at Risk (VaR) and Conditional Value at Risk (CVaR) are two metrics commonly used in the world of risk management. Our model additionally calculates these. VaR basically tells us, upto a certain confidence level (usually 95%), what is the maximum money we could expect to lose i.e our maximum possible risk.

CVaR, also known as the expected shortfall, then tells us how much money we might expect to lose given a very extreme situation, a situation beyond our wildest nightmares. Beyond our wildest nightmares is just fancy talk for a situation beyond our previously mentioned confidence level.

#Input 

We'll be using a list of 15 stocks for the simulations. We'll be using the historical data for past five years and our forecast period will be the next five years. for the time being we'll be conducting 1000 simulations on the list of stocks. The input is same as shown below:
<img width="933" alt="image" src="https://user-images.githubusercontent.com/99968604/180613970-e5256800-17a1-4755-9e70-c2541327d57a.png">

#Output 
The output predictions are as follows:

<img width="426" alt="image" src="https://user-images.githubusercontent.com/99968604/180614080-787665a4-8841-4045-a718-caa9a05cb185.png">
