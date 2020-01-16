# Cohort Setup

The previous pages we have covered on creating, previewing, and publishing a curriculum block repo. This makes your content available for all cohorts in Learn, but doesn't actually attach it to any one cohort for students to use. To do that, create a cohort in the Learn UI and attach curriculum blocks.

## Creating a cohort

1. Go to the cohorts list in Learn https://learn-2.galvanize.com/cohorts and click NEW COHORT.
2. Auth opens in a new tab. Fill out the form and submit.
3. You now have a cohort in Learn! Either click the link back to Learn, or find it on the cohorts list page from step 1.

Note -- the previous dependency with Salesforce has been removed from this process.

## Adding curriculum to your cohort

1. Open the cohort you created in Learn.
2. Click SETUP in the navigation.
3. Make sure that the secondary nav is on REPOS.
4. Create a course yaml file following the instructions and examples from https://github.com/gSchool/learn-course-files/. Course yaml files are basically a list of repos. They make it easy to teach multiple courses from the same list and track which repos are used in each course.
5. Sync your course to the yaml file you created.
