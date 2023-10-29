
### Overview

This repository contains code for an interactive text-based adventure game called "Temporal Traverse." Players will navigate a character named Alex through various time periods, making choices that determine the narrative's path and, ultimately, Alex's fate. The game is powered by Cassandra for chat history and AI-based language model from OpenAI to generate responses.

### Requirements

-   Python 3.x
-   A Cassandra cluster (or use AstraDB) to store chat history
-   OpenAI API key for language generation


### Setup

1.  **Cassandra Configuration**
    
    -   Ensure you have a Cassandra cluster or AstraDB set up. Update the `cloud_config` variable with the appropriate credentials in the code.
    -   Replace `secure-connect-choose-your-adventure.zip` with the bundle corresponding to your Cassandra or AstraDB setup.
2.  **Environment Variables**
    
    -   Store your Cassandra and OpenAI credentials in a file named `token.json`.
    -   Set up a `.env` file and add the `OPENAI_API_KEY` variable.
3.  **OpenAI API Key**
    
    -   To provision an OpenAI API key, visit [OpenAI's website](https://platform.openai.com/account/api-keys) and create an API key. Insert this key as the value for `OPENAI_API_KEY` in your `.env` file.
4.  **Vector Database Provisioning**
    
    -   This game uses Cassandra for chat history storage, but you can also integrate a Vector Database for advanced functionalities. Provision a Vector Database for an additional data layer to support complex data queries and analysis.
5.  **Game Rules and Narrative**
    
    -   The game's narrative and rules are defined within the Python script. Players will guide Alex through the Temporal Traverse, making decisions that impact the storyline. The game ends when a path leads to "The End."

### How to Play

1.  **Execution**
    
    -   Run the Python script to start the game.
    
    bashCopy code
    
    `python connect-database.py` 
    
2.  **Gameplay**
    
    -   The game initiates by choosing a time-travel device for transportation.
    -   Players will encounter decision points where they must make choices, each affecting the story's direction.
    -   After three decision points, paths leading to potential character death are presented, and the game ends upon encountering "The End."

### Chat History and AI Model

The game utilizes a chat history stored in Cassandra through `CassandraChatMessageHistory`. This context aids the AI model (LLMChain) from OpenAI to generate responses based on the player's input and the established narrative template.

### Contribution

Contributions are welcome! If you wish to enhance the game, feel free to fork the repository and submit a pull request with your changes.

### Licensing

This project is licensed under MIT License. Feel free to modify and distribute it as per the license terms.

### Disclaimer

This game is a demonstration and should be used responsibly. The AI-generated content might not always follow a predictable or desired path due to its learning nature.

Thank you for checking out the Temporal Traverse Adventure Game repository. Enjoy your journey through time and storytelling! If you have any queries or suggestions, feel free to reach out or create an issue in the repository.