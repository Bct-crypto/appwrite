import 'package:dart_appwrite/dart_appwrite.dart';

Client client = Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>') // Your project ID
    .setKey('<YOUR_API_KEY>'); // Your secret API key

Databases databases = Databases(client);

CollectionList result = await databases.listCollections(
    databaseId: '<DATABASE_ID>',
    queries: [], // (optional)
    search: '<SEARCH>', // (optional)
);