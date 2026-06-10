# AIBootCamp-Task2B
# Day 2 Lab 2B - Resume Extractor

## Objective

Extract structured resume data using Gemini and validate it using Pydantic.

## Errors Handled

### 1. Markdown Fence Wrapping

Sometimes Gemini returns:

```json
{}
```

instead of raw JSON.

Retry logic fixes this.

### 2. Missing Phone Number

Phone is defined as:

```python
Optional[str] = None
```

Therefore resumes without a phone number still validate.

### 3. Empty Input

Pydantic raises ValidationError when required fields are missing.

The exception is caught gracefully.

## Results

Successfully processed 3 sample resumes using Gemini structured output.

## Technologies Used

* Gemini 2.5 Flash
* Google GenAI SDK
* Pydantic
* Google Colab
