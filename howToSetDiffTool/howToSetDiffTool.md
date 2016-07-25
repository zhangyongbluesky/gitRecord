How to set diff tool
=========================== 

##config path : 
C:\Users\rockiezhang\AppData\Local\GitHub\PortableGit_cf76fc1621ac41ad4fe86c420ab5ff403f1808b9\mingw32\etc  (rely on os system and must modify the global config)


##windows diff and merge init config:

[diff]
	tool = bc3
	algorithm = histogram

[difftool]
	prompt = false
[difftool "bc3"]`
	cmd = \"c:/program files (x86)/beyond compare 3/bcomp.exe\" \"$LOCAL\" \"$REMOTE\"
[difftool "p4"]
	cmd = \"c:/program files/Perforce/p4merge.exe\" \"$LOCAL\" \"$REMOTE\"
[difftool "vs2012"]
	cmd = \"c:/program files (x86)/microsoft visual studio 11.0/common7/ide/devenv.exe\" '//diff' \"$LOCAL\" \"$REMOTE\"
[difftool "vs2013"]
	cmd = \"c:/program files (x86)/microsoft visual studio 12.0/common7/ide/devenv.exe\" '//diff' \"$LOCAL\" \"$REMOTE\"

[merge]
	tool = bc3
[mergetool]
	prompt = false
	keepBackup = false
[mergetool "bc3"]
	cmd = \"c:/program files (x86)/beyond compare 3/bcomp.exe\" \"$LOCAL\" \"$REMOTE\" \"$BASE\" \"$MERGED\"
	trustExitCode = true
[mergetool "p4"]
	cmd = \"c:/program files/Perforce/p4merge.exe\" \"$BASE\" \"$LOCAL\" \"$REMOTE\" \"$MERGED\"
	
##use command
git difftool filename
git mergetool

