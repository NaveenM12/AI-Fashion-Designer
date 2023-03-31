# AI-Fashion-Designer

This project trains [Nvidia's StyleGAN2](https://github.com/NVlabs/stylegan2-ada-pytorch) model from scratch on a custom dataset of fashion images to generate completely new and unique designs. The model has the ability to generate a nearly-infinite number of novel looks, while also allowing the user to adjust key aspects such as color, sleeve length, and more! The program learns from past designs from brands such as LV, Dior, Givenchy, and more over the past few years to innovate new looks and produce creative designs.

Example (See Example Image Folder for More!):
![My Image](AI_Fashion_Designer_Examples/SC2.png)


## Training
The model is trained on thousands of scraped images from [firstView fashion archives](https://firstview.com/) which are cleaned and normalized for the model inputs. The [training file](https://github.com/NaveenM12/AI-Fashion-Designer/blob/main/Fashion_SG2_ADA_PyTorch.ipynb) was run using a T4 GPU for 2 weeks then I manually chose the model instance with what I deemed to be the best fit (there is oscillating accuracy that does not singularly converge). The model produces a .pkl file that can be converted to a .pt file in the notebook for easier access and makes it easy to resume training. The procces of scraping and generating such a dataset from scratch was challenging, as was training the model and this process could surely be improved. 

## Generation
Using Gradio, we are able to use the trained model to generate completely new images for different seeds. Using any positive seed entered in gradio, the model will generate new images. Note that it may take many tries to generate a realistic seed image as some of the images produced may not be realistic. Nevertheless, the seed is saved, so no matter if you restart the model or not, going back to the same seed in the next run will produce the same image, so if you find a suitable seed, you will be able to return to it, which is really helpful. 
The ability of this model to innovate new looks is really creative, so it may take a few tries to find a good seed, but the variety of looks is till really cool to see. Further, I think that these generations can serve as inspirations for actual looks, so even if they are not directly transferred to individual looks, I think they can be extremely valuable in sparking a new idea or helping create new designs. 

## Customization & UI

## Next Steps
Separation of Training Sets: Male vs Female, Fall vs Spring, etc. 
Training for Longer:
More/Better customization: 

Technologies Used: Python, Pytorch, Tensorflow, Keras, StyleGAN2, Neural Network, Clustering, Gradio
