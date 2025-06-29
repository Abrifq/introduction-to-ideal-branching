# Branch Managing

Navigator: [Index](index.md), [Next Article: Branch rulesets (Github)](branch-rulesets-github.md)

In a perfect world of my mind, the branches are categorized in two ways:

- The "development" branches where developers will directly push code into,
- The "safe" branches where the changes are pushed after required controls happen.

## Development Branches

- Naming rule: `branch-owner/branch-name`

	Usually, the `branch-name` is the feature the `branch-owner` is working on.

	Examples:

	- `Abrifq/clarify-dual-license`,
	- `Abrifq/migrate-to-another-CI-provider`,
	- `Abrifq/customer-<id>/request-<request-number>`

- Working rules:
	- People can push without a problem. Pushing to the correct branch is a self-governance issue.

		A developer should not wait for a [ruleset](branch-rulesets-github.md) to be changed and then push helping commits.

	- Code checks will run **after** code has been pushed into the branch.
		Code prettifiers / style linters will **not run** in these branches, as it will hinder the developer when pushing.

	- These branches are also supposed to be **based upon the target safe branch** the developer is trying to contribute to.

		`Abrifq/release/fix-translation-in-5.16` should be based on `release/5.16` and should contribute back to `release/5.16`

		This rule helps ease eliminating merge commits as the branch will always be on topic.

## Safe Branches

Navigator: [Index](index.md), [Next Article: Branch rulesets (Github)](branch-rulesets-github.md), [Go to start of this article](#branch-managing)
