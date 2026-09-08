# Contributing to bobashare

Outside contributors are welcome! If you're here for the first time and not sure
what to work on, consider checking the [good first issue
label][good-first-issue]. Or, if you see any other issue that catches your eye,
feel free to work on it as well. I can answer any questions if you just post a
comment.

[good-first-issue]: https://github.com/BBaoVanC/bobashare/issues?q=state%3Aopen%20label%3A%22good%20first%20issue%22

## Checklist

This is a list of things that are easy to forget (including for me):

- Are your commit messages descriptive?
  - Commit messages in pull requests are a controversial topic. But in my
    opinion, I think it's fine to leave incremental commits that show the
    history and evolution of your pull request. Additionally, it can be a pain
    to try and hound contributors into making absolutely spotless commit
    messages. To accomodate this, I often squash PRs upon merge.
  - TL;DR: Write good commit messages, but don't stress to hard about it. Expect
    commits to be squashed and manipulated a bit when the PR is merged.
- Did you update the changelog?
  - When submitting new features, place them under the "Unreleased" section.
  - The release section is split into three h3 subsections: "Security",
    "Features", "Bugfixes", and "Internal Changes", in that order. If the
    subsection doesn't already exist, then create it.

## Structure

bobashare is split into three crates:

### bobashare-web

This is where the bulk of the development is happening. It holds the web
backend, written with [axum](https://docs.rs/axum/latest/axum/).

### bobashare

This helper library handles the actual storage backend. It interfaces between
bobashare-web and the operating system, acting like a database for uploads.

### bobashare-admin

This is an incomplete CLI meant for doing basic operations on the bobashare
database. I haven't had time to work on it, but it's intended to be used by
administrators for creating, deleting, and editing uploads manually.
