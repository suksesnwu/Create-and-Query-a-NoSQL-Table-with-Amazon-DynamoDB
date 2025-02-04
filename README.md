# Create and Query a NoSQL Table with Amazon DynamoDB: Music Library Use Case

In this tutorial, we'll walk you through the process of creating a NoSQL table in DynamoDB for a music library. You'll use DynamoDB to store and query data about various South African artists and their songs.

## Prerequisites

Before you begin, make sure you have:

- An AWS account.
- Basic understanding of DynamoDB and AWS services.

## Tutorial Steps

### 1. Creating the DynamoDB Table

1. Sign in to your AWS Management Console and navigate to **DynamoDB**.
2. Click on **Create Table**.
3. In the **Table name** box, enter `Music`.
4. In the **Partition key** box, type `Artist`. This will allow data to be spread across partitions for scalability.
5. In the **Sort key** box, enter `Song` to enable sorting by song titles for each artist.

#### Enabling DynamoDB Auto Scaling

1. Click on **Customize settings** under Capacity.
2. Select **Enable Auto Scaling** for both read and write capacities.
3. DynamoDB will automatically manage capacity scaling using an IAM role called `DynamoDBAutoscaleRole`.

Creating the Music Table
![music table](https://github.com/user-attachments/assets/505f144b-c313-44ae-b27b-f9e1c939baa3)

### 2. Adding Items to the Music Table

Now, let's add some South African local artists and their songs to the table. For example:

- **Artist**: Kabza De Small
  - **Song**: "Iyasha Imoto"
- **Artist**: DJ Maphorisa
  - **Song**: "Pretty Girls Love Amapiano"
- **Artist**: Makhadzi
  - **Song**: "Ghanama"
  - **Album**: "African Queen" // add attribute
- **Artist**: Makhadzi
  - **Song**: "Yellow Bone"
  - **Year**: "2022" // add attribute
- **Artist**: Kabza De Small
  - **Song**: "Iyasho Imoto"
  - **Feat**: "JazziQ" // add attribute
- **Artist**: JazziQ
  - **Song**: "Fede"

To add items manually:

1. Go to the **Items** tab in your DynamoDB table.
2. Click on **Create item**.
3. Add key-value pairs for each song (e.g., Artist, SongTitle, etc.).
4. Click **Save** after adding each song.

 Adding Items to the Music Table  
![add items to the table](https://github.com/user-attachments/assets/0f47751a-30fa-45e9-bcff-6a75e4dd10a0)

### 3. Querying Data from the Music Table

To query the data you just added, follow these steps:

1. Go to the **Query** tab in your table.
2. Select **Artist** as the partition key and enter a specific artist (e.g., "Kabza De Small") to retrieve all songs by that artist.
3. Click on **Run** to see the list of songs by that artist.

You can also add a **SongTitle** filter to query for a specific song.

 Querying Music Data 
![Query Kabza](https://github.com/user-attachments/assets/b70eb812-de1b-4285-a4e2-685a01582b90)

### 4. Cleaning Up the Table

After completing the tutorial, remember to delete the table to avoid incurring charges:

1. Go to the **Tables** section in DynamoDB.
2. Select the `Music` table.
3. Click **Delete**.
4. Confirm the deletion.

 Deleting the Table  
![delete-music-table](https://github.com/user-attachments/assets/ea831063-e9fd-4a0c-b06b-3df268a1d2a0)

## Conclusion

In this tutorial, you created and queried a DynamoDB table for a music library featuring South African artists. You also learned how to use DynamoDB Auto Scaling to manage table capacity and how to add and query data efficiently.

For more information, you can refer to the [official tutorial](https://aws.amazon.com/tutorials/create-nosql-table/).

---

You can replace the image links with your actual screenshot files. 
