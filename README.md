[yml-link]: https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-githubs-form-schema

# Template for C or C++ projects

This repository is a template that you can use for your C or C++ projects.  
It use actions to have a CICD for the projects.  
You have already templates for issues and pull requests configured.  

## Mandatory

To make the CI works correctly you will need to have those points :
- Makefile / CMake (or both) building correctly
- Tests rules :
    - For Makefile -> make tests_run
    - For CMake -> use ctest  
    - The Coverage will be tested automatically

## CI Jobs
Here are the details of what jobs are doing on CI.
- Test the build on epitech docker image
- Test the build on differents environnement :
    - Ubuntu
    - MacOS
- Run the tests present on the project with epitech docker image (Makefile / Cmake)
- Run the tests on differents environnement

## Setup CD
Here is some advice to setup some feature on the CD inside ./github/workflows/CD.yml.
- Mirroring :  
  If you want to setup a push to miror, uncomment the commentaries and create/fill the variables :
  - MIRROR_URL : the link of the repo you want to push.
  - GIT_SSH_PRIVATE_KEY : the key that will represents the rights of push.

## Customization
If you want to customize CI depends on what you needs here some little advice.
- Dependencies :
    - If you need to download some dependencies the CI might not work.  
      Don't worry ! You can change the steps Install dependencies inside build jobs.  
      You can find the file to change into .github/workflows/CI.yml.  
      (You might change the CD too : .github/workflow/CD.yml).  
- Mirroring :
    - If you want to setup a mirror repository there's already a mirroring feature.  
      You simply need to setup the environnement variable where you want to mirror.  
      Find the variable name inside workflows files in ./github/workflow.  
- Issues :
    - There is many templates for issues.  
      If there is one that you don't like or you want to modify check the files inside .github/ISSUES_TEMPLATES.  
      I wrote them in .yml but you can change into .md if you prefer.  
      [Here is a little link that can help you for yml][yml-link]
- Pull request :
    - There is a template for pull request.  
      You can modify it inside .github/pull_request_template.md.  
      Warning ! The template is in md only, you can't do it in yml.  
      If you find a way to write it in yml see CONTIBUTING.md.  
    
- Contribution :
    - If you want to add few more features look at CONTRIBUTING.md file


## Usefull links
https://gist.github.com/StevenACoffman/66573a444d3b1f36b2347259752968b9

https://github.com/bevyengine/bevy

https://docs.github.com/en/actions/learn-github-actions/variables#using-the-env-context-to-access-environment-variable-values

https://github.com/actions/runner/issues/662

https://docs.github.com/en/actions/learn-github-actions/contexts

https://github.com/softprops/action-gh-release
