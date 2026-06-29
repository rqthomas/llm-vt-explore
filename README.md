# LLM explore

## Setting up 

The set up involves getting your credentials for accessing Virginia Tech's LLM service and running the tutorial in a Docker container.  We are using a Docker container so that the LLM agent doesn't accidentally edit or remove files from your computer without your instructions.

1. If not on campus, log into the university VPN.
2. Go to <https://llm.arc.vt.edu>
3. In the bottom right is the settings menu.  Click it and click "Settings".  Click "Account".  In "Account", click "API keys" and create one if you don't already have one. Copy the key — you'll need it in step 9.

4. Download Docker Desktop if you haven't already downloaded it.
5. In your terminal or powershell, run 

```
docker run --rm -ti -e PASSWORD=yourpassword -p 8787:8787 rocker/tidyverse
```
6. Open a web browser and type
```
http://localhost:8787
```
7. User name = "rstudio", Password = "yourpassword"

8. Create a new project with version control using this repo (`rqthomas/llm-vt-explore`). 

9. Create a new "File -> Text file"  called ".Renviron".  Add this line to the file and save it to the home directory.  It should not be in the llm-vt-explore directory.  
```
OPENAI_API_KEY = "PASTE YOUR API KEY FROM STEP 3"
```

10. Install the ellmer package: 
```
remotes::install_github("tidyverse/ellmer")
```

## Next steps

Open and work through `simple-coding-agent.qmd`
