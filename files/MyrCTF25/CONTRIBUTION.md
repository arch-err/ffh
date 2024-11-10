# Contribution to MyrCTF 2025
First off, if you decide to contribute to MyrCTF 2025 you have to keep in mind that all of the challenges, challenge data, and author handles will be made public via a git repo at a later date.


## Contact
To submit challenges you can contact us and share your work, either via e-mail at [archer@jesber.xyz](mailto:archer@jesber.xyz) or contact **arch-err** via discord.


## Technical Requirements
If the following requirements are not met your challenge will most likely not even be considered for *MyrCTF 2025*. Make sure too meet them at the best of your abillity.

### Template
A challenge template repo can be found on [arch-err's GitHub](https://github.com/arch-err/ctf-challenge-creation-template)

### Requirements
- **Flag Format**: The flag must match the RegEx `MyrCTF\{[A-Za-z0-9_\.\|-]{8,32}\}`
- **Challenge Metadata**: Create and fill out the following file (named `challenge.yaml`):
```yaml
name: "Challenge Name"
author: "author"
category: category
description: This is a sample description
difficulty: <a range from 1-10, 1 being very easy and 10 being incredibly difficult>
attribution: Written by [author](https://github.com/my-name/)

topics:
    - information disclosure
    - buffer overflow
    - memory forensics

files:
    - dist/source.py

# Flags specify answers that your challenge use. You should ONLY provide  one.
flags:
    # A static, case-insensitive, flag
    - {
        type: "static",
        content: "MyrCTF{3xampl3}",
        data: "case_insensitive",
    }
    # A regex, case-sensitive, flag
    - {
        type: "regex",
        content: "(.*)STUFF(.*)",
        data: "case_sensitive",
    }
```
- **Files (IF NECESSARY)**: Create a directory called `files` that holds files given to the player when starting the challenge. Should be the same as listed under `challenge.yml > files`
- **Solution**: A file, `SOLVE.md`, should be given along with any scripts/code needed to solve the challenge. This means you MUST be able to solve the challenge yourself. If you've used online tools to solve the challenge, make sure to include links.
- **Generation (OPTIONAL)**: A file, `generation/GENERATE.md`, and any scripts you may have used to generate your challenge.
- Everything should be packaged in a 7z-archive with the name `<challenge_name>.7z`.
