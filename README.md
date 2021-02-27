# Good, Great, Excellent Quality Reviews of Amazon Electronics

## Project4 Natural Language Processing (NLP)

# Inspiration for the Study
	Amazon organizes its products into categories, but that doesn't tell us how the customers are talking about the products.  We can take text from 22 years of "Electronics" product reviews and apply unsupervised learning techniques to identify topics of particular interest to customers. With this information Amazon could redesign some of its website layout to increase the user experience.  
	
	For example, (Spoiler Alert!) it is apparent from modeling that 'tablets' are of particular interest to customers, but 'tablets' do not have their own 'Category' as designated by Amazon on their Electronics Deparmtnet page.  This may hinder user experience when tryign to learn about which tablet may be best for them.

# Repo Overview

The notebook is organzed into folders:

* Presentation
  * PPTX and PDF format

* Notebooks
  * nb1 - Data import, Pre-Processing, and NMF (Non-negative Matrix Factorization) model
  * nb2 - LDA (Latent Dirichlet Allocation) Model setup, pre-processing, and visualizations.
* Misc
  * text file linking data source, code references, and Amazon sections referenced

# Data

## Methods



* NMF and LDA Topic Modeling methods were applied to a subset of the data represetnging ~67,000 electronics product reviews from 1996-2018.
* The LDA model was chosen over NMF due to ease of interpretability of topics.
  * 5 topics were chosen from model runs ranging from 4-12 topics.
* ![topics_pyLDAavis](/Users/johnmetzger/Desktop/topics_pyLDAavis.png)

## Findings

* The 5 topics were labeled along with descriptors:

  1) Camera

  * Performance

  * Hardware

  * Connectivity

    ![camera_docword_count](/Users/johnmetzger/Desktop/camera_docword_count.png)

    ![camera_pyLDAvis](/Users/johnmetzger/Desktop/camera_pyLDAvis.png)

  2) Laptop

  * Hardware
  * Battery
  * Performance

  ![laptop_docword_count](/Users/johnmetzger/Desktop/laptop_docword_count.png)

  ![laptop_pyLDAvis](/Users/johnmetzger/Desktop/laptop_pyLDAvis.png)

  3) Tablet

  * Ease of Use
  * Size

  ![tablet_docword_count](/Users/johnmetzger/Desktop/tablet_docword_count.png)

  ![sound_pyLDAvis](/Users/johnmetzger/Desktop/sound_pyLDAvis.png)

  4) Sound

  * Speakers
  * Quality
  * Performance

  ![sound_docword_count](/Users/johnmetzger/Desktop/sound_docword_count.png)

  ![tablet_pyLDAvis](/Users/johnmetzger/Desktop/tablet_pyLDAvis.png)

  5) Miscallaneous Hardware

  * Chargers
  * Time
  * Connectivity

![topics_all_count](/Users/johnmetzger/Desktop/topics_all_count.png)

![misc_pyLDAvis](/Users/johnmetzger/Desktop/misc_pyLDAvis.png)

# Final Thoughts

* Topic modeling using LDA shows that 'tablets' and 'camera'-related items are discussed in ways that differentiate themselves from other reviews.  Unlike camera-related items, the tablets are not given their own Category (as defined by amazon: https://www.amazon.com/b?node=172282) suggesting that altering the website format make it easier to navigate to tablets and tablet-related items may increase user experience.
* Further work:
  * Experiment with different models and libraries
    * e.g., spaCy
  * Control for language
    * Spanish words because to show up in topics when the number of topics in LDA was expanded to 12.
  * Compare results with other departments to see if topics are identified that do not neatly watch with Amazon's chosen categories.
    * e.g., Pet Supplies