import Appwrite

let client = Client()
    .setEndpoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .setProject("<YOUR_PROJECT_ID>") // Your project ID
    .setKey("<YOUR_API_KEY>") // Your secret API key

let messaging = Messaging(client)

let provider = try await messaging.createMailgunProvider(
    providerId: "<PROVIDER_ID>",
    name: "<NAME>",
    apiKey: "<API_KEY>", // optional
    domain: "<DOMAIN>", // optional
    isEuRegion: false, // optional
    fromName: "<FROM_NAME>", // optional
    fromEmail: "email@example.com", // optional
    replyToName: "<REPLY_TO_NAME>", // optional
    replyToEmail: "email@example.com", // optional
    enabled: false // optional
)

