# Pneumonia-Prediction

## Summary

This project developed a convolutional neural network (CNN) model that identifies pneumonia cases from chest x-rays.

The model achieved a 91.67% accuracy, with a 95% recall on identifying positive cases (95% sensitivity), and a 86% on negative cases (86% specificity) on 120 testing x-ray images.

Examples: 
![predict](/images/test_5) ![predict2](/images/test_78)

## Background

Pneumonia is an infection of the lungs. Its seriousness can range from mild to life-threatening, whisch is why identifying positive pneumonia cases from the results of the medical tests is important.

| normal | pnemonia |
|-------|-------|
| ![normal x ray](/chest_xray/val/NORMAL/NORMAL2-IM-1436-0001.jpeg) | ![pna x ray](/chest_xray/val/PNEUMONIA/person1954_bacteria_4886.jpeg) |


## Results

The same CNN model yielded good results with two different random states. However, one of them has a 100% sensitivity, which would never happen in real world. The one kept in this repo is therefore the other one.

| Accuracy | Loss | Sensitivity (True positive rate) | False negative rate | False positive rate | Specificity (true negative rate) |
|------|-----|-----|-----|------|------|
| 0.9167 | 0.22 | 0.95 | 0.05 | 0.08 | 0.86 |

95% sensitivity in medical tests is genearlly considered a high number. The model also has a 86% specificity. Therefore, this trained model is good at identifying positive cases correctly, but is more prone to falsely predicting a negative result as positive.

However, in the context of pneumonia, this result should be not bad, if not pretty good.

86% specificity - although there is room for improvement, this number of specificity is not very low in medical tests
95% sensitiivty - a very good sensitivity in real world medical tests

In the case of pneumonia, sensitivity is more ipmortant than specifity because pneumonia could be deadly. If we have to choose, we would rather have false poisitives than missing a true positive case.

| model architecture |
|-----|
| ![arch](/images/cnn_architecture.png)
