# Pet Classifier AI

Final project for the Building AI course

## Summary

This project uses a neural network to classify whether an animal is a dog or a cat based on height, weight, and length. The model applies AI methods to make binary predictions with high accuracy.

## Background

Many pet adoption centers and veterinary clinics need a quick way to identify animals from basic measurements. Manual classification is prone to error and takes time.  
My motivation came from wanting to practice AI classification while solving a real-world need in animal care. This project is important because:

* It automates pet type identification from simple measurements.
* It reduces manual work for shelters and vets.
* It can be expanded to other species or traits.

## How is it used?

The user provides the animal’s height, weight, and length.  
The neural network processes these inputs through hidden layers, applies an activation function in the output layer, and predicts “dog” or “cat.”

Example use cases:
* Animal shelters quickly identify new intakes.
* Mobile vet apps help pet owners identify breeds.
* Educational demos in AI courses.

<img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Sleeping_cat_on_her_back.jpg" width="300">

## Data sources and AI methods

Data comes from a custom dataset of pet measurements (simulated for this project).  
The AI model uses:
* Logistic regression for binary classification
* Feed-forward neural network with sigmoid activation
* Supervised learning with labeled data

| Feature  | Description            |
|----------|------------------------|
| Height   | Pet’s height in cm      |
| Weight   | Pet’s weight in kg      |
| Length   | Pet’s body length in cm |

## Challenges

This project does not:
* Identify pet breeds
* Handle mixed or ambiguous species data
* Account for measurement errors or outliers

Ethical considerations:
* Always use AI as an assistive tool, not the sole decision-maker.
* Avoid bias from small or unbalanced datasets.

## What next?

Future improvements:
* Expand dataset with real-world pet measurements
* Add more features (fur type, ear shape)
* Deploy as a mobile or web app

## Acknowledgments

* Inspiration: pet adoption workflows
* Course: [Building AI by Reaktor & University of Helsinki](https://buildingai.elementsofai.com/)
* Image: [Sleeping Cat on Her Back by Umberto Salvagnin](https://commons.wikimedia.org/wiki/File:Sleeping_cat_on_her_back.jpg#filelinks) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
