# LLM explore

## Setting up 

The set up involve getting your credential for accessing Virginia Tech's LLM service and running the tutorial in a Docker container.  We are using a Docker container so that the LLM agent doesn't accidentally edit or remove files from your computer without your instructions.

1. If not on campus go, log into university VPN
2. Go to <llm.arc.vt.edu>
3. In the bottom right is the setting menu.  Click it and click "Settings".  Click "Account".  In "Account", click "API keys"" and create one if you don't already have one. Leave this page up for step #9

4. Download Docker desktop if you haven't already download it.
5. In your terminal or powershell, run 

```
docker run --rm -ti -e PASSWORD=yourpassword -p 8787:8787 rocker/tidyverse
```
6. Open a web-browser and type
```
http://localhost:8787
```
7. User name = "Rstudio", Password = "yourpassword"

8. Create a new project with version control with this repo (`rqthomas/llm-vt-explore`)

9. Create a new file called "creds.R".  Add this line to the file and save it
```
Sys.setenv(OPENAI_API_KEY = "PASTE YOUR API KEY FROM LLM.ARC.VT.EDU")
```
the value you will add is API Key from step #9

##

Open and work through `simple-coding-agent.qmd`
