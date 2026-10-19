# Reflection

## Where Codex struggled

The first dependency setup used Codex’s bundled Python rather than the Python installation I use in VS Code. Although packages installed, the resulting venv was not available as the notebook kernel I needed. I clarified the interpreter path and asked Codex to recreate the environment with my installed Python 3.12.4, then install the packages and register the Ames Week 7 kernel. At first this was very difficult to understand, but most of it has to do with the CLI itself because it's just not that easy to read compared to what im used to with calude code or using the Codex gui. Once we figured out it was a bundled python problem i just had it reinstall the venv with my interper. Other than that, I did not have many issues with Codex at all during this, it was pretty good but it did seem to take longer than i am used to to write code compared to claude code.

## How my prompts evolved

My prompts started with a larger initial prompt to help with the setup to ensure the follow on instructions were more easily received and did what i needed them to do without using too many tokens. Once i realized that the wireframe was laid out a little too granularly i started having it bundle like-tasks together to avoid constant prompting and confirmations. Overall my prompts did not have to change much sicne the initial instruictions were easy given i have the entire assignment and rubric available.

## What I would do differently
I think next time i would just set up the venv ahead of time to avoid the package conflcits i was frustrated with at first, and then prompt it to use it appropriately. I also would just not prefer the CLI over the codex gui, I am actually unsure why anyone would use the CLI over the gui given how much easier it is to read the text on the normal codex tab within the chatgpt desktop app. I have had a lot of experience coding with AI already so a lot of my lessons learned admittedly i already have dealt with prior to this assignment. Some examples of that woudl be prompting compelte instreuctions and writing down a plan beforehand instead of just winging the project like i had done in the past. A lot of good lessons learned I've had with AI over the last couple of years has been that specificity is key. You have to be specific and if you have a plan before using the tool it is just far more streamlined, this makes more and more sense the more you understand how LLMs work.

