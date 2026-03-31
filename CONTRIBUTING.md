# Contributing to CRE Agent Skills

Thank you for your interest in improving these skills. Contributions are welcome.

## How to Contribute

### Improving Existing Skills

If you find a formula that's wrong, a threshold that's outdated, or a step that could be clearer:

1. Fork this repo
2. Make your changes to the skill file in `skills/`
3. If the same skill exists in `claude-code-plugins/`, update the copy there too
4. Submit a pull request with a clear description of what changed and why

### Adding New Skills

If you want to add a new CRE analysis skill:

1. Follow the template structure used by existing skills (see any file in `skills/` for the pattern)
2. Include all required sections: When to Use, What You'll Need, Mission, Strategy, Output Format, Quality Checks, When Data is Missing, Confidence Scoring, Related Knowledge Bases
3. Place it in the appropriate department directory under `skills/`
4. Add it to the relevant Claude Code plugin in `claude-code-plugins/`
5. Update README.md and docs/SKILL-INDEX.md

### Updating Knowledge Bases

Knowledge base files contain formulas, benchmarks, and criteria. If you have updated industry data:

1. Cite your source for any benchmark or threshold changes
2. Preserve all existing formulas unless correcting an error
3. Update both the `knowledge/` file and any copies in `claude-code-plugins/`

## Code of Conduct

Be professional. These skills are used for real financial analysis. Accuracy matters.

## License

By contributing, you agree that your contributions will be licensed under the [Apache 2.0 License](LICENSE).
