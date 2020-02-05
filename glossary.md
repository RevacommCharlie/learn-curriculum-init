# Glossary

This is a quick list of key terms for curriculum and Learn, including terms related to the new Learn CLI. For more detailed instructions and examples, refer to the Learn CLI Walkthrough by opening `./walkthrough` and following instructions from there.  

## Learn and Auth

* **Learn**: Manages course content and student progress https://learn-2.galvanize.com/.
* **Auth**: Manages users and product creation https://auth.galvanize.com/

## Creating Curriculum

#### Learn CLI

[Details](./_walkthrough)

* `learn help`: See a list of commands (also `learn preview --help`, `learn publish --help` etc.)

* `learn guide`: Create a new curriculum repository from a guide template

* `learn preview`:  Render files in Learn before committing to Git.

* `learn publish`: Publishes the Master branch of a repo to Learn.

* `learn set`: Set your your credentials for ~/.glearn-config.yaml

* `learn version`: Retrieve the currently installed learn CLI version

#### Other curriculum tools
[Install and details](https://github.com/gSchool/galvanize-flavored-markdown)
* **Galvanize-flavored markdown Atom/VSCode plugin**: Snippets to speed local curriculum creation for Learn.

#### Configuration
[Details](./_walkthrough/03-organize-content.md)
* `config.yaml`: Manually created file that defines the content and sequence of a curriculum block.

* `autoconfig.yaml`: Automatically created when no `config.yaml` present. Follow a folder and file naming convention to control how the `autoconfig.yaml` is written.

#### Content Organization

[Details](https://learn-2.galvanize.com/cohorts/667)

* **Block**: The smallest discrete building block in Learn. Blocks are one repo of content published individually in Learn. Contain units, Lessons, Checkpoints, etc.

* **Lesson**: Content file within a repo that holds written material, videos, slides, and challenges. Can be markdown, pdf, or ipynb.

* **Checkpoint**: Content file with one or more challenges that are scored together as one assessment. There can be 0 or 1 Checkpoints per unit.

* **Challenge**: An interactive component within Lessons and Checkpoints that students respond to. Defined in the Markdown of content files.

* **Instructor File**: A content file that's only visible to instructors.

* **Resource**: A content file that's accessible to students but not included in the left navigation

#### Challenge types

All challenges auto-evaluated unless noted. [Details](https://learn-2.galvanize.com/cohorts/667/blocks/13/content_files/Testable-Project-Challenge.md)

* **Multiple Choice**: submit a single answer to a multiple-choice question.
* **Checkbox**: submit multiple answers to a multiple-choice question.
* **Number**: submit a number as the answer to a question (incl. decimals and fractions)
* **Paragraph**: submit a long free-form text answer to a question. Not auto-evaluated by Learn.  
* **Short Answer**: submit a short answer that's evaluated as exact-match or RegEx
* **Code Snippets (Python, JS, Java, SQL)**: write code directly in Learn. Submission is evaluated against unit tests
* **Custom Code Snippets**: Functionality of Code Snippets for any language
* **Project**: student completes work outside of Learn, submits a link (typically from Github) for tracking and review within Learn.
* **Testable Project**: like Project Challenges, but Learn automatically runs tests in the repo and publishes results to instructor

## Learn Content Management
[Details](https://learn-2.galvanize.com/cohorts/667/blocks/13/content_files/versions-branches.md)

* **Block versions**: When a curriculum block is published from master, a new version is created. Cohorts can teach off of latest version or past versions.
* **Block branches**: A curriculum block can be taught off of a branch other than Master, but can only be published from Master.


## Learn User Management
* **Unconfirmed user**: user has been invited to Learn but has never confirmed their email/created a password

#### Roles / Permissions

Roles for users within Learn and Auth

* `auth.admin`: App-level permission. Manage users for all courses. Create and destroy courses.  
* `auth.app_admin`: Admin permissions for the Auth application. *Only granted to the Learn Product team*
* `auth.product_admin`: Cohort-level permission. Manage users for any cohort user is an `auth.product_admin`.

* `forge.admin`: App-level permission. View and manage content for all cohorts in Learn.
* `forge.blocks_manager`: User has permission to publish new blocks and new block versions in Learn
* `forge.instructor`: Cohort-level permission. Manage content and users for any cohort user is a `forge.instructor`.
