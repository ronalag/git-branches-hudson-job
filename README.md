This plugin adds a build step to configuration of a job to allow adding a build step which adds hudson jobs for every feature branch created in the git repository.
# Build instructions
1.mvn pacakge

# Run instructions
1.copy the .hbi file created into your hudson plugin folder.
  eg. cp target/gitFeatureBranch.hpi ~/.hudson/plugins/
If you don't want to actually build the hbi file yourself, you can grab it from the Downloads Section.

# Hudson prerequisites
You need the git plugin for Hudson installed.

#Configuring Hudson
1. Create a new job with "Build a free style Software project".
2. Set the git branch to ** so it builds everytime.
3. Add a build step called "Add hudson project for git branches".
4. Step 3 will lead to a Project-prefix field, this should be same as your current Project name.
5. For windows make sure that you install cygwin and put in the path, also git should be installed separately and put in the path.
6. On windows you will need .sh in your path.

# Results
1. If the project prefix is set to "Job1" then all branches will appear as jobs with names like "Job1-master", "Job1-release".
2. The initial job that will build every time and simply grab create branches as a build step.





