+++
# A Projects section created with the Portfolio widget.
widget = "portfolio"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 65  # Order that this section will appear.

title = "Research"
subtitle = "If you can't access a paywalled article, feel free to email me. I can almost always share a pre-print version.<br>[Publications](#publications)<br>[Working papers](#working)"

[content]
  # Page type to display. E.g. project.
  page_type = "project"

  # Filter toolbar (optional).
  # Add or remove as many filters (`[[content.filter_button]]` instances) as you like.
  # To show all items, set `tag` to "*".
  # To filter by a specific tag, set `tag` to an existing tag name.
  # To remove toolbar, delete/comment all instances of `[[content.filter_button]]` below.

  # Default filter index (e.g. 0 corresponds to the first `[[filter_button]]` instance below).
  filter_default = 0

  # [[content.filter_button]]
  #   name = "All"
  #   tag = "*"

  # [[content.filter_button]]
  #   name = "Deep Learning"
  #   tag = "Deep Learning"

  # [[content.filter_button]]
  #   name = "Other"
  #   tag = "Demo"

[design]
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns = "2"

  # Toggle between the various page layout types.
  #   1 = List
  #   2 = Compact
  #   3 = Card
  #   5 = Showcase
  view = 2

  # For Showcase view, flip alternate rows?
  flip_alt_rows = false

[design.background]
  # Apply a background color, gradient, or image.
  #   Uncomment (by removing `#`) an option to apply it.
  #   Choose a light or dark text color by setting `text_color_light`.
  #   Any HTML color name or Hex value is valid.

  # Background color.
  color = "#E0DFDB80"

  # Background gradient.
  # gradient_start = "DeepSkyBlue"
  # gradient_end = "SkyBlue"

  # Background image.
  # image = "background.jpg"  # Name of image in `static/img/`.
  # image_darken = 0.1  # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.

  # Text color (true=light or false=dark).
  # text_color_light = true  

[advanced]
 # Custom CSS.
 css_style = ""

 # CSS class.
 css_class = ""
+++

## Publications
### {#nica-dynamics}
* [Heterogeneous impact dynamics of a rural business development program in Nicaragua](https://www.sciencedirect.com/science/article/pii/S0304387818304851)
with Michael Carter and Patricia Toledo<br>
_Journal of Development Economics_, 138:77-98, May 2019 <br>
  - [NBER WP version (No. 22628)](https://www.nber.org/papers/w22628.pdf)
    <details><summary>Abstract</summary>
    We study the impacts of a rural development program designed to boost   the income of the small-farm sector in Nicaragua. Exploiting the random   assignment of treatment, we find statistically and economically   significant impacts on gross farm income and investment in productive   farm capital. Using continuous treatment estimation techniques, we   examine the evolution of program impacts over time and find that the   estimated income increase persists and that the impacts on productive   capital stock continue to rise even after the program concluded.   Additionally, panel quantile methods reveal striking heterogeneity of   program impacts on both income and investment. We show that this   heterogeneity is not random and that there appear to exist low-  performing household types who benefit little from the program, whereas   high-performing (upper quantile) households benefit more substantially.   Analysis using generalized random forests, a machine learning algorithm,   points toward greater program impacts for households who were   disadvantaged at baseline. Even after controlling for this source of   heterogeneity, we find large and persistent differences in how much   different types of households benefited from the program. While the   benefit-cost ratio of the program is on average positive, the impact   heterogeneity suggests that business development programs aiming to   engage farm households as agricultural entrepreneurs have limitations as   instruments to eliminate rural poverty.
    </details>
{{< figure library="true" src="nica_capital_small.png" title="Heterogeneity matters" lightbox="false" width="300px" >}}

### {#money-matters}
* [Money matters: the role of income and yields in agricultural technology adoption](https://doi.org/10.1093/ajae/aay050) with Jeffrey D. Michler, Simone Verkaart, and Kai Mausch <br>
_American Journal of Agricultural Economics_, July 2018.
  * [Ungated WP version](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3174824)
  * [Replication data](/files/AJAE-data.zip)
    <details><summary>Abstract</summary>
    Despite the growing attention to technology adoption in the economics literature, knowledge gaps remain regarding why some valuable technologies are rapidly adopted, while others are not. This paper contributes to our understanding of agricultural technology adoption by showing that a focus on yield gains may, in some contexts, be misguided. We study a technology in Ethiopia that has no impact on yields, but that has nonetheless been widely adopted. Using three waves of panel data, we estimate a correlated random coefficient model and calculate the returns to improved chickpea in terms of yields, costs, and profits. We find that farmers’ comparative advantage does not play a significant role in their adoption decisions and hypothesize that this is due to the overall high economic returns to adoption, despite the limited yield impacts of the technology. Our results suggest economic measures of returns may be more relevant than increases in yields in explaining technology adoption decisions.
    </details>
{{< figure library="true" src="chickpea_returns_small.jpg" title="Returns by adoption groups" lightbox="false" width="300px" >}}

### {#natural-disasters}
* [Natural disasters, social protection, and risk perception](https://www.sciencedirect.com/science/article/pii/S0305750X17303893)
with Philip Brown, Adam J. Daigneault, and Wenbo Zou <br>
_World Development_, 104:310–325, April 2018
  * [Ungated WP version](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3086868)
    <details><summary>Abstract</summary>
    Natural disasters give rise to loss and damage and may affect subjective expectations about the prevalence and severity of future disasters. These expectations might then in turn shape individuals’ investment behaviors, potentially affecting their incomes in subsequent years. As part of an emerging literature on endogenous preferences, economists have begun studying the consequences that exposure to natural disasters have on risk attitudes, perceptions, and behavior. We add to this field by studying the impact of being struck by the December 2012 Cyclone Evan on Fijian households’ risk attitudes and subjective expectations about the likelihood and severity of natural disasters over the next 20 years. The randomness of the cyclone’s path allows us to estimate the causal effects of exposure on both risk attitudes and risk perceptions. Our results show that being struck by an extreme event substantially changes individuals’ risk perceptions as well as their beliefs about the frequency and magnitude of future shocks. However, we find sharply distinct results for the two ethnicities in our sample, indigenous Fijians and Indo-Fijians; the impact of the natural disaster aligns with previous results in the literature on risk attitudes and risk perceptions for Indo-Fijians, whereas they have little to no impact on those same measures for indigenous Fijians.
    </details>
{{< figure library="true" src="violin_plot_ethnicity_evan.png" title="Beliefs about losses" lightbox="false" width="300px" >}}
{{< figure library="true" src="Evan_Dec_16-17_IR_Animation.gif" title="Cyclone Evan" lightbox="false" width="300px" >}}

### {#stata-paper}
* [Fitting and interpreting correlated random coefficient (CRC) models using Stata](https://www.stata-journal.com/article.html?article=st0517)
with Oscar Barriga Cabanillas, Jeffrey D. Michler and Aleksandr Michuda
_Stata Journal_, 18(1):159–173, 2018
  * The `-randcoef-` command estimates follows [Suri (2011)](http://onlinelibrary.wiley.com/doi/10.3982/ECTA7749/abstract) to estimate correlated random effects (CRE) and correlated random coefficient (CRC) models
  * [Blog post](https://blogs.worldbank.org/impactevaluations/stata-package-estimating-correlated-random-coefficient-models)



### {#Nica-semipar}
* [Identifying the impact dynamics of a small farmer development scheme in Nicaragua](https://doi.org/10.1093/ajae/aat042)
with Michael Carter and Patricia Toledo<br>
_American Journal of Agricultural Economics (Papers and Proceedings)_, 95(5):1359–1365, July 2013

* [Do differences in attitudes explain differences in national climate change policies?](http://www.sciencedirect.com/science/article/pii/S0921800907003588)
with Thomas H. Tietenberg <br>
_Ecological Economics_, 65(2):315–324, 2008

* [Rational foolishness would destroy a public service broadcasting system](http://www.tandfonline.com/doi/full/10.1080/08997760802544772#.VF_H1_mXCq4)<br>
with Sune Tjernström<br>
_Journal of Media Economics_, 21(4):258–263, 2008.

<br>
<br>

## Working papers {#working}
### {#mahindi-master}
* [Learning by (Virtually) Doing: Experimentation and Belief Updating in Smallholder Agriculture](files/TLHC2020.pdf)
_with Travis Lybbert, Rachel Hernández Frattarola, and Juan Sebastian Correa_ <br>
Revised and resubmitted :crossed_fingers:
  <details><summary>Abstract</summary>
  In much of sub-Saharan Africa, soil quality heterogeneity hampers farmer   learning about the returns to different inputs. This can partly explain   why we observe
  limited adoption of improved inputs in the region. We study how Kenyan   farmers respond to an interactive app that enables them to discover   agricultural input returns on a virtual plot that is calibrated to   resemble their own. Farmers update both their beliefs and behaviors after   engaging with the virtual learning app. Additionally, farmers revise their   beliefs
  upwards after using the app. In an incentive-compatible experiment,   farmers receive an input budget from the research team, which they can   allocate across farm inputs. After they play several virtual seasons on   the app, they have the opportunity to update these allocations. Farmers   revise their input allocations along several dimensions after the virtual   learning experience. As evidence that these adjustments emerge from real   learning, we show that farmers with the highest predicted returns to lime--  -an unfamiliar input in this region---increase their lime orders more than   others. Our results suggest that engagement with a personalized virtual   platform can induce real learning and enhance  farmers' beliefs and   technology choices.
  </details>

### {#1af}
* [Can Smallholder Extension Transform African Agriculture?](https://www.nber.org/papers/w26054)
_with Joshua Deutschmann, Maya Duru and Kim Siegal_ <br>
NBER Working Paper No. 26054
  <details><summary>Abstract</summary>
  Agricultural productivity in Sub-Saharan Africa lags behind all
  other regions of the world. Decades of investment in agricultural research and extension have yielded more
  evidence on what fails than on what works---especially for the small-scale producers
  who dominate the sector.
  We study a program that targets multiple constraints to productivity at   once,
  similar to anti-poverty "graduation" interventions. Analyzing a randomized   controlled trial in western
  Kenya, we find that participation causes statistically and economically
  significant gains in output, yields, and profits. In our preferred
  specification, the program increases maize production by 26% and profits by
  16%. The program increases yields uniformly across the sample,
  while treatment effects on total output and profit impacts are slightly
  attenuated at the top end of the distribution.
  </details>

### {#media-motivation}
* [Media and Motivation: the Effect of
Performance Pay on Writers and Content](files/BGT2020.pdf)
_with Ivan Balbuzanov and Jared Gars_
  <details><summary>Abstract</summary>
  We study how incentives for journalists affect the quantity, quality, and composition of online
  media content. We report results from a field experiment within an online news firm in Kenya.
  Writers were randomly allocated to earn a piece-rate per article published or to a pay-per-view
  (PPV) contract. The PPV contract induced writers to produce more "popular" articles, but
  writers chose to submit fewer articles. Specifically, the PPV contract resulted in a 120% increase
  in total pageviews, a 180% increase in pageviews per article, and a 40% reduction in the number
  of articles produced. In line with our theoretical predictions, the effect on article quantity
  is concentrated among risk averse writers. Further, when given a choice, risk-averse writers
  tend to select out of the output-based contract. We also document changes along multiple
  non-incentivized dimensions of news production: writers shift away from producing local news
  towards national-level news. We see limited changes in article quality or in the prevalence of
  clickbait. Our study suggests that output-based incentive contracts have substantial implications
  for journalists' effort and content choices, and more broadly for selection into risky "gig work."
  </details>

### {#grc}
* [A Group Random Coefficient Approach to Modeling Heterogeneity in Technology Adoption](files/TGBLMM2020)
_with Oscar Barriga Cabanillas, Dalia
Ghanem, Travis Lybbert, Jeffrey D. Michler, and Aleksander Michuda_
  <details><summary>Abstract</summary>
  Our paper revisits the econometric model that Suri (2011) (S2011) used in her study of heterogeneous returns to agricultural technology adoption. We propose an alternative group random coefficient (GRC) estimation strategy and revisit the empirical puzzle of why relatively
  few sub-Saharan farmers adopt modern technologies. Drawing on recent developments in the
  nonparametric panel identification literature, we start with an unrestricted GRC model that
  nonparametrically identifies the returns to adoption under time homogeneity. We show that the
  parameters of the S2011 correlated random coefficient model (CRC) can be identified from a
  restricted version of the GRC method. Specifically, the model in S2011 implies a key restriction
  that we call linearity in comparative advantage (LCA). Our unrestricted GRC model can be
  used to detect identification concerns for key structural parameters from the CRC model. We
  illustrate our method using the same data set as the original study andnd that the motivating
  empirical puzzle remains unsolved.
  </details>

### {#networks}
* Learning from Others in Heterogeneous Environments <br>
(being revised; draft available upon request)

### {#beliefs-kenya}
* Seeds of Uncertainty: Information, Subjective Expectations, and Technology Adoption
_with Jared Gars_ <br>
draft available upon request

### {#filling-niche}
* Filling a Niche: the Impacts of a Local Seed Company on Maize Productivity in Kenya
_with Samuel Bird, Michael Carter, Travis Lybbert, Mary Mathenge and Tim Njagi_ <br>
draft available upon request

<br>
<br>

## Work in progress

### {#dukas}
* Market-Level Effects of Competition in Agricultural Input Markets: Prices, Quality, and Mechanisms<br>
_with Maya Duru and Laura Schechter_

### {#dukas}

* When Intentions Matter---Identifying the Prevalence
and Source of Poor-quality Inputs in Kenya <br>
_with Jose Clavijo and Travis Lybbert_

### {#bundling}
* Nonlinear Pricing Complexity and Consumer Behavior
_with Joshua Deutschmann and Jeff Michler_

### {#arrested-development}
* Arrested Development: the Inefficiencies
of Electoral Cycles in Infrastructure Projects
_with Evan Morier_

### {#dirt-on-dirt}
* The Dirt on Dirt: Soil Characteristics
and Variable Fertilizer Returns in Kenyan Maize Systems
_with Michael Carter and Travis Lybbert_

### {#disadoption}
* Income Volatility and Technology Choice
_with Rachel Hernández  Frattarola_

### {#migration}
* Selection and Heterogeneity in the Returns to Migratio
_with Eduardo Cenci and Marieke Kleemans_
