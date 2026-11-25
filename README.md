# one-job-five-posts

**One visit to a job site, a week of posts.** A free Claude skill from Terramore.

- **What you give it:** the job you're doing tomorrow, in a few sentences.
- **What you get back:** five posts to make from that one visit, the shots to grab on site in the order they'll happen, the first line to say for each, and the order to post them.
- **What it never does:** film, edit or post, or make up claims about the job.

## What it does

Before you go, tell Claude about the job. It plans five posts:

1. the problem;
2. the work;
3. a tip;
4. the result;
5. a question people ask.

For each post you get the first line to say on camera, two to four shots, and why it's its own post.

Then it merges every shot into **one list in the order they'll happen on site**: before shots first (from the same spot you'll use for the after), the work, the after, and the talking parts last, once your hands are free. That way nothing needs a second trip.

It only uses the facts you give it. Anything it needs and doesn't have is left as a blank for you to fill: "[what you found up close]".

## Requirements

- Claude Code (tested with 2.1.332 on macOS).
- Nothing else to install. No scripts.

## Install

Ask Claude: "Install the one-job-five-posts skill from github.com/adam-moreno/one-job-five-posts."

Or by hand. **For you, on every project:**

```sh
git clone https://github.com/adam-moreno/one-job-five-posts.git
mkdir -p ~/.claude/skills
cp -R one-job-five-posts/skills/one-job-five-posts ~/.claude/skills/
```

**For one project:** copy `skills/one-job-five-posts` into that project's `.claude/skills/` folder.

Start a new Claude Code session afterwards so the skill is picked up.

## Use

Type `/one-job-five-posts`, or ask: "what should I film on tomorrow's job?", "give me a shot list for this job", "how do I get a week of posts out of one job?".

## Example: before and after

Real input and output from `examples/`. Made-up businesses only, never a real client.

- `examples/before/job-notes.md`: a made-up roofer (Fernbrook Roofing) fixing a chimney leak, with a helper who can film.
- `examples/after/five-posts-plan.md`: what the skill gave back in one real run. That's the five posts, a 10-step shot list, and a posting order.

From that run: the helper films everything on the roof, so the owner never holds a phone up there. The question post is marked "(check: do you hear this?)" because the owner didn't give one.

## Limitations

- **It plans; you film.** It can't see the job, so the plan is only as good as your notes.
- **Privacy and safety come first.** It asks you to get the customer's OK and keep house numbers, faces and plates out of shot. It never plans a shot that means filming while doing dangerous work.
- **It doesn't say which order gets more views.** The posting order tells the story; that's all it claims.
- **Tested once on one made-up business** (see `TESTED.md`).

## Privacy

No telemetry. Nothing leaves your computer except what Claude Code itself sends to Claude. It writes no files.

## Credits

None: written by Terramore.

## Tests

`python3 -m unittest discover -s tests`

## License

MIT. Made by Terramore (terramore.io). Want the video side done for you? Terramore Studio: terramore.io/studio
