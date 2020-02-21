---
description: Instructions for updating git config to accept long path values.
---

# Updating Git Config \(Windows Only\)

If you have a Windows machine complete the following configuration steps to avoid an issue with long file names in the future:

1. Open up Git Bash and run as administrator. \(This can be done by typing in git bash to the search bar and right clicking the icon and selecting run as administrator from the drop down menu.\)
2. Type in the following command:  

```bash
git config --system core.longpaths true
```

If these steps have been completed successfully there should be no output.

To test if this configuration has been successful, type in the following command:

```bash
git config --system core.longpaths
```

There should be the value `true` printed in the bash window.

If you have not yet completed a Git Bash installation follow these instructions:

**Git & Git Bash**

Coders depend on this tool for version control; the process of logging the development of programs and applications. This comes in handy during collaborative programming, when teams of programmers change, add and remove code throughout a project’s directory. This process would be chaotic without Git.

The installation also includes Git Bash or Bash for short. You'll be using this command line terminal throughout the course and during the rest of these instructions.

1. Go to Git download page: [https://git-scm.com/downloads](https://git-scm.com/downloads). Click on the download for your computer.

![](https://raw.githubusercontent.com/coding-boot-camp/enterprise-prework-assets/master/assets/Install-GitWindows1.png)

1. Run through the installation file. Make sure you check off the right boxes as shown in these four images.
2. Save Git to the desktop \(this should save Git Bash to your desktop too\).

![](https://raw.githubusercontent.com/coding-boot-camp/enterprise-prework-assets/master/assets/Install-GitWindows2.1.png)

* Use Git from the Windows Command Prompt.

![](https://raw.githubusercontent.com/coding-boot-camp/enterprise-prework-assets/master/assets/Install-GitWindows2.2.png)

* Checkout as-is.

![](https://raw.githubusercontent.com/coding-boot-camp/enterprise-prework-assets/master/assets/Install-GitWindows2.3.png)

* Use Windows' default console window.

![](https://raw.githubusercontent.com/coding-boot-camp/enterprise-prework-assets/master/assets/Install-GitWindows2.4.png)

