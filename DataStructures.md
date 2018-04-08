# Data Structures

## DominoResult

- **domino-id**: a project id given by the arbiter when the project is registered
  - must be random so that duplicate project names can exist
  - or use repository url eg "https://github.com/user/project"
  - or totally random eg "abcdefgh"
- **domino-token**: a randomly generated password / identifier for the project
  - eg ejflkwejfwjergf2342_23
  - must be stored as a configuration variable, not in source
- **event-token**: a token that contains the parent event and child event as given by the arbiter
- **project**: a file grabbed from disk containing:
  - **repository-url**
  - **owners-url**
- **metadata**:
  - branch
  - tags
  - commit
  - commit message
  - pipeline url
  - pipeline result: SUCCESS, CANCELLED, FAILED, SKIPPED, TIMED OUT
  - artifacts built

## DominoEvent

- **ci-token**: token needed to trigger the CI pipeline
- **event-token**: token given by arbiter to keep track of event flow
- **metadata**: upstream metadata
- **artifacts**: upstream artifacts
- **project**: upstream project
