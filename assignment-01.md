# Assignment O1: Wrangling geodata via command line

Your assignment is to create a new map using a different data set and geographical area of interest, practicing the techniques introduced and demonstrated through the lesson.

Your process should be documented through Git branches and commit messages to complete the map, as well as notes you add to a repository's _README.md_ file using Markdown (see the [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)).

**Tip**: You can view the history of your commands in the terminal (`history` in Mac OS) and even redirect that to a file (`history > history.txt`). You can then copy and paste the important commands you use within your README.md file for thorough documentation of your process and to reference later.

## Recommended process

Consider using this recommended process:

1. Choose an urban environment somewhere in the world to explore through geospatial data and mapping (similar to the example of Atlanta within the lesson). Search the web for available datasets (see [Searching for GIS data](#searching-for-gis-data) below) and let this somewhat drive your decision of which city to study. You don't want to spend days looking for a "perfect" dataset. Just pick one and be playful!
2. Create a new GitHub repository on your personal GitHub account. Include a _README.md_ file and a _.gitignore_ file to exclude packages (e.g., .zip files) and Shapefiles (see the lesson). Add your instructor (@rgdonohue) as a collaborator with write credentials within the GitHub web interface so he can clone down, push up, and create Pull Requests. Then, clone the repository down to your local machines to begin working.
3. Download various datasets related to your chosen urban environment to your local machine. Spend some time examining the data and attributes. Save these in a "temp" directory of some kind outside of the project repository (unless you've already done step 5 below), or include this temp directory in your _.gitignore_ file (only commit and push up to the remote repo data that you actually want to use and backup).
4. Think about what the map may achieve (a basic "scenario" such as the one used in the lesson). We're not doing full-blown user-centered design here; just trying to make a map with the data.
5. As you work consider creating new branches (locally) for different tasks for practice. Review the excellent [collaborative Git workflow](http://vallandingham.me/git-workflow.html) for additional support.
6. Your initial workflow should include the following:

   - build a file/directory structure for the project (see [recommended structure](#recommended-directory-structure) below)
   - build a basic HTML document to load a Leaflet map (or use another library such as Open Layers or D3)
   - commit changes to the master branch and pushed up to the remote

7. Process your data files to ensure they're all correctly converted to WGS84 GeoJSON files (ready for a Leaflet web map). Try using OGR and/or Mapshaper to do this and record your process within your README.md file.
8. Add the GeoJSON files to the _data/_ directory of the project. Commit this work. Also edit the _README.md_ file to document the sources of the data, the names of the source data files, and the process you used to convert them to the desirable formats. Include terminal commands and other useful information so someone else could reproduce your process. You can even include links to [Stack Overflow](https://stackoverflow.com/questions/tagged/git-commands) or [GIS Stack Exchange](https://gis.stackexchange.com/).

   Note ... if you get too frustrated with a command and need to jump into QGIS, then we always have that tool as well! But avoid resorting back to your comfortable desktop GIS processes when you can through this course. We're here to push ourselves out of our comfort zones.

9. Once there is a single master branch (without merge conflicts) containing the datasets and _index.html_ starter file, edit your web document to load the data, and then plot and and style the map. Add optional interaction.

   **Use Git commit messages along the way, post Issues to GitHub, and document the process within the _README.md_ file**. Your instructor will be evaluating your work along these criteria.

10. Submit a URL to the repository within Canvas Assignments by the due date

**Assignment Advice:** Be experimental with the process. Don't stress too much about creating perfect data or the best map. Communicate your experiences with your class on Slack and your instructor. Merge conflicts happen (and will happen). Command processes can be very frustrating. Learning is also failing at times. The key is to gain from it and move forward. And above all, have fun and enjoy the process.

Also, be mindful that you should not commit and try to push large files to GitHub. You can use the [git LFS](https://git-lfs.github.com/). But if you simply want to quickly share some large files with your team member or instructor, [Firefox Send](https://send.firefox.com/) works well too.

### Searching for GIS data

Given that we're targeting a particular city, perusing general data portals and resources may be less useful than a specific topic. Use search terms such as "open data," "GIS data," "Shapefiles," "city planning" along with your city name. Searching by particular country, state, and regional government offices may also be fruitful.

See also:

- [A data resources list maintained by @rgdonohue](https://github.com/rgdonohue/resources#data-sources)
- [A comprehensive list of 2600+ open data portals around the world](https://www.opendatasoft.com/a-comprehensive-list-of-all-open-data-portals-around-the-world/)

### Recommended directory structure

```bash
/root
  -- README.md
  -- index.html
  -- data/
```

Note that you can also seperate your assets such as the CSS and JS like so:


```bash
/root
  -- README.md
  -- index.html
  -- data/
  -- css/
    -- styles.css
  -- js/
    -- index.js
  --images/
    -- hero.png 
```