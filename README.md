
Introduction:

Tamil, being one of the oldest and widely spoken languages in the world, has a rich cultural heritage. The ability to accurately extract and process Tamil text from digital documents and images is crucial for various applications, such as document digitization, translation, and information retrieval. This project explores the use of the Tesseract Open Source OCR Engine to perform Tamil printed word recognition, highlighting the steps involved in setting up the required tools and libraries, and evaluating the performance of the OCR system.

Objectives:
1. Install and configure the Tesseract-OCR engine and the Tamil language pack on a Colab environment.
2. Implement a workflow to extract text from a single TIFF file, including pre-processing steps like grayscaling, blurring, and thresholding.
3. Evaluate the performance of the proposed OCR system by comparing it with an existing online OCR service and the manual ground truth.
4. Extend the OCR implementation to process a set of TIFF files and generate a consolidated output.

Methodology:
1. **Installing Tesseract-OCR and Language Packs**: The first step is to install the Tesseract-OCR engine and the Tamil language pack on the Colab environment. This is achieved using the `apt-get` command, and the necessary packages are downloaded and installed.

2. **Extracting Text from a Single TIFF File**: The process of extracting text from a TIFF file involves several pre-processing steps. The image is first read using OpenCV, then converted to grayscale, blurred to reduce noise, and thresholded to highlight the text. Contours are detected, and bounding boxes are drawn around the text regions. The text is then extracted using the Tesseract-OCR engine with the Tamil language model.

3. **Cleaning the Recognized OCR Text**: The extracted text is cleaned by removing unnecessary characters, such as newlines, apostrophes, and underscores, to prepare it for evaluation.

4. **Evaluation Metrics**: The performance of the proposed OCR system is evaluated using the following metrics:
   - Accuracy: Calculated using the `fastwer` library, which compares the OCR output with the manual ground truth.
   - Levenshtein Distance: Measures the edit distance between the OCR output and the manual ground truth.
   - Cosine Similarity: Computes the cosine similarity between the OCR output and the manual ground truth, providing an additional metric for similarity.

5. **Extending to Multiple TIFF Files**: The OCR implementation is further extended to process a set of TIFF files. The text from each file is extracted, concatenated, and saved to a single output file, following the same cleaning and preprocessing steps.

Results and Discussion:
The results of the evaluation show that the proposed OCR system achieves an accuracy of 98.10% when compared to the manual ground truth, outperforming the existing online OCR service, which had an accuracy of 96.00%. The Levenshtein Distance also reflects this improvement, with the proposed OCR having a distance of 79 compared to 131 for the online OCR.

The cosine similarity between the proposed OCR output and the manual ground truth is 98.6%, further confirming the high similarity and accuracy of the proposed system.

Conclusion:
This project demonstrates the effectiveness of the Tesseract-OCR engine in recognizing Tamil printed text, even when dealing with scanned TIFF files. The step-by-step implementation, including the preprocessing steps and evaluation metrics, provides a comprehensive approach to Tamil text recognition. The superior performance of the proposed OCR system highlights the potential for using open-source tools like Tesseract to address the challenges of Tamil text extraction and processing. This work can serve as a valuable reference for researchers and developers working on Tamil language processing and digitization tasks.
