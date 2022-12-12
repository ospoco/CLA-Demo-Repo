# OSPO-Demo-Repo

One recommendation that we frequently make is to use Git/GitHub to store and manage OSPO
documents, including CLAs and other artifacts needed for legal compliance. This repository 
illustrates one method of organizing such a repo.

This repo is customizable. The important thing is that it stores all the information together
and the files are primarily text, allowing developers to easily update them.

# Parts of the repo

This repo has two parts: "contributing" (for upstream community contributions) and "using"
(for internal use, including use that may go into a product).

## Contributing (upstream)

The contributing directory is designed around a series of project directories, each identified by 
the domain and path portions of the primary URL for the project. This allows the list of projects that 
are ready for contribution to be easily determined - just look at the list.

Within each project directory are a few files.

**CONTRIBUTING.md:** The CONTRIBUTING.md file is a text description of the current status of this project vis-a-vis
the organization. Does the product use a CLA? A DCO? Does it just require an inbound license?

If the project requires an inbound license or DCO, the CONTRIBUTING file can record who provided
the authority for developers to put the license on their contributions or sign the DCO.

This file can also include miscellaneous instructions that may be useful for contributions. For example,
Google-managed open source projects usually manage their approvals using a Google Groups mailing list.
This file can include the name and location of the group and who is administering it for your organization.

**INFO.md:** The INFO file contains metadata about the project. What is the full name? The URL? The license?
We suggest having one value per line and using the [Trove classifier](https://peps.python.org/pep-0301/#distutils-trove-classification) format
or an ini-style format (name = value). 

What you put in the INFO file is up to you, but we recommend having a common set of identifiers so 
that it is easy to gather and compare information. However, the format is intentionally flexible so
that additional information can be added.

**CLA.pdf (or similar):** Many projects use a manual signing procedure or Docusign for their CLAs. Save
a copy of the CLA in this directory. If the project uses some other procedure that doesn't produce an output,
use this file to describe when and by whom the CLA was signed.

**approved_contributors.md:** Many projects will want to track approved contributors by matching them to
either email addresses, Github usernames, or similar. By using a Markdown-formatted file, the information for
each contributor is kept on a single row, and many piecese of software (including Github) will format it 
as a nice-looking table.

These aren't the only files that can go in this directory. If your organization has a special need, you can 
add something more.

## Using (downstream)

One of the hardest things to do is keeping track of what open source you are using, what policy decisions have been
made, and any exceptions. Keeping this information up to date should probably be handled via an automatic
scanning and update process - but having it in one place is very useful.

This method of managing open source package use boils everything down to three lists: *approved*, *exceptions*, and
*prohibited.* The names are self-explanatory. It makes it easy for developers to get self-service information - to 
know if something is allowed (or has been allowed) is just a matter of looking at a file.

These, like the approved_contributors files, is a Markdown-formatted file. We recommend the use of a table to keep
any necessary information together so that it is both easy to view and easy to update. Need exta information for
your organization? Just add a column to the table.

If for some reason these files are not enough, any of these can be turned into a directory and additional files or 
metadata can be easily stored along side the project information.

# Updating the repo

One benefit of using Git/Github to manage this information is that it provides a built-in developer-friendly method
of interaction. It turns many of the administrative tasks into ordinary, every-day actions. Need an update? A developer 
can open an issue and make a pull request. 


