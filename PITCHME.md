
### Why Git?

- masterthesis.docx
- masterthesis_v1.docx
- masterthesis_FINAL.docx
- masterthesis_FINAL_FINAL.docx

---

![Help](https://media.giphy.com/media/phJ6eMRFYI6CQ/giphy.gif)

---

### Version Control to the Rescue!
- Example: This presentation 

---


# Download the data - Fork und Clone

---

### Fork und Clone


@box[bg-blue text-black rounded](Repository#"A Git repository is a virtual storage of your project. It allows you to save versions of your code, which you can access when needed." ([Source](https://www.atlassian.com/git/tutorials/setting-up-a-repository)))

@box[bg-blue text-black rounded](Fork#"A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project." ([Source](https://help.github.com/articles/fork-a-repo/))

---

### Hands On 1 - Fork und Clone
 
#### Mona

@ol

- [https://github.com/friep/git-our-shit-together/](https://github.com/friep/git-our-shit-together/): Fork (oben rechts)
- `https://github.com/{USERNAME}/git-our-shit-together` öffnet sich
- unter Settings->Collaborators Grace hinzufügen

@olend

---

### Hands On 1 - Fork und Clone

#### Mona & Grace

![Git clone](images/gitclone.png)

@ol

- Gitkraken Clone Repo -> Clone with URL
- Kopierten Link unter URL eintragen

@olend


---

### Oh!

![Git clone error](images/gitclone_auth_error.png)


---

### Oh! - Nicht-Gitkraken

```
Cloning into 'git-our-shit-together'...
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```

---

### SSH 

@ul 

- Download: 
    - prinzipell jede*r @fa[lock-open] über `https` --> @fa[github]: @fa[check]
    - `ssh`: vorherige Einrichtung ntowendig --> @fa[github]: @fa[question]
- Upload: nur authentifizierte Personen @fa[lock]
- --> @fa[github]: @fa[question]

@ulend

---

### Authentification - Passwort

- bei jedem Push GitHub Passwort eingeben
- beachte: clone `https://...` 

![Git clone](images/gitclone_https.png)

--- 

### Authentification - SSH
- public key, private key cryptography (siehe z.B. [Youtube](https://www.youtube.com/watch?v=AQDCe585Lnc))
- nur einmal einrichten -> 
- clone `ssh://...`

---

### Hands On 1.1: Gitkraken mit Github verbinden

@ol

- Gitkraken Profil (rechts oben)
- Preferences->Authentification->GitHub
- connect to GitHub
- Generate SSH key and add to GitHub

@olend

---

# Daten speichern - Add und Commit 

---
### Commit

@box[bg-blue text-black rounded](Commit#"A commit is the Git equivalent of a "save".[...] Git committing is an operation that acts upon a collection of files and directories." ([Source](https://www.atlassian.com/git/tutorials/saving-changes))

--> Commit = Ein "Speicherpunkt" in Git. 

--- 

### Commit history

![Git commits](images/gitkraken_commits.png)

---

### Go back in time! 

![Time Machine](https://media.giphy.com/media/Vqvr9BGv1vhDi/giphy.gif)

---

### Hands On 2 - Go back in time 

@ol

- `reset master to this commit`
- spiele mit: `hard`, `mixed`, `soft`
- `fast forward master to origin/master` (oberster commit)

@olend


---

### Commit

- Commit hält **Veränderungen** gegenüber dem vorherigen Commit fest
    - Änderungen von Dateien
    - Neuerstellung von Dateien
    - Löschung von Dateien
    - Umbenennung von Dateien
- ein Commit kann mehrere Änderungen beinhalten

---

### Adding und Staging Area 

![Staging Area](images/staging.png)

(Source: [https://git-scm.com/about/staging-area](https://git-scm.com/about/staging-area))

---

### Hands On 3 - einen Commit machen 

Grace + Mona

@ol

-  Change stuff!
- **GIT ADD** von den "Unstaged Files" Dateien **GIT ADD**en, die man in Git "speichern" möchte. 
- (halbwegs) aussagekräftige Commit Message schreiben
- **GIT COMMIT** 

@olend

---

![](https://i.gifer.com/XtFT.gif)

---


### Git quizzed!

![Lokal](images/git_workflow_lokal_without_solution.png)

---

### Git quizzed!


![Lokal](images/git_workflow_lokal_with_solution.png)

--- 

# Daten syncen - Push und Pull

---


### Git  Hosting

- Die Cloud! z.B.

@fa[gitlab]
@fa[github]

---

### Git Lokal und Git Remote 

... what? 

**Lokal**: dein PC
**Remote**: in der Cloud (GitHub, GitLab, ...)

![Gitkraken Lokal Remote](images/gitkraken_remote_lokal.png)

---


### Sync: Git Pull und Git Push

- Git Pull: neue Commits von GitHub downloaden
- Git Push: lokal erstellte Commits nach GitHub hochladen

---

### Sync: Git Pull und Git Push

![Push Pull](images/push_pull.png)

---

![Push the button](https://media.giphy.com/media/139lMwJ9ow7bKE/giphy.gif)

--- 


### Hands On 4 - Pull und Push

@ol

- Grace: Push 
- Mona: Pull 
- Mona: Push 
- Grace: Pull

@olend

--- 

### Git quizzed!

![Push Pull](images/git_workflow_with_github_without_solution.png)

--- 


### Git quizzed!

![Push Pull](images/git_workflow_with_github_with_solution.png)

---

# When things go wrong...

---

![git google](images/giterrors.png)

---

![xccd](images/xkcd_comic.png)


---

### When things go wrong...

@ol

- so lange nichts gepusht ist, alles (halbwegs) gut
    - oft committen!
- zur Not: Codestand sichern und neu clonen 

@olend 


--- 

### Git stash

@box[bg-blue text-black rounded](Stash#"git stash temporarily shelves (or stashes) changes you've made to your working copy so you can work on something else, and then come back and re-apply them later on. Stashing is handy if you need to quickly switch context and work on something else, but you're mid-way through a code change and aren't quite ready to commit". ([Source](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)))

---

### Git stash

![stash](https://media.giphy.com/media/l0HlxJfVUKhtR8Jna/giphy.gif)

--> put it away for now!

---

### Git stash bei merge conflicts

@ol

- git stash
- git pull
- apply stash 
- solve merge conflicts 
- (delete stash)

@olend


---

### Hands on 5: Merge conflicts

---

# mit GitHub arbeiten


---

### Issues

@ul

- issues: Todos / Bugs / Ideen
- jeder issue hat eine Nummer
- #issueno in commit message verknüpft commit mit issue

@ulend

---

### Hands On 4: Issue

@ol

- Mona: Issue erstellen: "Grace's LieblingsGIF fehlt"
- Grace: füge der Präsentation eine neue Folie hinzu mit deinem Lieblingsgif (giphy -> copy link)
- Grace: add + commit. verlinke issue Nummer in der commit message (#issueno)
- Grace: push
- Mona: Issue neu laden (STRG+R)

@olend

---

# Branches

---


[picture of complicated gitkraken with a lot of branches]

---

![Come on](https://media.giphy.com/media/HfFccPJv7a9k4/giphy.gif)

---


### Branches

@box[bg-blue text-black rounded](Branch#A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. You can think of them as a way to request a brand new working directory, staging area, and project history. [Source](https://www.atlassian.com/git/tutorials/using-branches))

---

### Branches

@box[bg-blue text-black rounded](Checkout#The git checkout command lets you navigate between the branches created by git branch. Checking out a branch updates the files in the working directory to match the version stored in that branch, and it tells Git to record all new commits on that branch. Think of it as a way to select which line of development you’re working on. [Source](https://www.atlassian.com/git/tutorials/using-branches/git-checkout))

---

### Why branches?

@ul

- "master" branch frei von unfertigem Code halten
- unabhängige Entwicklung von Code ("feature branches")
- Experimente

@ulend

---

### Branches Workflow

@ol

- Branch erstellen
- normal weiterarbeiten (pull-commit-push cycles)
- (optional: merge andere branches in deinen branch um Updates zu bekommen)
- merge Branch in master branch 

@olend

---

### Merging branches

- Rechtsclick auf branch name / master
- hängt davon ab, wer "weiter vorne" ist (?)
    - wenn neue commits auf master: merge master into #1-add-branch-slides -> branch wird geupdatet
    - wenn neue commits auf branch: merge #1-add-branch-slides into master -> master wird geupdatet



---

### Branches Fazit

@ul

- besonders nützlich bei Kollaboration
- Entwicklung von Packages 
- Relevanz für Datenprojekte (?)
 -test text
 
@ulend

---

# Das wars. 

### gerne den Tag über fragen! 