# AWS CDK S3 Bucket Creation

This project demonstrates how to create an S3 bucket with specific properties like versioning and encryption using the AWS Cloud Development Kit (AWS CDK).

## Overview

The AWS CDK is an open-source software development framework to define cloud infrastructure in code and provision it through AWS CloudFormation. This project focuses on creating an S3 bucket with enhanced security features and data retention policies.

## Features

- **Create S3 Bucket**: Set up a new S3 bucket on AWS.
- **Bucket Versioning**: Enable versioning to keep multiple versions of an object in the same bucket.
- **Bucket Encryption**: Apply encryption to secure the data stored in the bucket.
- **Removal Policy**: Define a removal policy for the bucket when the stack is deleted.

## Project Setup

In the CDK stack setup for this project, I've meticulously configured it to establish an Amazon S3 bucket endowed with several pivotal properties aimed at augmenting its functionality and security:

- **Bucket Creation:** The foundation of our configuration is the instantiation of a new Amazon S3 bucket. This vital storage resource facilitates the storage and retrieval of data objects. Designed to be globally unique within AWS, the bucket's name ensures its accessibility and distinctiveness.

- **Versioning Enabled:** A key feature activated for the S3 bucket is versioning. This functionality is instrumental in maintaining multiple variants of an object within the bucket, providing a robust framework for data retention and recovery. It enables the preservation, retrieval, and restoration of every version of every object stored, offering a safeguard against accidental deletions or modifications.

- **Encryption Management:** To secure the stored objects, the bucket is configured with S3-managed encryption (SSE-S3). This encryption method automatically secures your object before it is saved to the disk and decrypts it upon access. Managing encryption in this manner ensures the security of data at rest, protecting it against unauthorized access and aligning with industry best practices for data security.

- **Retention Policy on Stack Deletion:** An essential safety measure implemented is setting the bucket's retention policy to be retained even if the CDK stack is deleted. This policy is a critical safeguard against accidental data loss, ensuring that the deletion of the CDK stack does not result in the loss of the bucket and its contents. It underscores the importance of resource lifecycle management, especially in dynamic environments where resources are regularly updated or redeployed.

## Using CodeWhisperer for CDK Code Generation

During the development of this project, we utilized AWS CodeWhisperer to assist with generating CDK code snippets. This AI-powered pair programmer provided suggestions for complex code patterns and best practices, which enhanced the development workflow.

Specifically, CodeWhisperer was instrumental in generating the code necessary for implementing the removal policy and encryption for the S3 bucket. It suggested configurations that align with AWS best practices for security and resource management.

## Deployment

The image below shows the bucket was deployed.
![Deployed S3 Bucket](./images/hellocdk-s3-deployed.png)