# Amazon Comprehend Developer Guide

-----
*****Copyright &copy; Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What Is Amazon Comprehend?](what-is.md)
+ [How It Works](how-it-works.md)
   + [Languages Supported in Amazon Comprehend](supported-languages.md)
+ [Tutorial: Analyzing Insights from Customer Reviews with Amazon Comprehend](tutorial-reviews.md)
   + [Step 1: Adding Documents to Amazon S3](tutorial-reviews-add-docs.md)
   + [Step 2: (CLI Only) Creating an IAM Role for Amazon Comprehend](tutorial-reviews-create-role.md)
   + [Step 3: Running Analysis Jobs on Documents in Amazon S3](tutorial-reviews-analysis.md)
   + [Step 4: Preparing the Amazon Comprehend Output for Data Visualization](tutorial-reviews-tables.md)
   + [Step 5: Visualizing Amazon Comprehend Output in Amazon QuickSight](tutorial-reviews-visualize.md)
+ [Getting Started with Amazon Comprehend](getting-started.md)
   + [Step 1: Set Up an AWS Account and Create an Administrator User](setting-up.md)
   + [Step 2: Set Up the AWS Command Line Interface (AWS CLI)](setup-awscli.md)
   + [Step 3: Getting Started Using the Amazon Comprehend Console](get-started-console.md)
      + [Analyzing Documents Using the Console](get-started-console-analysis.md)
      + [Creating and Using Custom Entity Recognizer](getting-started-custom-entity-recognizer.md)
      + [Creating and Using Custom Classifiers](getting-started-document-classification.md)
         + [Creating a Custom Classifier (Console)](getting-started-console-classifier.md)
         + [Running an Asynchronous Custom Classification Job](getting-started-console-classification.md)
         + [Creating a Real-time Custom Classification Request](getting-started-console-endpoint.md)
      + [Model Versioning with Amazon Comprehend](model-versioning.md)
      + [Creating a Topic Modeling Job Using the Console](getting-started-console-topics.md)
      + [Creating an Events Detection Job Using the Console](getting-started-console-events.md)
   + [Step 4: Getting Started Using the Amazon Comprehend API](get-started-api.md)
      + [Detecting the Dominant Language](get-started-api-dominant-language.md)
      + [Detecting Named Entities](get-started-api-entities.md)
      + [Detecting Key Phrases](get-started-api-key-phrases.md)
      + [Detecting Personally Identifiable Information (PII)](get-started-api-pii.md)
      + [Labeling Documents with Personally Identifiable Information (PII)](get-started-api-pii-labels.md)
      + [Detecting Sentiment](get-started-api-sentiment.md)
      + [Detecting Syntax](get-started-api-syntax.md)
      + [Using Custom Classification](get-started-customclass.md)
      + [Detecting Custom Entities](get-started-cer.md)
      + [Detecting Events](get-started-api-events.md)
      + [Topic Modeling](get-started-topics.md)
      + [Using the Batch APIs](get-started-batch.md)
   + [Solution: Analyzing Text with Amazon Comprehend and Amazon Elasticsearch Service](elasticsearch.md)
+ [Using Amazon S3 Object Lambda Access Points for Personally Identifiable Information (PII)](using-access-points.md)
   + [Controlling Access to Documents with Personally Identifiable Information (PII)](access-point-pii-control.md)
   + [Redacting Personally Identifiable Information (PII) from Documents](access-point-pii-redact.md)
+ [Text Analysis APIs](functionality.md)
   + [Detect Entities](how-entities.md)
   + [Detect Events](how-events.md)
   + [Detect Key Phrases](how-key-phrases.md)
   + [Detect the Dominant Language](how-languages.md)
   + [Detect Personally Identifiable Information (PII)](how-pii.md)
   + [Label Documents with Personally Identifiable Information (PII)](how-pii-labels.md)
   + [Determine Sentiment](how-sentiment.md)
   + [Analyze Syntax](how-syntax.md)
   + [Topic Modeling](topic-modeling.md)
+ [Document Processing Modes](process.md)
   + [Single-Document Processing](how-single.md)
   + [Asynchronous Batch Processing](how-async.md)
   + [Multiple Document Synchronous Processing](how-batch.md)
+ [Comprehend Custom](auto-ml.md)
   + [Custom Classification](how-document-classification.md)
      + [Training a Custom Classifier](how-document-classification-training.md)
         + [Creating Training Data](how-document-classification-training-data.md)
         + [Multi-Class Mode](how-document-classification-training-multi-class.md)
         + [Multi-Label Mode](how-document-classification-training-multi-label.md)
         + [Testing the Training Data](testing-the-model.md)
      + [Running an Asynchronous Classification Job](how-class-run.md)
      + [Real-time Analysis with Custom Classification](custom-sync.md)
         + [Creating an Endpoint for Custom Classification](create-endpoint.md)
         + [Running Real-Time Custom Classification](cc-real-time-analysis.md)
      + [Tagging Custom Classifiers](class-tagging.md)
      + [Custom Classifier Metrics](cer-doc-class.md)
         + [Confusion Matrix](conf-matrix.md)
   + [Custom Entity Recognition](custom-entity-recognition.md)
      + [Training Custom Entity Recognizers](training-recognizers.md)
         + [Annotations](cer-annotation.md)
         + [PDF Annotations](pdf-word-annotation.md)
         + [Annotation Best Practices](annotation-best-practices.md)
         + [Entity Lists (Plain Text Only)](cer-entity-list.md)
      + [Detecting Custom Entities with an Asynchronous Batch Job with Amazon Comprehend](detecting-cer.md)
      + [Detecting Custom Entities in Real Time with Amazon Comprehend](detecting-cer-real-time.md)
      + [Tagging Custom Entity Recognizers](CER-tagging.md)
      + [Custom Entity Recognizer Metrics](cer-metrics.md)
   + [Managing Endpoints with Amazon Comprehend](manage-endpoints.md)
      + [Endpoints Overview with Amazon Comprehend](manage-endpoints-overview.md)
      + [Monitoring an Endpoint with Amazon Comprehend](manage-endpoints-monitor.md)
      + [Updating an Endpoint with Amazon Comprehend](manage-endpoints-update.md)
      + [Using Trusted Advisor with Amazon Comprehend](manage-endpoints-trusted-advisor.md)
      + [Deleting an Endpoint with Amazon Comprehend](manage-endpoints-delete.md)
      + [Auto Scaling with Endpoints](comprehend-autoscaling.md)
         + [Target Tracking](targettracking.md)
         + [Scheduled Scaling](ScheduledScaling.md)
+ [Security in Amazon Comprehend](comp-security.md)
   + [Data Protection in Amazon Comprehend](comp-data-protection.md)
      + [KMS Encryption in Amazon Comprehend](kms-in-comprehend.md)
      + [Protect Jobs by Using an Amazon Virtual Private Cloud](usingVPC.md)
      + [Amazon Comprehend and interface VPC endpoints (AWS PrivateLink)](vpc-interface-endpoints.md)
   + [Authentication and Access Control for Amazon Comprehend](auth-and-access-control.md)
      + [Overview of Managing Access Permissions to Amazon Comprehend Resources](access-control-overview.md)
      + [Using Identity-Based Policies (IAM Policies) for Amazon Comprehend](access-control-managing-permissions.md)
      + [Amazon Comprehend API Permissions: Actions, Resources, and Conditions Reference](comprehend-api-permissions-ref.md)
      + [AWS Managed Policies for Amazon Comprehend](security-iam-awsmanpol.md)
   + [Logging Amazon Comprehend API Calls with AWS CloudTrail](logging-using-cloudtrail.md)
   + [Compliance Validation for Amazon Comprehend](comp-compliance.md)
   + [Resilience in Amazon Comprehend](comp-disaster-recovery-resiliency.md)
   + [Infrastructure Security in Amazon Comprehend](comp-infrastructure-security.md)
   + [Permissions Required for a Custom Asynchronous Analysis Job](tagging-resources.md)
+ [Guidelines and Quotas](guidelines-and-limits.md)
+ [API Reference](API_Reference.md)
   + [Actions](API_Operations.md)
      + [BatchDetectDominantLanguage](API_BatchDetectDominantLanguage.md)
      + [BatchDetectEntities](API_BatchDetectEntities.md)
      + [BatchDetectKeyPhrases](API_BatchDetectKeyPhrases.md)
      + [BatchDetectSentiment](API_BatchDetectSentiment.md)
      + [BatchDetectSyntax](API_BatchDetectSyntax.md)
      + [ClassifyDocument](API_ClassifyDocument.md)
      + [ContainsPiiEntities](API_ContainsPiiEntities.md)
      + [CreateDocumentClassifier](API_CreateDocumentClassifier.md)
      + [CreateEndpoint](API_CreateEndpoint.md)
      + [CreateEntityRecognizer](API_CreateEntityRecognizer.md)
      + [DeleteDocumentClassifier](API_DeleteDocumentClassifier.md)
      + [DeleteEndpoint](API_DeleteEndpoint.md)
      + [DeleteEntityRecognizer](API_DeleteEntityRecognizer.md)
      + [DescribeDocumentClassificationJob](API_DescribeDocumentClassificationJob.md)
      + [DescribeDocumentClassifier](API_DescribeDocumentClassifier.md)
      + [DescribeDominantLanguageDetectionJob](API_DescribeDominantLanguageDetectionJob.md)
      + [DescribeEndpoint](API_DescribeEndpoint.md)
      + [DescribeEntitiesDetectionJob](API_DescribeEntitiesDetectionJob.md)
      + [DescribeEntityRecognizer](API_DescribeEntityRecognizer.md)
      + [DescribeEventsDetectionJob](API_DescribeEventsDetectionJob.md)
      + [DescribeKeyPhrasesDetectionJob](API_DescribeKeyPhrasesDetectionJob.md)
      + [DescribePiiEntitiesDetectionJob](API_DescribePiiEntitiesDetectionJob.md)
      + [DescribeSentimentDetectionJob](API_DescribeSentimentDetectionJob.md)
      + [DescribeTopicsDetectionJob](API_DescribeTopicsDetectionJob.md)
      + [DetectDominantLanguage](API_DetectDominantLanguage.md)
      + [DetectEntities](API_DetectEntities.md)
      + [DetectKeyPhrases](API_DetectKeyPhrases.md)
      + [DetectPiiEntities](API_DetectPiiEntities.md)
      + [DetectSentiment](API_DetectSentiment.md)
      + [DetectSyntax](API_DetectSyntax.md)
      + [ListDocumentClassificationJobs](API_ListDocumentClassificationJobs.md)
      + [ListDocumentClassifiers](API_ListDocumentClassifiers.md)
      + [ListDocumentClassifierSummaries](API_ListDocumentClassifierSummaries.md)
      + [ListDominantLanguageDetectionJobs](API_ListDominantLanguageDetectionJobs.md)
      + [ListEndpoints](API_ListEndpoints.md)
      + [ListEntitiesDetectionJobs](API_ListEntitiesDetectionJobs.md)
      + [ListEntityRecognizers](API_ListEntityRecognizers.md)
      + [ListEntityRecognizerSummaries](API_ListEntityRecognizerSummaries.md)
      + [ListEventsDetectionJobs](API_ListEventsDetectionJobs.md)
      + [ListKeyPhrasesDetectionJobs](API_ListKeyPhrasesDetectionJobs.md)
      + [ListPiiEntitiesDetectionJobs](API_ListPiiEntitiesDetectionJobs.md)
      + [ListSentimentDetectionJobs](API_ListSentimentDetectionJobs.md)
      + [ListTagsForResource](API_ListTagsForResource.md)
      + [ListTopicsDetectionJobs](API_ListTopicsDetectionJobs.md)
      + [StartDocumentClassificationJob](API_StartDocumentClassificationJob.md)
      + [StartDominantLanguageDetectionJob](API_StartDominantLanguageDetectionJob.md)
      + [StartEntitiesDetectionJob](API_StartEntitiesDetectionJob.md)
      + [StartEventsDetectionJob](API_StartEventsDetectionJob.md)
      + [StartKeyPhrasesDetectionJob](API_StartKeyPhrasesDetectionJob.md)
      + [StartPiiEntitiesDetectionJob](API_StartPiiEntitiesDetectionJob.md)
      + [StartSentimentDetectionJob](API_StartSentimentDetectionJob.md)
      + [StartTopicsDetectionJob](API_StartTopicsDetectionJob.md)
      + [StopDominantLanguageDetectionJob](API_StopDominantLanguageDetectionJob.md)
      + [StopEntitiesDetectionJob](API_StopEntitiesDetectionJob.md)
      + [StopEventsDetectionJob](API_StopEventsDetectionJob.md)
      + [StopKeyPhrasesDetectionJob](API_StopKeyPhrasesDetectionJob.md)
      + [StopPiiEntitiesDetectionJob](API_StopPiiEntitiesDetectionJob.md)
      + [StopSentimentDetectionJob](API_StopSentimentDetectionJob.md)
      + [StopTrainingDocumentClassifier](API_StopTrainingDocumentClassifier.md)
      + [StopTrainingEntityRecognizer](API_StopTrainingEntityRecognizer.md)
      + [TagResource](API_TagResource.md)
      + [UntagResource](API_UntagResource.md)
      + [UpdateEndpoint](API_UpdateEndpoint.md)
   + [Data Types](API_Types.md)
      + [AugmentedManifestsListItem](API_AugmentedManifestsListItem.md)
      + [BatchDetectDominantLanguageItemResult](API_BatchDetectDominantLanguageItemResult.md)
      + [BatchDetectEntitiesItemResult](API_BatchDetectEntitiesItemResult.md)
      + [BatchDetectKeyPhrasesItemResult](API_BatchDetectKeyPhrasesItemResult.md)
      + [BatchDetectSentimentItemResult](API_BatchDetectSentimentItemResult.md)
      + [BatchDetectSyntaxItemResult](API_BatchDetectSyntaxItemResult.md)
      + [BatchItemError](API_BatchItemError.md)
      + [ClassifierEvaluationMetrics](API_ClassifierEvaluationMetrics.md)
      + [ClassifierMetadata](API_ClassifierMetadata.md)
      + [DocumentClass](API_DocumentClass.md)
      + [DocumentClassificationJobFilter](API_DocumentClassificationJobFilter.md)
      + [DocumentClassificationJobProperties](API_DocumentClassificationJobProperties.md)
      + [DocumentClassifierFilter](API_DocumentClassifierFilter.md)
      + [DocumentClassifierInputDataConfig](API_DocumentClassifierInputDataConfig.md)
      + [DocumentClassifierOutputDataConfig](API_DocumentClassifierOutputDataConfig.md)
      + [DocumentClassifierProperties](API_DocumentClassifierProperties.md)
      + [DocumentClassifierSummary](API_DocumentClassifierSummary.md)
      + [DocumentLabel](API_DocumentLabel.md)
      + [DocumentReaderConfig](API_DocumentReaderConfig.md)
      + [DominantLanguage](API_DominantLanguage.md)
      + [DominantLanguageDetectionJobFilter](API_DominantLanguageDetectionJobFilter.md)
      + [DominantLanguageDetectionJobProperties](API_DominantLanguageDetectionJobProperties.md)
      + [EndpointFilter](API_EndpointFilter.md)
      + [EndpointProperties](API_EndpointProperties.md)
      + [EntitiesDetectionJobFilter](API_EntitiesDetectionJobFilter.md)
      + [EntitiesDetectionJobProperties](API_EntitiesDetectionJobProperties.md)
      + [Entity](API_Entity.md)
      + [EntityLabel](API_EntityLabel.md)
      + [EntityRecognizerAnnotations](API_EntityRecognizerAnnotations.md)
      + [EntityRecognizerDocuments](API_EntityRecognizerDocuments.md)
      + [EntityRecognizerEntityList](API_EntityRecognizerEntityList.md)
      + [EntityRecognizerEvaluationMetrics](API_EntityRecognizerEvaluationMetrics.md)
      + [EntityRecognizerFilter](API_EntityRecognizerFilter.md)
      + [EntityRecognizerInputDataConfig](API_EntityRecognizerInputDataConfig.md)
      + [EntityRecognizerMetadata](API_EntityRecognizerMetadata.md)
      + [EntityRecognizerMetadataEntityTypesListItem](API_EntityRecognizerMetadataEntityTypesListItem.md)
      + [EntityRecognizerProperties](API_EntityRecognizerProperties.md)
      + [EntityRecognizerSummary](API_EntityRecognizerSummary.md)
      + [EntityTypesEvaluationMetrics](API_EntityTypesEvaluationMetrics.md)
      + [EntityTypesListItem](API_EntityTypesListItem.md)
      + [EventsDetectionJobFilter](API_EventsDetectionJobFilter.md)
      + [EventsDetectionJobProperties](API_EventsDetectionJobProperties.md)
      + [InputDataConfig](API_InputDataConfig.md)
      + [KeyPhrase](API_KeyPhrase.md)
      + [KeyPhrasesDetectionJobFilter](API_KeyPhrasesDetectionJobFilter.md)
      + [KeyPhrasesDetectionJobProperties](API_KeyPhrasesDetectionJobProperties.md)
      + [OutputDataConfig](API_OutputDataConfig.md)
      + [PartOfSpeechTag](API_PartOfSpeechTag.md)
      + [PiiEntitiesDetectionJobFilter](API_PiiEntitiesDetectionJobFilter.md)
      + [PiiEntitiesDetectionJobProperties](API_PiiEntitiesDetectionJobProperties.md)
      + [PiiEntity](API_PiiEntity.md)
      + [PiiOutputDataConfig](API_PiiOutputDataConfig.md)
      + [RedactionConfig](API_RedactionConfig.md)
      + [SentimentDetectionJobFilter](API_SentimentDetectionJobFilter.md)
      + [SentimentDetectionJobProperties](API_SentimentDetectionJobProperties.md)
      + [SentimentScore](API_SentimentScore.md)
      + [SyntaxToken](API_SyntaxToken.md)
      + [Tag](API_Tag.md)
      + [TopicsDetectionJobFilter](API_TopicsDetectionJobFilter.md)
      + [TopicsDetectionJobProperties](API_TopicsDetectionJobProperties.md)
      + [VpcConfig](API_VpcConfig.md)
   + [Common Errors](CommonErrors.md)
   + [Common Parameters](CommonParameters.md)
+ [Document History for Amazon Comprehend](doc-history.md)