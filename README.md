# Individuell examination: Git & GitHub

## Fråga 1: Versionshantering vs vanliga filer

- För Godkänt (G): Vad är versionshantering och vad är den stora skillnaden mellan att spara en fil via editorns vanliga sparaknapp och att spara ändringar i Git?

- För Väl Godkänt (VG): Förklara vad som menas med att Git sparar en tidslinje av frysta ögonblicksbilder (commits). Vad bevisar det faktum att du när som helst kan klicka på din allra första commit på GitHub och fortfarande se alla tre TODO kvar i koden, trots att filen på din dator ser helt annorlunda ut idag?

### My Answer:

Version control is a way to keep track of changes in a project over time. When I save a file in VS Code, it saves my latest changes on my computer, but Git allows me to save different versions of my project as commits.

Each `commit` is like a frozen snapshot of the project at that moment and together they create a history of changes. For example, I can open my first commit on GitHub and still see all three TODO comments, even though I have removed them from my current code. This shows that Git keeps the older versions, so I can check what I changed or return to an earlier version if needed. I also learned that each commit has its own ID(commit hash). I can use that ID to find an older version of a file and restore it if my current file gets damaged, without changing the other files in my project.

## Fråga 2: Arbetsytan, Staging och Commits

- För Godkänt (G): Beskriv vad kommandona git status, git add och git commit gör i det dagliga arbetsflödet och när du kör dem.

- För Väl Godkänt (VG): Förklara relationen mellan arbetsytan (arket på skrivbordet), staging (kuvertet) och commit (arkivlådan). Förklara också varför Git protesterar med no changes added to commit om man har ändrat filen i editorn och försöker köra git commit direkt utan git add.

### My Answer:

I use `git status` to check which files are changed, staged or untracked before I make a commit.
I understand the working directory as a paper on my desk, where I make changes. When I use `git add`, I select the changes and put them into an envelope (staging). When I use `git commit -m "message"`, I save a snapshot of those staged changes in an archive box(local Git history).

If I change a file but try to commit without using `git add`, Git says `no changes added to commit` because the new changes are still on my desk and have not been put into the envelope.

I can summarize this as:

- **Desk** = Working directory

- **Envelope** = Staging area

- **Archive box** = Local commit history

- **Error explanation** = Nothing new was staged for the commit

## Fråga 3: Lådan hemma vs Montern på GitHub

- För Godkänt (G): Vad är skillnaden mellan mappen på din dator och repot på GitHub, och vad gör kommandot git push?

- För Väl Godkänt (VG): Förklara konceptet med de två rummen / minnesytorna (lådan hemma på datorn vs glasmontern på GitHub). Förklara varför git push svarar Everything up-to-date om du har ändrat i koden men glömt att staga och committa innan du kör push.

### My Answer:

My local repository is on my computer, while the remote repository is on GitHub. They are two seperate storage places, like a box at my home and a glass display on GitHub. I can change files and make commits locally without updating GitHub immediately.

When I use `git push`, Git sends my new local commits to GitHub. If I change my code but forget to stage and commit it, Git has no new commits to send and responds with `Everything up-to-date`. This means GitHub already has my commited history, but my working directory may still contain changes.
