### Description:
Use Bing Image search API to scrape down 
a dataset for training

### Setup:
[Get an API key here](https://azure.microsoft.com/en-us/try/cognitive-services/?api=bing-image-search-api)
and put it in a file called `apiKey.txt`

### Downloading dataset: 
`python search_bing_api.py --query "charmander" --output dataset/charmander`

### Training:
`python train.py --dataset dataset --model pokedex.model --labelbin lb.pickle` 

### Classify Test 
`python classify.py --model pokedex.model --labelbin lb.pickle --image charmander_counter.png`

### CoreML converter
`python coremlconverter.py --model pokedex.model --labelbin lb.pickle`

#### References:
[Scraping Dataset for Training](https://www.pyimagesearch.com/2018/04/09/how-to-quickly-build-a-deep-learning-image-dataset/)
[Training a Keras Model](https://pyimagesearch.com/2018/04/16/keras-and-convolutional-neural-networks-cnns/)
[Running Keras models on iOS with CoreMLs](https://www.pyimagesearch.com/2018/04/23/running-keras-models-on-ios-with-coreml/)