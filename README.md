# Sandwich Ingredient Identifier

My project helps people who have many foods they are allergic to or dislike. Using AI, my project helps cut down on the time and effort dedicated to finding something to eat.

Though I hope to expand on this project, it currently only classfies sandwiches as either having tomatoes and eggs ("deluxe"), having tomatoes ("veggie"), or having neither ("plain").

![Sandwiches that contain both tomatoes and eggs are classified as "deluxe"](https://i.imgur.com/9CUV0sV.jpeg)

## The Algorithm

I used a Jetson Nano to complete this project. Using a resnet18 model retrained with images of three classes of sandwiches, imagenet is then able to classify any sandwich into these groups. 

## Running this project

1. Download my code from the GitHub project onto your Jetson Nano
2. To classify an image under data/sandwich/test/deluxe, run `imagenet  --model=models/sandwich/resnet18.onnx --labels=data/sandwich/labels.txt --input_blob=input_0 --output_blob=output_0 data/sandwich/test/deluxe data/sandwich/test_deluxe_output`
3. The result will be output in data/sandwich/test_deluxe_output.
4. To see the result, scp the outputted file from the Jetson Nano onto your computer or if Visual Studio Code has been set up, view the file there.


[Video Demo](https://youtu.be/5wYSKe4doLY)
