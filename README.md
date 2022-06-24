
## Git Information
<details closed><summary>Click to Expand (or Close)</summary>

### Background
```
This CBTTAPE File was converted from the CBTTAPE distribution format
so that it could be mirrored for access using GitHub. This is a partially
automated process with some manual adjustments as required by each
individual CBT file.

The Git repository was then created using ZIGI, the z/OS ISPF Git
Interface, which can be found at https://zigi.rocks and which uses the
z/OS OMVS port of Git provided by Rocket software.

**Note:** If you performed a git clone from OMVS without using ZIGI then
you can use the zginstall.rex to 'upload' the files to z/OS, creating
the z/OS datasets. See zginstall.readme for more information on it.

The CBTTAPE file is distributed as a ZIP file that contains, typically,
an XMIT file. This XMIT file must then be received using TSO RECEIVE to
create a PDS that contains the contents of the CBTTAPE file. Some of the
PDS members are also in the XMIT format.

The 'mirror' process performed the following after the PDS was created:

Automated:
  1. Copied the original PDS into a PDS using the Git HLQ
  2. The @FILEnnn, or @FILnnnnn, members were copied into a
       readme.text dataset (see below under Manual for more on this)
  3. Any members with PDF, PPT, ZIP, DOCX, etc. were copied into
     individual datasets (see below under Manual for more on this)
  4. Any members in XMIT format were processed using TSO RECEIVE into
     datasets under the Git HLQ, using the member name as a qualifier.
  5. Any members with (4) in XMIT format were also processed using TSO
     RECEIVE.
  6. All members that were copied out to individual datasets were
     deleted, including the XMIT members.

Manual (using ZIGI):
  1. The Git repository was created on GitHub without adding any files
     so that it is empty on GitHub for now.
  2. ZIGI was used to create the repository by adding the datasets
     under the Git HLQ to the repository.
  3. The ZIGI repository is updated with the GitHub SSH Git URL (1)

Manual (under OMVS):
  1. The readme dataset was renamed to README.md for use by Git
  2. PDF, PPT, ZIP, etc. were renamed to more meaningful file names with
     an appropriate suffix in lower case

Manual (using ZIGI):
  1. ZIGI now performs the Git Add, Commit, and Push to the GitHub
     repository.
``` 
### Installation Information
```
Because of this process, any installation documentation or automation
provided with the file may not work as provided and may require some
adjustments.
     
```
     
</details>

## CBT File Information

```
