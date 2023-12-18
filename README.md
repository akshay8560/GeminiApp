Google AI SDK for Android
The Google AI client SDK for Android enables developers to use Google's state-of-the-art generative AI models (like Gemini) to build AI-powered features and applications. This SDK supports use cases like:


Generate text from text-only input
Generate text from text-and-images input (multimodal)
Build multi-turn conversations (chat)
For example, with just a few lines of code, you can access Gemini's multimodal capabilities to generate text from text-and-image input:

val generativeModel = GenerativeModel(
    modelName = "gemini-pro-vision",
    apiKey = BuildConfig.apiKey
)

val cookieImage: Bitmap = // ...
val inputContent = content() {
  image(cookieImage)
  text("Does this look store-bought or homemade?")
}

val response = generativeModel.generateContent(inputContent)
print(response.text)
Note

If you want to access Gemini on-device (Gemini Nano), check out the Google AI Edge SDK for Android, which is enabled via Android AICore.

Try out the sample Android app
This repository contains a sample app demonstrating how the SDK can access and utilize the Gemini model for various use cases.

To try out the sample app you can directly import the project from Android Studio via File > New > Import Sample and searching for Generative AI Sample or follow these steps below:

Check out this repository.
git clone https://github.com/google/generative-ai-android

Obtain an API key to use with the Google AI SDKs.

Open and build the sample app in the generativeai-android-sample folder of this repo.

Paste your API key into the apiKey property in the local.properties file.

Run the app.

Installation and usage
Add the dependency implementation("com.google.ai.client.generativeai:generativeai:<version>") to your Android project.

For detailed instructions, you can find a quickstart for the Google AI client SDK for Android in the Google documentation.

This quickstart describes how to add your API key and the SDK's dependency to your app, initialize the model, and then call the API to access the model. It also describes some additional use cases and features, like streaming, counting tokens, and controlling responses.

Documentation
Find complete documentation for the Google AI SDKs and the Gemini model in the Google documentation:
https://ai.google.dev/docs

