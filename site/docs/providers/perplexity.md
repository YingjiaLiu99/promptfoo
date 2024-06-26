# Perplexity

The [Perplexity API](https://blog.perplexity.ai/blog/introducing-pplx-api) (pplx-api) offers access to Perplexity, Mistral, Llama, and other models.

It is compatible with the [OpenAI API](/docs/providers/openai). In order to use the Perplexity API in an eval, set the `apiHost` config key to `api.perplexity.ai`.

Here's an example config that compares Perplexity's large and small Llama 3 online models:

```yaml
providers:
  - id: openai:chat:llama-3-sonar-large-32k-online
    config:
      apiHost: api.perplexity.ai
      apiKeyEnvar: PERPLEXITY_API_KEY
  - id: openai:chat:llama-3-sonar-small-32k-online
    config:
      apiHost: api.perplexity.ai
      apiKeyEnvar: PERPLEXITY_API_KEY
```

In this example, you'd have to set the `PERPLEXITY_API_KEY` environment variable (you can also enter it directly in the config using the `apiKey` property).

If desired, you can instead use the `OPENAI_API_HOST` environment variable instead of the `apiHost` config key.

For a complete list of supported models, see Perplexity's [chat completion documentation](https://docs.perplexity.ai/reference/post_chat_completions).
