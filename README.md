# Avellaneda-Stoikov-Model

I recreate the result of the paper 'High-frequency trading in a limite order book' here.

I uploaded three pdfs in the repository, they the 1st editon of the paper, the 2nd edition of the paper and a PPT with detailed mathematical proof of the model.
Note that all three pdfs have some mathematical errors during the proof, I recommend the PPT because it's the most detailed and only lost a denominator of 2 in the middle of equation (21) and (22)

In the paper, the authors compared two strategies: inventory strategy and symmetric strategy. The authors said that the symmetric strategy used the same spread as the inventory strategy, but centers it around the mid-price rather than the reservation price
However, in the table the spreads are all fixed and they are equal to the second part of the spread equation
So I code two ways: both inventory and symmetric strategy's spread are dynamic but they centered around reservation price and mid-price respectivelly, the other way is that inventory strategy's spread is dynamic but symmetric strategy's spread is fixed (which only depends on gamma and k)
Throught the result, we can see that the result of fixed spread is more similar to the result in the paper.

Future research: How will latency affect the model? current model assumes no latency, the price/inventory we get is the current value and our order will be sent immediately to the exchange.
