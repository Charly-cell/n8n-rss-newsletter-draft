# From an RSS feed to a newsletter draft with n8n and Gemini

Beginner course: automate a weekly AI newsletter draft with n8n and Gemini.

## The problem
A training team must follow AI and no-code news for its newsletter. Reading source after source takes time, so the newsletter comes out irregularly.

## What you build
An n8n workflow of 7 nodes. With one click, it reads the latest articles of a public blog (RSS), asks Google's Gemini API to write a newsletter draft in English, and returns it. A human still reviews the draft before sending.

## What is in this repository
| Folder | Content |
|---|---|
| [`course/`](course/Charly_JEDHA_course.pdf) | The course (PDF, 15 pages): prerequisites, setup steps with screenshots, test and expected result, troubleshooting |
| [`workflow/`](workflow/rss-to-newsletter-draft.json) | The n8n workflow, exported as JSON |
| [`video/`](video/Charly_JEDHA_presentation.mp4) | Presentation video of the use case and learning goals (1 min 35) |

Notes: GitHub's preview does not make links in a PDF clickable and cannot play files over 10 MB. Download the PDF to use its links, and use **Download raw file** on the video page to watch the video.

## Prerequisites
- A Google account
- A free [n8n Cloud trial](https://n8n.io) (14 days)
- A free Gemini API key from [Google AI Studio](https://aistudio.google.com/apikey?hl=en)

## Quick start
1. Create your Gemini API key (course, Step 0).
2. In n8n, import `workflow/rss-to-newsletter-draft.json` (menu **Import from file**).
3. In the **Ask Gemini** node, create a Header Auth credential (name `x-goog-api-key`, value: your key).
4. Click **Execute workflow**, then open **Extract draft** to read the draft.

The course explains each step in detail.

## Important
- No API key is stored in this repository. Each learner uses their own key.
- On Google's free tier, prompts may be used to improve Google products. Use public content only.
- The AI text changes at each run: always review the draft against the source articles.

## Author
Charles-Henry Geoffroy. Built as the use case for the Content Creator – Product Builder application at Jedha.
