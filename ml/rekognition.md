# Amazon Rekognition

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

**Amazon Rekognition** is a fully managed computer vision service that enables you to analyze images and videos for object detection, facial analysis, text recognition, and more. It offers pre-trained models and supports custom label training to identify specific objects or scenes relevant to your business needs. Rekognition can process both stored and streaming content, making it suitable for a wide range of applications.

---

## Why should I care?

- **No ML Expertise Required**: Utilize powerful computer vision capabilities without building or training models.
- **Scalable and Cost-Effective**: Automatically scales to handle large volumes of data with pay-as-you-go pricing.
- **Real-Time Analysis**: Analyze live video streams for immediate insights.
- **Customizable**: Train models to detect custom objects specific to your use case.

---

## When to use it

- Implementing facial recognition for user verification.
- Moderating user-generated content to detect inappropriate imagery.
- Extracting text from images for indexing or compliance purposes.
- Monitoring live video feeds for specific objects or activities.

---

## Key features

- **Face Detection and Analysis**: Identify faces and analyze attributes like emotions, age range, and facial landmarks.
- **Object and Scene Detection**: Recognize thousands of objects, scenes, and activities in images and videos.
- **Text Detection**: Extract printed and handwritten text from images and videos.
- **Content Moderation**: Detect explicit or suggestive content to maintain safe environments.
- **Celebrity Recognition**: Identify celebrities in images and videos.
- **Custom Labels**: Train models to detect specific objects or scenes unique to your application.

---

## Common use cases

- **Security and Surveillance**: Monitor live feeds for unauthorized access or specific activities.
- **Retail Analytics**: Analyze shopper behavior and demographics.
- **Media and Entertainment**: Automate metadata tagging and content moderation.
- **Healthcare**: Ensure compliance by detecting protected health information in images.

---

## Integrations

- **Amazon S3**: Store and retrieve images and videos for analysis.
- **AWS Lambda**: Trigger analysis workflows in response to events.
- **Amazon Kinesis Video Streams**: Process live video streams in real-time.
- **Amazon SageMaker**: Develop and deploy custom ML models alongside Rekognition.
- **Amazon CloudWatch**: Monitor and log Rekognition operations.

---

## Example: Detecting Labels in an Image with Boto3


```python
import boto3

# Create a Rekognition client
rekognition = boto3.client('rekognition')

# Specify the S3 bucket and image
response = rekognition.detect_labels(
    Image={
        'S3Object': {
            'Bucket': 'your-bucket-name',
            'Name': 'your-image.jpg'
        }
    },
    MaxLabels=10,
    MinConfidence=75
)

# Print detected labels
for label in response['Labels']:
    print(f"{label['Name']} : {label['Confidence']:.2f}%")
```


---

## Learn More

- [Amazon Rekognition Documentation](https://docs.aws.amazon.com/rekognition/)
- [Amazon Rekognition Developer Guide](https://docs.aws.amazon.com/rekognition/latest/dg/what-is.html)
- [Amazon Rekognition FAQs](https://aws.amazon.com/rekognition/faqs/)
- [Amazon Rekognition Pricing](https://aws.amazon.com/rekognition/pricing/)
