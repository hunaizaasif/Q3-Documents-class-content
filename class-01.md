### Agentic AI - Class:01 [31-May-2025]

##  Topics Covered: 

We worked on the following resources during class:

https://github.com/panaversity/learn-agentic-ai/blob/main/01_ai_agents_first/04_hello_agent/hello_agent.ipynb  
https://openai.github.io/openai-agents-python/models/litellm/ 

###  Gemini API Key: 

To generate your **Gemini API Key** go to https://makersuite.google.com/app

### litellm code:

https://colab.research.google.com/drive/1dz1lViKhXBJCMyv40zH4pAc90P1LVP-m?usp=sharing

##  Class Code
from dotenv import load_dotenv
import os
from agents import AsyncOpenAI, OpenAIChatCompletionsModel, Agent, Runner, RunConfig
import asyncio


load_dotenv()


async def main():
    MODEL_NAME = "gemini-2.0-flash"
    GEMINI_API_KEY = os.getenv("GEMINI_API_KEY")

    external_client = AsyncOpenAI(
        api_key=GEMINI_API_KEY,
        base_url="https://generativelanguage.googleapis.com/v1beta/openai/"
    )

    model = OpenAIChatCompletionsModel(
        model=MODEL_NAME,
        openai_client=external_client
    )

    config = RunConfig(
        model=model,
        model_provider=external_client,
        tracing_disabled=True
    )

    assistant = Agent(
        name="Assistant",
        instructions="Your job is to resolve queries",
        # model=model
    )

    result = await Runner.run(assistant, "tell me something interesting about Pakistan.", run_config=config)

    print(result.final_output)


if __name__ == "__main__":
    asyncio.run(main())

    https://discord.com/channels/1352950461883482172/1376559198623760474/1378294037630550148

    https://discord.com/channels/1352950461883482172/1376559198623760474/1378312025754570854
