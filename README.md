# AWS RAG Knowledge Base POC

A production-ready Retrieval-Augmented Generation (RAG) system built with AWS Bedrock Knowledge Bases, demonstrating semantic search over documents with AI-powered responses.

## Architecture

- **Amazon Bedrock**: Knowledge Base + Claude 3 Sonnet
- **Amazon OpenSearch Serverless**: Vector database
- **AWS Lambda**: Query processing
- **Amazon S3**: Document storage
- **Amazon DynamoDB**: Query history
- **API Gateway**: REST API endpoint

## Features

- ✅ Semantic document search using vector embeddings
- ✅ AI-powered responses with source citations
- ✅ Query history tracking
- ✅ RESTful API interface
- ✅ Simple web UI

## Setup Instructions

[Link to your detailed guide or include abbreviated steps]

## API Usage

```bash
curl -X POST your-api-url/prod/query \
  -H "Content-Type: application/json" \
  -d '{"query": "Your question here"}'
