# OncoVision for BISV Hacks 2025
## Inspiration
We noticed that many people delay doctor visits, often risking late diagnoses. Our project is about making cancer screening more accessible and effortless, giving people the power to catch warning signs early and take control of their health before it’s too late.
## What it does
Users can take pictures to scan for signs of cancer on the skin (arm, leg, face) or orally (mouth, tongue, lips) 
## How we built it
For our website, we used a locally downloaded convolutional neural network--a model we trained ourselves--to detect different forms of cancer. The front end of the website is built with Svelte and SvelteKit, we use suppabase to store results--Your uploaded results do not contain pictures taken, only the model's predicted outputs. We also worked on an iOS app, this app uses the iPhone's Neural Engine, GPU, and CPU to their full extent to run the model efficiently on the device. The data stored in the iOS app is local to the device but would be shared through iCloud, completely end-to-end encrypted if put on the App Store--Us, nor Apple, would be able to see your pictures or results.
## Challenges we ran into
Training a convolutional neural network is no easy feat. We spent a great quantity of time refining our training scheme and data set. We made sure to train on a wide variety of inputs with the respective categories per model.
## Accomplishments that we're proud of
We are proud of not only the accuracy of the model but the ease of use of the application. The whole model runs locally on the device for a secure user experience.
## What we learned
We learned how hard it can be to work on a project with a love camera, in the browser, and mobile. Keeping track of results 
## What's next for OncoVision
We plan to finish building out the iOS app, and work to add other forms of cancer.
