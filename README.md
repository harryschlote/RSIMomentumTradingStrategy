# RSIMomentumTradingStrategy

Relative Strength Index measures the speed and magnitude of a security's recent price changes to evaluate overvalued or undervalued conditions. It is given by:
  $$\text{RSI} = 1 - \frac{1}{\left(1+\text{abs}\left(\frac{\text{average of previous gains}}{\text{average of previous losses}}\right)\right)}$$

The value of the RSI ranges from 0 to 1.

If the value os the RSI is close to 0, then this indicates that the aset is underpriced. If it is close to 1 then it is overpriced.

The boundary values are 0.3 and 0.7 for low and high respectively.

The algorithm will:
- Calculate RSI at each date
- If RSI is less than 0.3 enter long position
- If RSI greater than 0.7 then enter long position
- If RSI is inbetween then keep the same position as before

The weighting function w(x) will simply be an algebraic function of the RSI value. The function maps as follows:

$\text{w}\left([0,1]\right)\rightarrow [-1,1]$ with $\text{w}(0) > 0,\text{w}(1) < 0$.
