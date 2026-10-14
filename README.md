# AI-200 Practice

A single-page practice site for the Microsoft AI-200 exam (Developing AI Cloud Solutions on Azure).

- Full timed practice exam (50 questions, 100 minutes, 70% pass mark) with mark-for-review and a question navigator
- Exam questions are drawn in proportion to the AI-200 domain weights
- Practice by topic, grouped under Containers, Data for AI, Using Azure services, and Security and monitoring
- Five question formats: multiple choice, choose more than one, drag to order, drag to match, select from lists
- Partial credit: each correct selection, step, match or list choice earns a point, as on the real exam
- Case-study questions show an expandable case summary, and code questions show the code above the answers
- Progress is based on your latest answer to each question, from both practice and full exams, and is saved in the browser (localStorage)

This is an unofficial study aid and is not affiliated with Microsoft.

## Run it

Put `index.html` and `private-questions.js` in the same folder and open `index.html` in a browser. No build step or dependencies.

The questions live only in `private-questions.js`. Without it, the site shows a "No questions loaded" message. The file is listed in `.gitignore`, so it is not pushed to GitHub.
