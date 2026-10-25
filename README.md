# Evidence Check

Evidence Check is a small, approachable classroom game for students beginning an introductory evidence unit. It introduces three ideas in two separate rounds:

1. Direct evidence and circumstantial evidence describe how a fact is established.
2. Potential hearsay concerns how an out-of-court statement is being used.

The activity has no score, timer, grade, streak, login, analytics, external library, API, or backend. Questions are shuffled within each round and immediate plain-English feedback follows every answer.

## How it works

The entire game is contained in `index.html`. The file includes:

- Responsive HTML and CSS
- The complete question banks in the `ROUNDS` JavaScript array
- Randomization, answer feedback, round transitions, replay, and review behavior
- Full keyboard navigation with standard `Tab`, `Space`, and `Enter` controls
- Visible focus styles, large tap targets, live feedback announcements, and reduced-motion support

The rounds always stay in order, but the questions within each round are shuffled each time the player starts again.

## Run locally

There is no build step. Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8080
```

Then visit <http://localhost:8080>.

## Edit questions

Open `index.html` and find `const ROUNDS`. Each question has four fields:

```js
{
  fact: "Fact to prove: the driver ran the red light",
  prompt: "A witness testifies, “I saw the driver run the red light.”",
  answer: "Direct Evidence",
  explanation: "The witness personally saw the driver run the light."
}
```

For Round 1, use exactly `Direct Evidence` or `Circumstantial Evidence`. For Round 2, use exactly `Potential Hearsay` or `Not Hearsay`.

Keep examples suitable for absolute beginners. Do not add hearsay exceptions, opposing-party statements, or ambiguous examples. Direct and circumstantial evidence concern how a fact is established; hearsay concerns the use of an out-of-court statement.

## Publish with GitHub Pages

The repository includes `.github/workflows/pages.yml`.

1. Push the repository to GitHub.
2. Open **Settings > Pages** in the repository.
3. Under **Build and deployment**, select **GitHub Actions**.
4. Push to `main` or run the Pages workflow from the **Actions** tab.

Project URLs:

- Source: <https://github.com/JenS246/evidence-check>
- Live game: <https://jens246.github.io/evidence-check/>

No backend or persistent data is used, so there is no data backup or restore procedure.
