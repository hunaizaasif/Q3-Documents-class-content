Hello world for beginners 
In easy steps
# Step 1 install packages and dependencies  (all packages run and add through cmd)
# Uv init hello_agent (create Prject)
# Cd hello_agent (goto project folder)
# Uv add openai-agents python-dotenv (install package)
# .venv\Scripts\activate (Activate environment)
# Uv run hello_agent.py (run your Code)
# Step 2: open VS code and import some module like
### (for get file from vs code)
import os 
### (for making  main function awaited)
import asyncio 
### (for accessing key)
from dotenv  import  load_dotenv 
from agents import Agent, AsyncOpenAI, OpenAIChatCompletionsModel, Runner

# Step 3 create .env file in present folder ie in “hello_agent”
# 1.    Past api key like this: in .env file
# GEMINI_API_KEY=AIzaSyCcK_j4fbz*************W5d9k
# Step 4: Now building you main code 
    # Code:  
load_dotenv()
    ## Now set Api key
gemini_api_key = os.getenv("GEMINI_API_KEY")
    ## create external Client using AsyncOpenAI() and it required two (2) parameter
# (i)    Api_key     (ii)     base_url
External_client = AsyncOpenAI (
        api_key = gemini_api_key ,
        base_url = "https://generativelanguage.googleapis.com/v1beta/openai" )
### Now Create Model OpenAIChatCompletiosModel() : it take two parameter model and openai_client
model =OpenAIChatCompletionsModel (
        model = "gemini-2.0-flash",
        openai_client = External_client )
    ### now Create Agent in Main function
async def main():
        agent = Agent (
            name = "Assistant",
            instructions = "reply the query answer",
            model = model )
    ### Now final code for output or result 
        Result = await Runner.run(agent, "hello how are you??")
        print(Result.final_output)
if __name__ == "__main__":
        asyncio.run(main())

        Attachment file type: acrobat
Step 1 install packages and dependencies(2)(1).pdf
31.22 KB
        
