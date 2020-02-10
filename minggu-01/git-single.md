OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents
$ git --version
git version 2.10.1.windows.1

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents
$ pwd
/c/Users/OWNER/Documents

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents
$ git clone https://github.com/trimariaas27/tekn-cloud-computing.git
Cloning into 'tekn-cloud-computing'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents
$ git
usage: git [--version] [--help] [-C <path>] [-c name=value]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add        Add file contents to the index
   mv         Move or rename a file, a directory, or a symlink
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect     Use binary search to find the commit that introduced a bug
   grep       Print lines matching a pattern
   log        Show commit logs
   show       Show various types of objects
   status     Show the working tree status

grow, mark and tweak your common history
   branch     List, create, or delete branches
   checkout   Switch branches or restore working tree files
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   merge      Join two or more development histories together
   rebase     Reapply commits on top of another base tip
   tag        Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch      Download objects and refs from another repository
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents
$ cd C:\Users\OWNER\Documents\tekn-cloud-computing
bash: cd: C:UsersOWNERDocumentstekn-cloud-computing: No such file or directory

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents
$ git config --global user.name "trimariaas27"

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents
$ git config --global user.email mariatrias084@gmail.com

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents
$ git config --list
core.symlinks=false
core.autocrlf=true
core.fscache=true
color.diff=auto
color.status=auto
color.branch=auto
color.interactive=true
help.format=html
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
diff.astextplain.textconv=astextplain
rebase.autosquash=true
credential.helper=manager
user.name=trimariaas27
user.email=mariatrias084@gmail.com

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents
$ git init
Initialized empty Git repository in C:/Users/OWNER/Documents/.git/

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents (master)
$ git add *
warning: LF will be replaced by CRLF in Adobe/Premiere Pro/11.0/Profile-OWNER/Adobe Premiere Pro Prefs.
The file will have its original line endings in your working directory.
warning: LF will be replaced by CRLF in Adobe/Premiere Pro/11.0/Profile-OWNER/Effect Presets and Custom Items.prfpset.
The file will have its original line endings in your working directory.
warning: LF will be replaced by CRLF in Adobe/Premiere Pro/11.0/Profile-OWNER/Media Browser Provider Exception.
The file will have its original line endings in your working directory.
warning: LF will be replaced by CRLF in Adobe/Premiere Pro/11.0/Profile-OWNER/Recent Directories.
The file will have its original line endings in your working directory.
warning: LF will be replaced by CRLF in Adobe/Premiere Pro/11.0/Profile-OWNER/SharedView Column Settings.
The file will have its original line endings in your working directory.

dir



OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents (master)
$

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents (master)
$ dir
~$\ Chan\ Kim\ &\ Renee\ Mauborgne\ -\ BLUE\ OCEAN\ SHIFT\ BEYOND\ COMPETING\ (BM).docx  991125O414009240919Materi\ RO\ Ganjil\ 1920.zip  KULIAH\ AKAKOM          My\ Videos
~$GAS\ 6\ PRAKTIK\ PEMROGRAMAN\ BERORIENTASI\ OBJEK.docx                                 Adobe                                            Maria\ Tri\ Astuti      NetBeansProjects
~$GAS\ spk\ teori.docx                                                                   Bandicam                                         materi.txt              python
~$ku\ praktik\ akuntansi\ .doc                                                           Corel                                            Music\ -\ Shortcut.lnk  SafeNet\ Sentinel
~$llo\ Gusy.docx                                                                         Custom\ Office\ Templates                        My\ Data\ Sources       Scanned\ Documents
~$RKOM\ DAN\ IMK.docx                                                                    desktop.ini                                      My\ Music               tekn-cloud-computing
~$RTEMUAN\ 10.docx                                                                       Downloads\ -\ Shortcut.lnk                       My\ Palettes            Templates
~$ta\ yang\ diperlukan\ pada\ system.doc                                                 Fax                                              My\ Pictures            WORK

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents (master)
$


OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents (master)
$ dir
~$\ Chan\ Kim\ &\ Renee\ Mauborgne\ -\ BLUE\ OCEAN\ SHIFT\ BEYOND\ COMPETING\ (BM).docx  991125O414009240919Materi\ RO\ Ganjil\ 1920.zip  KULIAH\ AKAKOM          My\ Videos
~$GAS\ 6\ PRAKTIK\ PEMROGRAMAN\ BERORIENTASI\ OBJEK.docx                                 Adobe                                            Maria\ Tri\ Astuti      NetBeansProjects
~$GAS\ spk\ teori.docx                                                                   Bandicam                                         materi.txt              python
~$ku\ praktik\ akuntansi\ .doc                                                           Corel                                            Music\ -\ Shortcut.lnk  SafeNet\ Sentinel
~$llo\ Gusy.docx                                                                         Custom\ Office\ Templates                        My\ Data\ Sources       Scanned\ Documents
~$RKOM\ DAN\ IMK.docx                                                                    desktop.ini                                      My\ Music               tekn-cloud-computing
~$RTEMUAN\ 10.docx                                                                       Downloads\ -\ Shortcut.lnk                       My\ Palettes            Templates
~$ta\ yang\ diperlukan\ pada\ system.doc                                                 Fax                                              My\ Pictures            WORK

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents (master)
$ dir tekn-cloud-computing/
minggu-01  README.md

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents (master)
$ cd tekn-cloud-computing/

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents/tekn-cloud-computing (master)
$ git init
Reinitialized existing Git repository in C:/Users/OWNER/Documents/tekn-cloud-computing/.git/

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents/tekn-cloud-computing (master)
$ git add *

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents/tekn-cloud-computing (master)
$ git commit -m "Upload minggu-01"
[master 6128e9f] Upload minggu-01
 5 files changed, 29 insertions(+)
 create mode 100644 minggu-01/README.md
 create mode 100644 minggu-01/gambar-01.PNG
 create mode 100644 minggu-01/images 1.PNG
 create mode 100644 minggu-01/images 2.PNG
 create mode 100644 minggu-01/rangkuman-cloud-computing.md

OWNER@DESKTOP-I4RVD75 MINGW64 ~/Documents/tekn-cloud-computing (master)
$ git push -u origin master
Fatal: HttpRequestException encountered.
   An error occurred while sending the request.
Username for 'https://github.com': trimariaas27
Counting objects: 7, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 188.81 KiB | 0 bytes/s, done.
Total 7 (delta 0), reused 0 (delta 0)
To https://github.com/trimariaas27/tekn-cloud-computing.git
   59a464a..6128e9f  master -> master
Branch master set up to track remote branch master from origin.
