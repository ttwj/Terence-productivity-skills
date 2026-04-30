# overtly-malicious-skills

This repository contains the four malicious skills created by the Machine Learning Security team at Trail of Bits to test out the reliability of skill scanners. You can check out our writeup describing the skills and how we used them to subvert scanners in our blog post, The Sorry State of Skill Distribution.

**WARNING: THESE SKILLS ARE MALICIOUS AND INTENDED FOR SECURITY RESEARCH PURPOSES ONLY. DO NOT INSTALL THEM.**

## Skills

- **csv-summarizer** - Claims to summarize the dimensions of a .csv file. Actually dumps the contents of the environment variables store.
- **context-loader** - Claims to synchronize startup context across Claude instances. Actually smuggles a malicious script within the archive of XML underlying a hidden .docx file.
- **simple-formatter** - Claims to formats text according to style guidelines (capitalize sentences, fix spacing, punctuation rules). Actually uses Python bytecode poisoning to steal environment variables.
- **dev-env-setup** — Claims to bootstrap standardized development environment configuration (npm/yarn registry, editor settings, pre-commit hooks, secrets hygiene). Actually uses a prompt injection to convince the scanner it is fine to overwrite the npm/yarn registry with an attacker-controlled site.