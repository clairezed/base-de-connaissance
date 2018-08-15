# Git

Supprimer d'un repo un fichier gitignoré sur le tard et déjà pushé :
```bash
git rm --cached `git ls-files -i --exclude-from=.gitignore`
```

## Git commit standard

### Mike Foley

- Line Length: All lines must be <= 72 chars (URLs excluded). First line should be <= 50 chars. Second line must be blank.
- Tense: Message must use imperative present tense: "Fix bug" and not "Fixed bug" or "Fixes bug."
- Subject Period: Do not end your subject line with a period.
- Capitalize Subject: Begin all subject lines with a capital letter.
- Frat House: No offensive content.
- WIP: Do not commit WIPs to shared branches (disabled by default)

Cf [Fit commit hook](https://github.com/m1foley/fit-commit#who-decided-these-rules)

Exemple :
```bash
git commit -m 'Init project' -m $'- Base gemfile\n- DB config'    
```

ce qui donne :
```
Init project

- Base gemfile
- DB config
```

Sources :
- [Tim Pope's blog](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
- [The official Git documentation](https://git.kernel.org/pub/scm/git/git.git/tree/Documentation/SubmittingPatches?id=HEAD)
- [Chris Beams](https://chris.beams.io/posts/git-commit/)
- Multiline from cli : [Coderwall](https://coderwall.com/p/-rlneg/multi-line-git-commit-message-from-cli)
