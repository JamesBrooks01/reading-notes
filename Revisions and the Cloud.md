# Revisions and the Cloud

## Version Control

Version control allows you to more easily keep track of and revisit mulltiple versions of a file or set of files. With it you can easily revert changes, track how it's been modified and compare what's changed between versions. This allows mistakes to be easily fixed

Version Control was initially only a single database on a hard drive that stored the changes, then when the need for collaboration arrived, the database was placed on a server with multiple people being able to access and change things and was called Centralized Version Control(CVCS).
Then, they realized the vulnerability of a single server being that if it failed everything was gone. Thus, they created the Distributed Version Control(DVCS) which allowed the collaboraters to each have a copy of the database that they could push data to and pull from.

## So, What is Git?

Git is a DVCS that stores everything in snapshots, otherwise called a commit. Every time a changed version of a project is saved, Git stores a snapshot of the file and allows it to be referenced later. Git relies mostly on local operations, which allows projects to be worked on offline if necessary and every change applied to a file or directory is tracked by Git and due to how it's set up it minimizes the risk of damaged or lost files through transit.
Files in Git exist in three main states,
- Commited = Data is stored in local database
- Modified = Data has been chnaged but not commited
- Staged = Files set to bee commited in the next snapshot