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

✅ Semantic document search using vector embeddings
✅ AI-powered responses with source citations
✅ Query history tracking
✅ RESTful API interface
✅ Simple web UI

## Setup Instructions

[Link to your detailed guide or include abbreviated steps]

## API Usage

```bash
curl -X POST your-api-url/prod/query \
  -H "Content-Type: application/json" \
  -d '{"query": "Your question here"}'
```

## Cost Estimate

- **Bedrock**: ~$0.003 per 1K input tokens, ~$0.015 per 1K output tokens
- **OpenSearch Serverless**: ~$0.24/hour for OCU
- **Lambda**: Free tier covers most POC usage
- **S3**: Minimal for document storage
- **DynamoDB**: Free tier covers most POC usage

**Estimated monthly cost for POC**: $5-20 depending on usage

## Project Structure

```
aws-rag-knowledge-base-poc/
├── lambda/
│   └── query_processor.py
├── web/
│   └── index.html
├── docs/
│   └── SETUP_GUIDE.md
└── README.md
```

## Testing and Validation

Test these scenarios:

1. **Basic Query**: "What is covered in the policy?"
2. **Complex Query**: "Compare the deductibles for different claim types"
3. **Out-of-scope Query**: "What's the weather today?" (should indicate no relevant info)
4. **Follow-up Query**: Ask related questions to test context

## Monitoring

1. Go to **CloudWatch** in AWS Console
2. Click **Log groups**
3. Find `/aws/lambda/rag-query-processor`
4. Review logs for errors or performance issues

## Cost Optimization

### Set Up Billing Alerts

1. Go to **AWS Billing Console**
2. Click **Budgets** in left navigation
3. Click **Create budget**
4. Select **Cost budget**
5. Set amount: $20
6. Add email alert at 80% threshold
7. Click **Create budget**

### Optimization Tips

- Use **AWS Cost Explorer** to identify high-cost services
- Consider reducing OpenSearch OCU if not actively testing
- Delete test resources when not in use

## Cleanup Instructions

To avoid ongoing charges:

1. **Delete OpenSearch Collection**: OpenSearch Service → Serverless → Collections → Select → Delete
2. **Delete Knowledge Base**: Bedrock → Knowledge bases → Select → Delete
3. **Delete Lambda Function**: Lambda → Functions → Select → Actions → Delete
4. **Delete S3 Bucket**: S3 → Select bucket → Empty → Delete
5. **Delete DynamoDB Table**: DynamoDB → Tables → Select → Delete
6. **Delete API Gateway**: API Gateway → Select API → Actions → Delete
7. **Delete IAM Roles**: IAM → Roles → Search for created roles → Delete

## Next Steps and Enhancements

1. **Add authentication**: Implement API keys or Cognito
2. **Improve UI**: Build React/Vue frontend
3. **Add document upload**: Allow users to upload docs via UI
4. **Implement caching**: Use ElastiCache for frequent queries
5. **Add analytics**: Track popular queries and response quality
6. **Multi-language support**: Use translation services
7. **Streaming responses**: Implement real-time response streaming

## LinkedIn Post Template

🚀 Just built a RAG (Retrieval-Augmented Generation) system using AWS Bedrock!

This POC demonstrates how to create an AI-powered document Q&A system that:
✅ Searches documents semantically (not just keywords)
✅ Generates accurate answers with source citations
✅ Scales automatically with serverless architecture

**Tech stack**:
- Amazon Bedrock Knowledge Bases
- Claude 3 Sonnet
- OpenSearch Serverless (vector DB)
- AWS Lambda + API Gateway

The entire setup is documented step-by-step on GitHub, including:
- Complete architecture walkthrough
- Infrastructure setup guide
- Sample code and web interface
- Cost optimization tips

Check it out: [Your GitHub URL]

#AWS #AI #MachineLearning #RAG #Bedrock #CloudComputing #GenerativeAI

## Contributing

Contributions welcome! Please open an issue or submit a PR.

## License

MIT License
