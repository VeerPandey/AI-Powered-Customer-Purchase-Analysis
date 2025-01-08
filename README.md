# AI-Powered-Customer-Purchase-Analysis

# 1. Setting Up the Dataset

To ensure the program works correctly, you need to set up the dataset properly in Google Drive. Follow these steps:
	1.	Create a Folder in Google Drive:
	    Navigate to your Google Drive and create a folder named Dataset_AI_BookedBy in the My Drive.
	2.	Upload the Dataset:
  	  Upload the provided synthetic dataset file named synthetic_purchase_data.csv into the Dataset_AI_BookedBy folder.
	3.	Ensure the File Path:
	    The program expects the dataset to be located at this specific path: /content/drive/My Drive/Dataset_AI_BookedBy/synthetic_purchase_data.csv
      If you use a different folder name or file path, update the file_path variable in the code accordingly.
  4.	Generating the Dataset (if not available):
	    If the dataset is missing, the program will automatically generate a new one and save it to the specified path in Google Drive.

# 2. Installing Required Libraries
     Before running the program, ensure you have the necessary Python libraries installed. Use the following command to install them:
     pip install pandas numpy scikit-learn matplotlib tensorflow surprise

# 3. Running the Program

You can execute the program in Google Colab or any local Python environment. Follow these steps:
	1.	Mount Google Drive:
	•	Ensure your Google Drive is mounted in the notebook:
    from google.colab import drive
    drive.mount('/content/drive')


# 4.	Run the Main Program:
	•	Execute the main script that includes:
	•	Data Analysis
	•	Clustering
	•	Recommendation System
	•	The script will automatically load the dataset, perform analysis, cluster customers, and provide product recommendations.
# 5. Testing Functionalities

    To test specific parts of the program:
      	1.	Data Analysis:
      	•	The program will output:
      	•	Top-selling products.
      	•	Top-selling categories.
      	•	Average spending per customer.
      	•	Verify that these outputs match the expected results for the dataset.
      	2.	Customer Segmentation (Clustering):
      	•	The program will group customers into three clusters:
      	•	Frequent Recent Buyers
      	•	High Spenders
      	•	Dormant Buyers
      	•	Check the elbow plot and cluster labels to confirm that clustering is working as expected.
      	3.	Product Recommendation:
      	•	For a specific customer (e.g., C0102), the program will generate product recommendations using two methods:
      	•	Collaborative Filtering (Surprise Library)
      	•	TensorFlow-based Recommendation System
      	•	Verify the recommendations by running the respective functions:
          recommend_products_collaborative(customer_id='C0102')
          recommend_products_tensorflow(customer_id='C0102')
