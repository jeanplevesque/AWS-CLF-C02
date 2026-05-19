---
name: aws-service-docs
description: 'Research the latest official AWS service overview and feature information from aws.amazon.com. Use when you need a current summary, key capabilities, differentiation notes, or CLF-C02 study updates for an AWS service. Fetch both the product page and the features page when available.'
argument-hint: 'AWS service name or aws.amazon.com slug, for example: ec2, lambda, amazon-s3, or Amazon DynamoDB'
user-invocable: true
---

# AWS Service Docs

## What This Skill Does

This skill gathers the latest public information for an AWS service from official AWS marketing and product pages, then turns it into a concise, study-ready summary.

Primary sources:
- `https://aws.amazon.com/SERVICE_NAME/`
- `https://aws.amazon.com/SERVICE_NAME/features/`

Use this skill when the goal is to understand what a service does now, what AWS highlights as key features, and how to describe it briefly without relying on third-party summaries.

## When to Use

- You need the latest official AWS description for a service.
- You need to update study notes or a comparison table with current AWS wording and capabilities.
- You need quick differentiation notes between similar AWS services.
- You want current feature highlights from AWS without browsing manually.

## Inputs

Provide one of the following:
- AWS product slug, such as `ec2`, `s3`, `lambda`, or `dynamodb`
- Official product name, such as `Amazon EC2`, `Amazon S3`, or `AWS Lambda`

## Procedure

1. Normalize the service identifier.
   - If the input is already an AWS slug, use it directly.
   - If the input is a product name, resolve the likely slug from the official naming.
   - Keep the current official product name from the page heading, even if the user used an older or shorthand name.

2. Read the official AWS product page.
   - Fetch `https://aws.amazon.com/SERVICE_NAME/`.
   - Extract the current one-sentence product description.
   - Capture the primary use case, service category, and any positioning language that explains who the service is for.

3. Read the official AWS features page.
   - Fetch `https://aws.amazon.com/SERVICE_NAME/features/`.
   - Extract the major capabilities or feature groups AWS emphasizes.
   - Note feature wording that helps distinguish the service from adjacent services.

4. Reconcile naming and scope.
   - If the product page and features page use slightly different names, prefer the current official page heading.
   - If the features page redirects, is missing, or is not service-specific, state that explicitly and use only the product page.
   - If the service has been renamed or repositioned, mention the current official name and the older name only when that helps avoid confusion.

5. Produce a concise output.
   - One short summary sentence.
   - Three to six key capabilities or feature bullets.
   - Optional differentiation notes for nearby services when the distinction matters.
   - The date checked.
   - The AWS URLs used.

6. If updating CLF-C02 study material, keep the wording exam-focused.
   - Prefer simple descriptions over marketing phrasing.
   - Focus on what the service does, the workload it fits, and what makes it different.
   - Compress the result so it can fit into a study table cell or a short note.

## Decision Points

### If the Input Is Ambiguous

- Ask which service the user means when the name can map to more than one AWS product.
- If the repo already uses a specific official name, match that name in the output.

### If the Features Page Is Missing or Weak

- Use the product page as the primary source.
- Supplement only with closely related official AWS page content if needed.
- Call out that the standard `/features/` endpoint was unavailable or low-value.

### If the Service Is Similar to Another Service

- Add a short “how to tell it apart” note.
- Keep the comparison narrow and exam-relevant.

## Output Template

Use this shape unless the user asks for a different format:

```markdown
Service: <official AWS product name>
Checked: <YYYY-MM-DD>
Sources:
- https://aws.amazon.com/SERVICE_NAME/
- https://aws.amazon.com/SERVICE_NAME/features/

Short description: <one sentence>

Key capabilities:
- <capability>
- <capability>
- <capability>

How to tell it apart:
- <short differentiation note>
```

## Quality Checks

- Use official AWS pages first.
- Try both the product page and the features page.
- Preserve current official naming.
- Paraphrase instead of copying long AWS text blocks.
- Keep summaries concise and accurate.
- Include the date checked and the exact URLs used.
- State any uncertainty, redirects, or missing feature pages.

## Example Prompts

- `/aws-service-docs lambda`
- `/aws-service-docs Amazon DynamoDB`
- `/aws-service-docs route-53`
- `/aws-service-docs Compare AWS PrivateLink and Transit Gateway for CLF-C02 notes`