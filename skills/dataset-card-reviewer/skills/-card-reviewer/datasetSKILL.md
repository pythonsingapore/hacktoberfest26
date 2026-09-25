---
name: dataset-card-reviewer
description: Checks a small dataset card for name, license and tasks fields and reports missing or empty fields. Use when preparing a simple open dataset description for review.
license: Apache-2.0
---

# Review a dataset card

This example reviews a plain YAML, JSON or Python-dictionary-style card. It does not certify legal rights, dataset safety or license compatibility.

1. Read the card. Never execute untrusted code in the card. If the format cannot be parsed safely, report that and ask for a readable card.
2. Check whether `name` is a nonempty string, `license` is a nonempty string, and `tasks` is a nonempty list of nonempty strings. Report missing and empty fields separately.
3. Report the present values and the checks you actually performed. Do not claim a license is valid or the data may be redistributed merely because the field exists.
4. Suggest only the smallest fix needed. Ask the maintainer before changing a published dataset or opening a PR.

Sample input: `{ "name": "toy-cards", "license": "cc-by-4.0", "tasks": ["text-classification"] }`
Expected result: all three required fields are present and nonempty; license rights not verified.
Edge case: `{ "name": "toy-cards", "tasks": [] }` -> license missing, tasks empty.
