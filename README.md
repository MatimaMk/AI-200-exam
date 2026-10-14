# AI-200 Practice

A single-page practice site for the Microsoft AI-200 exam (Developing AI Cloud Solutions on Azure). Unofficial study aid, not affiliated with Microsoft.

- Timed exams in the style of the Microsoft exam screen: choose a length (10, 25, 50, 100 or all), or work through Exams 1–3 in order
- Practice by topic or by question format, with explanations after every answer
- Study page showing every question with its answer, plus search, filters and a hide-answers mode
- Five question formats, partial credit, case studies and code exhibits

## Access control

The questions are encrypted in `questions.enc.js`. Visitors sign in with a username and password, and their browser decrypts the questions. Without a valid login the file can't be read, so it is safe to keep in this repo.

## Managing users

You need Node.js. Keep these files in one folder on your computer:

- `manage-users.js`
- `private-questions.js` (the readable questions; never upload)
- `users.json` (created by the script; holds usernames and passwords; never upload)

Commands:

```bash
node manage-users.js add thabo "colleague"   # give access; prints the password to send them
node manage-users.js remove thabo            # take access away
node manage-users.js reset thabo             # new password for someone
node manage-users.js list                    # who has access
node manage-users.js build                   # re-encrypt after editing private-questions.js
```

After `add`, `remove`, `reset` or `build`, upload the new `questions.enc.js` to GitHub. Vercel redeploys automatically.

Back up `users.json` somewhere safe. If you lose it, run `add` again for each person and send them new passwords.
