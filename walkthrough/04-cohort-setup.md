# Cohort Setup

The previous pages covered creating, previewing, and publishing of a curriculum block repo. This makes content available for all cohorts on Learn, but doesn't actually attach it to any one cohort for students to use. To do that, create a cohort in the Learn UI and attach one or more curriculum repos.

## Step 1: Create a cohort

If you don't have a cohort yet--

1. Go to the cohorts list in Learn https://learn-2.galvanize.com/cohorts and click NEW COHORT.
2. The Auth application opens in a new tab. Fill out the form and submit.
3. You now have a new cohort in Learn! Either click the link back to Learn, or find it on the cohorts list page from step 1.

## Step 2: Add curriculum to your cohort

A set of curriculum repos is connected to your cohort through a course yaml file (which is a list of repos).

**Note**
This `course.yaml` file is completely separate from a repo's `config.yaml` or `autoconfig.yaml`.

1. Go to the cohort you created in Learn.
2. Click SETUP in the navigation. Make sure that the secondary nav is on REPOS.
3. Create and push a course yaml file following the instructions and examples from https://github.com/gSchool/learn-course-files/.
4. Back in the Learn UI, sync your cohort to the course yaml file you created.

## Curriculum updates

Once you have synced one or more repos to your cohort, there is no need to resync the `course.yaml` yaml file. Any curriculum updates that are published (using `learn publish`) will automatically be pulled in for any cohort that has included that repo.

If a cohort does not want to receive updates, the instructor can choose to change the update setting for any repo from "auto" to "manual" on the SETUP -> REPOS page.

## Continue

Next: [05-challenges.md](05-challenges.md)
