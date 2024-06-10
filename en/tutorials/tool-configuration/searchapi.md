# SearchApi
SearchApi is a real-time SERP API that provides structured data from a variety of search engines, including Google Search, Google Shopping, Google Jobs, YouTube, Amazon, and more.

## 1. Retrieve SearchApi API Key
Sign up for a free account at [searchapi.io](https://www.searchapi.io/) to get your API key.

## 2. Use Google Search, Google News, Google Jobs, or YouTube Transcripts Tool
- Google Search, Google News, Google Jobs: These engines require a search query.
- YouTube Transcripts Tool: This tool requires a `video_id`.

The SearchAPI class allows you to query these tools and process the results.

### For Google searches, the results can include:

For `result_type=text`:
- `answer_box` (fields: `answer`, `snippet`)
- `knowledge_graph` (field: `description`)
- `organic_results` (fields: `snippet`, `link`)

For `result_type=link`:
- `answer_box` (field: `organic_result` with subfields `title`, `link`)
- `organic_results` (fields: `title`, `link`)
- `related_questions` (fields: `title`, `link`)
- `related_searches` (fields: `title`, `link`)

## Integrating a New SearchApi Engine
To integrate a new engine into SearchApi, follow these steps:

1. Copy the existing tool code.
2. Modify the `get_params` request parameters to suit the new engine.
3. Adjust `_process_response` to handle and return the response according to your needs.

By following these instructions, you can easily expand the functionality of the SearchApi to include new search engines and customize how the data is processed and returned.
