# Shashi Kumar <!-- TODO: your full name as it appears on your CV -->

I'm a QA automation engineer who builds tools that make LLMs write tests, and
builds the checks that stop bad generated code from reaching the suite. Before
any AI output goes into a test framework, it has to parse, validate and compile.
<!-- TODO: add one line on years of experience / domain, e.g. "N years testing <domain> at <company>." -->

*Open to SDET / QA automation / AI-in-testing roles. [Contact below](#reach-me).*
<!-- TODO: upload your CV PDF to this repo and add a Résumé link here -->

## Start here

**[ai-playwright-framework](https://github.com/shashibalaji/ai-playwright-framework)**
turns plain-English requirement files into Playwright + TypeScript Page Objects
and specs. It uses a local LLM (Ollama, qwen2.5-coder), so it needs no API key
and costs nothing to run.

The LLM doesn't guess at the page. First, a headless browser visits the target
app and records its forms, tables, navigation and ranked locators. Existing Page
Objects and specs are indexed and pulled in by relevance. All of that becomes a
structured prompt built from real evidence.

**The part I'd want you to look at:** generated code is written to a
*candidate* folder, not to the suite. It only gets promoted into `tests/` and
`src/pages/` after it passes these checks:

- output parsing
- a code validator
- duplicate detection
- a strict `tsc --noEmit` compile

If any check fails, the candidate is thrown away. Every run writes a JSON + HTML
generation report, and a dashboard summarises success rate and validation
failures across runs.

Python orchestration · Playwright (sync API) for observation · TypeScript
Playwright for output · GitHub Actions CI.

## AI tools for testers

- **[user-story-to-tests](https://github.com/shashibalaji/user-story-to-tests)**:
  a full-stack app (React + Vite front end, Express + TypeScript API) that pulls
  a user story from **Jira** and generates positive, negative and edge-case test
  cases with an LLM (Groq). It can also generate Gherkin feature files and Page
  Objects. The LLM's responses are schema-validated with **Zod**.
- **[ai-extension](https://github.com/shashibalaji/ai-extension)**: a Chrome
  extension (Manifest V3, side panel). You select elements on any live page and
  it generates automation code for them using OpenAI or Groq.
- **[qabot](https://github.com/shashibalaji/qabot)**: a document Q&A bot built
  with LangChain + Express. Upload PDF, DOCX, TXT or CSV files and ask questions
  about them. It can switch between Groq, OpenAI and Anthropic models.

## Test automation frameworks

- **[playwright-ui](https://github.com/shashibalaji/playwright-ui)**: a
  Playwright + TypeScript UI suite against an Angular app. It uses a Page Object
  Manager, custom fixtures, setup/teardown projects, reuse of authenticated
  storage state, and runs in Docker. CI runs on GitHub Actions.
- **[playwright-api-testing](https://github.com/shashibalaji/playwright-api-testing)**:
  API testing with Playwright. It includes a custom request handler, JSON-schema
  validation of responses (AJV), custom `expect` matchers, Faker test data and
  request logging.
- **[Storyblok-automation-framework](https://github.com/shashibalaji/Storyblok-automation-framework)**:
  Cypress POM suite for a headless CMS's asset manager (upload, replace,
  private/public, bulk upload) with Mochawesome reporting.
- **[pipeline](https://github.com/shashibalaji/pipeline)**: Selenium + TestNG
  with Maven, run through reusable GitHub Actions workflows. It has separate
  PR, nightly, manual and cloud runs, plus SonarCloud analysis.

## Toolbox

**Automation:** Playwright · Cypress · Selenium · TestNG
**Languages:** TypeScript · JavaScript · Python · Java
**AI:** Ollama · OpenAI · Groq · Anthropic · LangChain · prompt design for code generation
**CI & tooling:** GitHub Actions · Docker · Maven · SonarCloud · Jira API

## Reach me

I'm open to SDET / QA automation roles, especially teams putting AI into their
testing workflow and wanting guardrails around it.

[shashikumar.star.bs@gmail.com](mailto:shashikumar.star.bs@gmail.com) ·
[LinkedIn](https://www.linkedin.com/in/shashi-kumar-qa/)
<!-- TODO: add · [Résumé (PDF)](<url>) -->
