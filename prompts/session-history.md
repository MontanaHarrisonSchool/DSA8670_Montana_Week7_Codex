# Chronological Prompt History

This is a retrospective capture of the user prompts visible in this project conversation. Exact per-message timestamps were not retained in the local project files; prompt order and wording are preserved here. The separate `01_final_analysis.md` file summarizes the selected analysis prompt.

## Prompt 01 — Assignment review and workflow wireframe

View the Assignment requirements word document in the project folder. After viewing the folder contents, create a wireframe of steps that you think would be the best method for the project. The goal of this project is to prove my fluency with codex by having you read through the data in the data folder, conduct analysis given a specified question, and approve/modify code before committing it to github. After we agree on the wireframe of work, we can get started with the folder architecture. We should design the wireframe to make sure we fill out all of the requirements in the grading criteria on the assignment details. At the end we will compare our results and make sure we are positioned to receive full credit. Let's utilize jupyter notebook for this analysis, i will check the results in vscode.

## Prompt 02 — Project folders and exploratory notebook

No real need for a /data folder so we can skip that.
Create all required folders and sub folders and let's start investigating the shape of the data and some trends. We want to build the notebook in small and reviewed steps yes, but not so small that each task is another prompt that wastes tokens. Let's start with data exploration, create a jupyter notebook that i can open in vscode that let's user explore the data releavant to our question choice.

## Prompt 03 — Dependency setup

Creeate an install block to install packages im currently missing so i dont have to keep managing it, after making the block, install the packages, and then comment out the install package lines

## Prompt 04 — Check the installation

Did our install not work? do i need to re open vs code for the dependencies to work? Im getting the the same issue

## Prompt 05 — Kernel discovery issue

the venv is not available, something is either set up incorrectly or something is wrong between the version commits with github. try one more time to view this before i fix it manually. i have vs code open, your venv you built is not avaialble to select as a kernel.

## Prompt 06 — Rebuild with the installed Python

Recreate the project's .venv using my existing Python installation at C:\Users\Montana\AppData\Local\Programs\Python\Python312\python.exe. Do not use Codex's bundled Python. Remove the existing .venv, create a new one using my installed Python 3.12, install pandas, matplotlib, and ipykernel, and register it as a Jupyter kernel named "Ames Week 7". Verify the environment works and do not modify any project files or make any Git commits.

## Prompt 07 — Investigate the Styler error

have an attribute error in the file, investigate it
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
Cell In[8], line 11
      7         median_living_area=("Gr Liv Area", "median"),
      8     )
      9     .sort_values("median_sale_price", ascending=False)
     10 )
---> 11 display(neighborhood_summary.style.format({
     12     "median_sale_price": "${:,.0f}",
     13     "mean_sale_price": "${:,.0f}",
     14     "median_living_area": "{:,.0f} sq ft",

File ~\Documents\GitHub\DSA8670_Montana_Week7_Codex\.venv\Lib\site-packages\pandas\core\generic.py:6194, in NDFrame.__getattr__(self, name)
   6190             and name not in self._accessors
   6191             and self._info_axis._can_hold_identifiers_and_holds_name(name)
   6192         ):
   6193             return object.__getattribute__(self, name)
-> 6194         return object.__getattribute__(self, name)

File ~\Documents\GitHub\DSA8670_Montana_Week7_Codex\.venv\Lib\site-packages\pandas\core\frame.py:1430, in DataFrame.style(self)
   1426         """
   1427         # Raise AttributeError so that inspect works even if jinja2 is not installed.
   1428         has_jinja2 = import_optional_dependency("jinja2", errors="ignore")
   1429         if not has_jinja2:
-> 1430             raise AttributeError("The '.style' accessor requires jinja2")

## Prompt 08 — Continue the wireframe

Great, now our notebook is functioning properly. What's next on our wireframe?

## Prompt 09 — Run the selected analysis

Grab the question you think is best and run the analysis. Do not ask to confirm before proceeding on the analysis, just pick the question and go

## Prompt 10 — README and rubric review

Let's proceed, when you are finished with the readme let me know and i will take a look. With this step in reviewing, let's pay extra attention to the rubric as well, so we are looknig for not just accuracy, but also completedness of the assignment at this stage.

## Prompt 11 — Complete remaining documentation

The readme looks good, let's finish the remaining tasks - for the Reflection, this will mostly be me typing, but what you can do is go ahead and highlight the shortcoimings or challenges we faced during the initial build such as the python bundle confusion and how we fixed it. I will finish the reflection from there

