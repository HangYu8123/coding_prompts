# create necessary files for guiding the entire agentic coding workflow

#Step 1
First go through the entire repo, keep what files exist in this repo in the memeory. 

#Step 2
Then, check the existence of the folliwing files:
1. codebase_overview.md
2. scripts_overview.md
3. update_logs.md
4. known_issues.md

#Step 3
Create a subagent, read through all the scripts in the code repo, understand them, and create a pipeline for the entire repo. The subagent should feed the pipeline of the code back to the main agent. 


#Step 4
create/update the files in step 2 with the **follwoing specifications in the following order**. 


##1 codebase_overview.md:
If the file does not exist, create an empty file, and set the pipeline to be the pipeline generate by step 3.
If the file exists, the main agent should read through the file and keep it inside the memeory, and set the pipeline to be the diagram pipeline in the file.
Then:
1. create a subagent, follow the pipeline of the repo, go through all the scripts in the order that specifies the pipeline and check the correctness of the pipeline. Then return the results to the main agent. 
2. based on the existing pipeline in the memory, and the review from the subagent, the main agent specifically checks the inconsistency, and make the final decision. 
3. the main agent should update the pipeline based on the final decision
4. the main agent should convert the pipeline into a code diagram. In each block in the diagram, the associate scripts should also be mentioned. 
5. Then, create a subagent, pass the pipeline diagram to the subagent, the subagent go through the generated diagram and associate scripts step by step and make sure the correctness and consistency. Then feed the review back to the main agent. 
6. Then based on the diagram and the review, the main agent check the correctness by itself and update the diagram accordingly.
7. Finally, write the diagram into the codebase_overview.md, along with a description of the repo. 


##2 scripts_overview.md


##3 known_issues.md:

##4 update_logs.md
get the git commit history, and create a file with the git commit history ( do not add any interpurtations, be faithful to the original contents) logs. 


