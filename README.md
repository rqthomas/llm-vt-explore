# Demo using an LLM for coding

## Setting up before the tutorial

The setup involves obtaining your credentials to access Virginia Tech's LLM service and running the tutorial in a Docker container.  We are using a Docker container so the LLM agent doesn't accidentally edit or delete files on your computer without your explicit instructions.

### Docker
1. Download Docker Desktop if you haven't already downloaded it.  If you already have Docker Desktop, update it to the latest version.
2. Launch Docker Desktop from your computer's applications.
3. In your terminal or PowerShell, run: 
```
docker run --rm -ti -e PASSWORD=yourpassword -p 8787:8787 rocker/tidyverse
```
This may take a while to download the Docker image.


4. To launch an instance of RStudio that is running in the Docker container (thus isolated from the rest of your computer), open a web browser and type
```
http://localhost:8787
```
5. [In RStudio in your browser] Log into RStudio with: User name = "rstudio", Password = "yourpassword"

### LLM Credentials

6. If not on campus, log into the university VPN.
7. Go to <https://llm.arc.vt.edu>
8. In the bottom left is the settings menu.  Click it and click "Settings".  Click "Account".  In "Account", click "API keys" and create a secret key if you don't already have one. Copy the key — you'll need it in step 10.

### In RStudio  

9. [In RStudio in your browser] Create a new project with version control (Git) using this repo (`https://github.com/rqthomas/llm-vt-explore`). 

10. [In RStudio in your browser] Create a new "File -> Text file"  called ".Renviron".  Add this line to the file and save it to the home directory (one directory up from the `llm-vt-explore` directory).  It should not be in the `llm-vt-explore` directory so the LLM doesn't read it.
```
OPENAI_API_KEY = "PASTE YOUR API KEY FROM STEP 8"
```

11. [In the RStudio in your browser] Install the `ellmer` package: 
```
remotes::install_github("tidyverse/ellmer")
```

## Next steps

Open and work through `simple-coding-agent.qmd`
