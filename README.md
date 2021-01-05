# Breast-cancer-ML-code
#Set the seed to 1, then create a data partition splitting brca$y and the scaled version of the brca$x matrix into a 20% test set and 80% train using the following code:
set.seed(1, sample.kind = "Rounding")    # if using R 3.6 or later
test_index <- createDataPartition(brca$y, times = 1, p = 0.2, list = FALSE)
test_x <- x_scaled[test_index,]
test_y <- brca$y[test_index]
train_x <- x_scaled[-test_index,]
train_y <- brca$y[-test_index]

#You will be using these training and test sets throughout the exercises in Parts 3 and 4. Save your models as you go, because at the end, you'll be asked to make an ensemble prediction and to compare the accuracy of the various models!


