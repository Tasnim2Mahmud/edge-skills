name: web-search
description: Search the internet for current information. Use this skill whenever the user asks about weather, news, facts, or any real-world data. Triggers on words like "search", "look up", "what is the weather", "find", "current", "latest", "today".
Web Search
Instructions
Call the run_js tool with the following exact parameters:
script name: index.html
data: A JSON string with the following fields:
query: Required. The search term or city name to look up.
type: Required. Use "weather" for weather queries, "wiki" for everything else.
Examples
User: "What's the weather in Dhaka?"
{ "query": "Dhaka", "type": "weather" }
User: "Search for quantum computing"
{ "query": "quantum computing", "type": "wiki" }
User: "Who is Albert Einstein?"
{ "query": "Albert Einstein", "type": "wiki" }
Constraints
Always extract the core topic or city name for the query field.
Remove filler words like "what is", "tell me about", "search for".
For weather, use only the city name.
Respond in the same language as the user's prompt.
Provide a concise 1-3 sentence summary of the result returned by the tool.
