# GSoC2021 @ ML4SCI - Graph Neural Networks for BoostedTopJets Identification
This repository is the submission of the final Google Summer of Code 2021 project.

## Summary
The training notebooks demonstrate the performance comparison of Graph Neural Networks trained on x1 granularity images and Convolutional Neural Networks trained on x3 granularity images. Images with x3 granularity are more informative and have higher resolution (to be precise 3 times higher resolution). As can be seen from the ROC curves and ROC AUC score, both GNN and CNN have around similar performance for specific channels. The channels used here are pT, ECAL and HCAL along with the coordinates [eta,phi] for GNNs and all the 8 channels (pT, ECAL, HCAL, dz, d0, BPIX1, BPIX2, BPIX3) for CNNs. 

## Results
Acheived competetive performance with GNNs on just (1/20)th of the dataset used for CNNs. This presents a crucial evidence that when the GNNs are optimised and scaled to larger larger dataset, there is a huge potential and scope of improvement for the GNNs and may even perform better than the CNNs.   
1) CNN on 640K BoostedTopJets (x3 granularity) - Test ROC AUC score: 0.976 +/- 0.01
2) GNN on 32K samples of BoostedTopJets (x1 granularity with just energy channels and pT track) - Test AUC score: 0.971 +/- 0.01

## Future Objectives
The future goals of the project include scaling the Graph Neural Networks to more channels (pixel layers and tracker layers) and train CNNs & GNNs on a much larger dataset for developing a robust model. 
