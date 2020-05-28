# GANS
Libraries used: __future__, torch, and various libraries from torch-like torch.nn, torch.optim , torchvision.transforms, etc.

Project Details:
• Trained the model on the CIFAR 10 dataset.
• Model had a batch size and image size of 64.
• The model produces 25 epochs.
• All the generated images and the real image are present in the results folder.

Generator:
• It uses the ReLU and tanh activation function.
• It has inverse convolution, with the initial input channels being 100 and initial output channels being 512.
• In every subsequent layer, the input channels are equal to the output channels of the previous layer and the output is half of the input channels i.e. in layer two input channels is 512 and output is 256.
• In the final layer, input channels become 64 and output becomes 3.
• Only for the final layer, tanh activation is used, for all else ReLU is used.

Discriminator:
• It uses the LeakyReLU and Sigmoid activation functions.
• It has a convolution, with the initial input channels being 3 and initial output channels being 64.
• In every subsequent layer, the input channels are equal to the output channels of the previous layer and the output is double the input channels i.e. in layer two input channels are 64 and output is 128.
• In the final layer, input channels become 512 and output becomes 1.
• Only for the final layer, Sigmoid activation is used, for all else LeakyReLU is used.
