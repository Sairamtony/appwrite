import 'package:appwrite/appwrite.dart';

Client client = Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>'); // Your project ID

Account account = Account(client);

Session result = await account.updateMfaChallenge(
    challengeId: '<CHALLENGE_ID>',
    otp: '<OTP>',
);
