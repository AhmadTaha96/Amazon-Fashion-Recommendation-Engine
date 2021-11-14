# Amazon-Fashion-Recommendation-Engine

### Recommend Similar Fashion Products Based on Content



![AF](https://user-images.githubusercontent.com/91129320/141696663-de3ba7ad-b0a1-4ae7-81f9-ad1ab013daf8.jpg)



# Real-world / Business


### Problem Statment

In this problem we want to recommend similar product to a given Amazon fashion product, that so we shall be given a product image with product information and we need to get most similar product to our product out of Amazon dataset.


**********************************


### objectives and constraints


**Objectives:**

Our task is to get the most similar product to our product out of Amazon fashion dataset, this data shall be updated regularly but we will not process this part here, we just keep up with the initial dataset we have.

**********************************

**Constraints:**

The Most important part of our task is not to recomment and get identical products to the query product, because in our dataset we might encounter some identical products to query product which may differ in size only so in this case the result would exactly the same except for the title or size features for that matter, for that we don't want that, because it's not good to get the exact product at the recommendation bar not to mention that give no info or value to the site.

In this problem some diversity in the result is requested, but a lot of it would get result far from the query product which yield bad and far results from desired, so cleaning the processing data is a critical stage in our processing taks, for that we shall dive depth into it.

Interpretability is not really important here because user care only about the results and only the results, so we shall not focus too much on this side.

Speed & Latency is not really strict here as well, but the result shall be given and prepared once the page loaded and this latency would be enough but no more.


**********************************


### ML Problem Formulation

Given a product information including image, we should get the top similar products that get the user or the client to discover more products at surfing time.


**********************************


### Performance metrics

The main performance metric here is distance between each product and the result that have been fetched, and of course after removing all identical products from the processing as this would result in the lowest distance such as Ecludian, Manhatan or any other Minkowski based distance.


**********************************


### Data Overview

The Data is taken from Amazon advertising api for women's tops, the dataset consist of 183138 rows and 19 features or columns so to speak.


The features or columns are:

* asin

* author 

* availability

* availability_type

* brand

* color

* editorial_reivew

* editorial_review

* formatted_price

* large_image_url

* manufacturer

* medium_image_url

* model

* product_type_name

* publisher

* reviews 

* sku

* small_image_url

* title



*********************

**Choosen Features:**


Out of the previous features we shall only consider using 6 or 7 features as follows:


* Asin -------------------------------> Amazon standard identification number.

* Brand ------------------------------> brand of the product.

* Color ------------------------------> Color information of apparel, it can contain many single or many colors as red and black stripes or None.

* Product_type_name ------------------------------> type of the product like SHIRT/TSHIRT.

* Large_image_url ------------------------------> url of the image in large size.

* Title ------------------------------> title of the product.

* Formatted_price ------------------------------> price of the product

* Manufacter ------------------------------> manufacter the product belong to.
