# Contributing to bedrock-v

Thanks for your interest in contributing to bedrock-v.

bedrock-v is a collection of open-source projects related to Minecraft:
Bedrock Edition and the V programming language. The organization includes
server software, protocol and networking implementations, data-format
libraries and developer tooling.

Most projects are under active development. APIs, internal structure and
project boundaries may change as they mature.

Contributions of all sizes are welcome.

## Getting started

Before working on a repository:

1. Read its README and repository specific contribution documentation.
2. Check existing issues and pull requests for related work.
3. Build and test the project locally when possible.
4. For large changes, discuss the design before spending significant time
   implementing it.

Repository-specific instructions take precedence over this document.

## Ways to contribute

Contributions are not limited to code. Useful contributions include:

- Bug reports and reproducible test cases
- Documentation improvements
- Testing on different platforms and environments
- Protocol and format research
- Bedrock behaviour observations
- Performance measurements and benchmarks
- Small fixes and cleanup
- New features
- Reviewing issues and pull requests

If you are unsure whether an idea belongs in a project, opening an issue or
starting a discussion first is usually the easiest way to find out.

## Pull requests

Keep pull requests focused.

A pull request should have one clear purpose and avoid unrelated cleanup or
refactoring. Smaller, coherent changes are generally easier to understand,
test and review.

Before opening a pull request:

1. Make sure the project builds or clearly document why it does not.
2. Run the relevant tests and checks described by the repository.
3. Keep unrelated changes out of the pull request.
4. Explain what changed and why.
5. Reference related issues when applicable.
6. Mention important limitations, compatibility concerns or intentionally
   unsupported cases.

Draft pull requests are welcome for work that needs early feedback.

## Larger changes

Please discuss substantial changes before implementing them.

This is especially useful for changes that:

- Introduce or significantly change a public API
- Add a dependency
- Change persistence or file formats
- Change protocol or networking behaviour
- Introduce new concurrency or ownership models
- Affect compatibility with existing worlds or users
- Add a large subsystem
- Move responsibilities between projects

An issue does not need to contain a complete design before discussion starts.
The goal is to agree on the problem and general direction before a large
amount of code is written.

## Bedrock behaviour and protocol work

Minecraft: Bedrock Edition behaviour changes between versions.

When implementing behaviour that is intended to match Bedrock, do not invent
semantics when they can be verified.

Use the strongest source available for the claim being implemented. Depending
on the work, this may include:

- Official Mojang or Microsoft documentation
- Published protocol or format specifications
- Behaviour observed from a current Bedrock client or server
- Reproducible experiments
- Independent implementations used for comparison

Existing third-party implementations are useful references but should not
automatically be treated as authoritative.

When behaviour is uncertain, say so. A documented uncertainty is preferable
to presenting an assumption as confirmed behaviour.

For substantial parity or protocol changes, include the relevant source,
observation or reproduction in the issue or pull request when practical.

Tests should verify the intended behaviour, not merely repeat assumptions made
by the implementation.

## Code

Follow the conventions of the repository you are contributing to.

In general:

- Prefer simple and explicit code.
- Keep ownership and mutation clear.
- Avoid abstractions without a concrete need.
- Keep public APIs as small as the problem allows.
- Handle errors deliberately.
- Avoid unnecessary dependencies.
- Do not optimize without understanding the relevant workload.
- Add comments when they explain behaviour, constraints or non obvious
  decisions rather than restating the code.

Run `v fmt` on V code before submitting it. 
(If the formatter mangles otherwise reasonable code, don't fight it just to satisfy the formatter. You may use v fmt from the latest stable V release or leave the affected code as-is. Formatter bugs are not a blocker for contributions.)

## Generated and data-driven code

Some bedrock-v projects work with large protocol definitions, palettes,
registries or other machine readable data.

Prefer reproducible generation or transformation over manually maintaining
large amounts of mechanical data.

Generated output should have a clear source and a reproducible way to update
it. Avoid manually editing generated files unless the repository explicitly
documents otherwise.

Automation must not invent protocol or gameplay behaviour. Generation can
transform known data; uncertain semantics still require evidence and review.

## Tests

Tests should protect behaviour that matters.

Add or update tests when a change introduces new behaviour, fixes a regression
or modifies an important invariant.

A useful regression test should fail for the problem it is intended to catch
and pass after the problem is fixed.

## Performance changes

Performance work should include evidence when practical.

This may be a benchmark, profile, allocation measurement, trace or a
reproducible workload depending on the change.

## AI-assisted contributions

Using AI-assisted development tools is allowed.

The contributor remains responsible for the submitted change regardless of
which tools were used to produce it.

AI-generated code, tests, explanations or protocol conclusions should be
reviewed and verified in the same way as manually written work.

## Code of Conduct

By participating in bedrock-v projects, you agree to follow the organization's
[Code of Conduct](https://github.com/bedrock-v/.github/blob/master/profile/CODE_OF_CONDUCT.MD).
