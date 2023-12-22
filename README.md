# cazton_test


- There are two `.ipynb` files present.
- One for collecting the data and the otehr for fine-tuning the model.
- The programs were run directly on the free version of Google Colab.
- Directly importing the files into Colab and running them should work.
- The only change that needs to be done is where to save the files.
  - In the `get data.ipynb` file, the cell at the beggining notes the main directory.
- Packages installed from `pip` that were not present in Colab: `datasets`, `evaluate`, `torch==2.0`, `peft`


###### Methodology
- Scrape data using BeutifulSoup from cazton.com
  - Using `href` and `a` tags, collect all pages linked on a page.
  - Recursively continue scraping pages until all under the domain are scraped.
- Save each webpage by the name of the URL after the domain.
- Merge all the files into one `json`.
- Create a file structure suitable for the `Dataset` class of Huggingface.
- Load required packages.
- Load base model to be fine-tuned.
- Load dataset.
- Tokenize dataset as required for a QnA dataset.
- Initialise and train using the Huggingface trainer.


Link to video Demo - 
