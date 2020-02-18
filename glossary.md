# Glossary

This is a quick list of key terms for curriculum and Learn, including terms related to the new Learn CLI. For more detailed instructions and examples, refer to the Learn CLI Walkthrough by opening `/__walkthrough` and following instructions from there.

## Learn and Auth

* **Learn**: Manages course content and student progress https://learn-2.galvanize.com/.
* **Auth**: Manages users and product creation https://auth.galvanize.com/


## Creating Curriculum

#### Creating Curriculum: Learn CLI

* `learn help`: See a list of commands (also `learn preview --help`, `learn publish --help` etc.)

* `learn guide`: Download this interactive guide and walkthrough to your current directory.

* `learn preview [path]`:  Render files in Learn before committing to Git.

* `learn publish`: Publishes the Master branch of a repo to Learn.

* `learn set --api_token=YOUR_LEARN_API_TOKEN`: Set your your credentials for the CLI.

* `learn version`: Retrieve the currently installed learn CLI version.

Learn more -- `/_walkthrough`


#### Creating Curriculum: Curriculum Tools

* **Galvanize-flavored markdown Atom/VSCode plugin**: Snippets to speed local curriculum creation for Learn.
Install and details -- https://github.com/gSchool/galvanize-flavored-markdown

* **Galvanize-curriculum-tools**: Other tools to help with curriculum creation.
Install and details -- https://github.com/gSchool/galvanize-curriculum-tools

* **Learn Command Line Tools**: CLI for publishing. You probably used these to get here.
Install and details -- https://github.com/gSchool/glearn-cli


#### Creating Curriculum: Configuration

* `config.yaml`: Manually created file that defines the content and sequence of a curriculum block.

* `autoconfig.yaml`: Automatically created when no `config.yaml` present. Follow a folder and file naming convention to control how the `autoconfig.yaml` is written.

Learn more -- `/__walkthrough/03-organize-content.md`


#### Creating Curriculum: Content Organization

* **Block**: The smallest discrete building block in Learn. Blocks are one repo of content published individually in Learn. Contain Units, Lessons, Checkpoints, etc.

* **Unit**: Appears as a square "card" on the curriculum overview page in Learn. Contain Lessons, Checkpoints, etc. In a Block repo's Config.yaml units are called `Standards`.

* **Lesson**: Content file within a repo that holds written material, videos, slides, and challenges. Can be markdown, pdf, or ipynb.

* **Checkpoint**: An assessment with one or more challenges that are scored together. There can be 0 or 1 Checkpoints per unit.

* **Challenge**: An interactive question or inline code editor within Lessons and Checkpoints that students respond to. Defined in the Markdown of content files.

* **Instructor File**: A content file that's only visible to instructors.

* **Resource**: A content file that's accessible to students but not included in the left navigation.

Learn more -- https://learn-2.galvanize.com/cohorts/667


#### Creating Curriculum: Challenge types

All challenges auto-evaluated unless noted.

* **Multiple Choice**: submit a single answer to a multiple-choice question.

* **Checkbox**: submit multiple answers to a multiple-choice question.

* **Number**: submit a number as the answer to a question (incl. decimals and fractions)

* **Paragraph**: submit a long free-form text answer to a question. Not auto-evaluated by Learn.  

* **Short Answer**: submit a short answer that's evaluated as exact-match or RegEx

* **Code Snippets (Python, JS, Java, SQL)**: write code directly in Learn. Submission is evaluated against unit tests

* **Custom Code Snippets**: Functionality of Code Snippets for any language

* **Project**: student completes work outside of Learn, submits a link (typically from Github) for tracking and review within Learn.

* **Testable Project**: like Project Challenges, but Learn automatically runs tests in the repo and publishes results to instructor

Learn more -- https://learn-2.galvanize.com/cohorts/667/blocks/13/content_files/Multiple-Choice-Challenge.md


## Content Management

* **Block versions**: When a curriculum block is published from master, a new version is created. Cohorts can teach off of latest version or past versions.

* **Block branches**: A curriculum block can be taught off of a branch other than Master, but can only be published from Master.

Learn more -- https://learn-2.galvanize.com/cohorts/667/blocks/13/content_files/versions-branches.md


## User Management

* **Unconfirmed user**: User has been invited to Learn but has never confirmed their email/created a password.


#### User Management: Roles / Permissions

Roles for users within Learn and Auth

* `auth.admin`: View and manage all users in Auth.

* `auth.product_admin`: View and manage all courses in Auth. Enroll users in courses.

* `auth.app_admin`: Admin permissions for the Auth application. *Only granted to the Learn Product team*

* `forge.admin`: View and manage all cohorts in Learn. Equivalent to having the `forge.instructor` role for every cohort.

* `forge.blocks_manager`: Publish new blocks and new block versions in Learn.

* `forge.instructor`: (Cohort-level permission.) Manage specific cohorts in Learn. View instructor-only pages for setup and grading.
