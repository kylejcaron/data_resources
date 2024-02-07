
# Resources List

--

This is an ongoing list of resources I've found helpful. Hopefully I'll organize it more later

# Censored Demand Forecasting

Favorite Resources
 * [Zalando - Deep Learning Based Forecasting](https://arxiv.org/pdf/2305.14406.pdf)
   * They use Multinomial imputation based on other SKUs. Didn't quite work for the dataset I had access to due to extreme censoring.
 * [Zalando's double ML pricing paper](https://arxiv.org/pdf/2312.15282.pdf)
   * Discusses how to account for and model pricing in an unbiased way for demand models   
 * https://github.com/FlorianWilhelm/bhm-at-scale
   *   Implements a hierarchical forecaster at scale and offers one approach of accounting for censoring
 * [Modern forecasting in practice course](https://maven.com/tim-januschowski/modern-forecasting)
    * Great course in general about forecasting. They discuss just not contributing to the log likelihood as a simple approach for accounting for stockouts, or imputing based on other SKUs
 *  [Logit choice model](https://khakieconomics.github.io/2019/03/17/The-logit-choice-model.html)
    *  Shows how to use discrete choice modeling in a way that could work for censored demand - basically adjusting the choice set and modeling utilities
 * [Discrete Choice Models with Simulation](https://eml.berkeley.edu/books/choice2.html)
   * Provides a really nice framework for how to think about stockout substitution, product utilities, and cross-product effects
 * [The poisson trick](https://stats.stackexchange.com/questions/554417/logit-poisson-trick#:~:text=(a)%20The%20Poisson%20Trick%20is,likelihood%20isn't%20directly%20available.) a way of estimating Multinomial distributions as a series of poisson models
 * Survival Convolutions (for modeling inventory returns and making simulations vectorized)
   *  https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7273280/
   *  [Thomas Wiecki's COVID modeling PyMC video](https://www.youtube.com/watch?v=_DCkJkMji0U)
 * [Dan Marthaler's work on Wallenius Multivariate Hypergeometric distribution in Stan](https://discourse.mc-stan.org/t/biased-urn-problem-wallenius-noncentral-hypergeometric-distribution/21461/3) - a better alternative to a "censored multinomial" distribution, although tough to work with
 * [Evaluating Survival models](https://proceedings.mlr.press/v202/qi23b/qi23b.pdf)
  

Other resources on censored demand 
 *  Some papers
     * https://par.nsf.gov/servlets/purl/10066022
     * https://www.lancaster.ac.uk/stor-i-student-sites/tessa-wilkie/wp-content/uploads/sites/14/2020/03/Wilkie_RT1.pdf
     * https://arxiv.org/pdf/1810.09166.pdf#:~:text=There%20is%20a%20wide%20range%20of%20econometric%20models%20that%20has,negative%2C%20leading%20to%20zero%20purchases
     *  Has some good resources referenced, and attempts to use ML
 *  Blog posts
     * https://medium.com/afresh-engineering/accounting-for-censored-demand-in-sales-forecasting-bdc77192802d
       * Uses imputation, which works when the censoring rate is low but probably doesnt work under extreme stockouts
     * [Nicholas Vandeput Blog](https://nicolas-vandeput.medium.com/forecasting-demand-despite-shortages-fee899120c08): Talks about censoring at a high level   
