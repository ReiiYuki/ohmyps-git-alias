# ohmyps-git-alias

Oh My Poweshell Git Alias

I'm falling in love with git alias in ohmyzsh but I can't use it in Windows. This is collection of ohmyzsh inspired git alias for `POWERSHELL!`

## Setup

1. Create or edit `profile.ps1` in `C:\Users\yourname\Documents` and your PowerShell location
    - Default PowerShell Location - `C:\Windows\System32\WindowsPowerShell\v1.0`
    - PowerShell7 Location - `C:\Program Files\PowerShell\7`
2. Add the following to `profile.ps1` in all location:
    ```
    function OhMyPSg{ & git $args }
    New-Alias -Name g -Value OhMyPSg
    function OhMyPSga{ & git add $args }
    New-Alias -Name ga -Value OhMyPSga
    function OhMyPSgaa{ & git add --all $args }
    New-Alias -Name gaa -Value OhMyPSgaa
    function OhMyPSgapa{ & git add --patch $args }
    New-Alias -Name gapa -Value OhMyPSgapa
    function OhMyPSgau{ & git add --update $args }
    New-Alias -Name gau -Value OhMyPSgau
    function OhMyPSgav{ & git add --verbose $args }
    New-Alias -Name gav -Value OhMyPSgav
    function OhMyPSgap{ & git apply $args }
    New-Alias -Name gap -Value OhMyPSgap
    function OhMyPSgb{ & git branch $args }
    New-Alias -Name gb -Value OhMyPSgb
    function OhMyPSgba{ & git branch -a $args }
    New-Alias -Name gba -Value OhMyPSgba
    function OhMyPSgbd{ & git branch -d $args }
    New-Alias -Name gbd -Value OhMyPSgbd
    function OhMyPSgbDel{ & git branch -D $args }
    New-Alias -Name gbDel -Value OhMyPSgbDel
    function OhMyPSgbl{ & git blame -b -w $args }
    New-Alias -Name gbl -Value OhMyPSgbl
    function OhMyPSgbnm{ & git branch --no-merged $args }
    New-Alias -Name gbnm -Value OhMyPSgbnm
    function OhMyPSgbr{ & git branch --remote $args }
    New-Alias -Name gbr -Value OhMyPSgbr
    function OhMyPSgbs{ & git bisect $args }
    New-Alias -Name gbs -Value OhMyPSgbs
    function OhMyPSgbsb{ & git bisect bad $args }
    New-Alias -Name gbsb -Value OhMyPSgbsb
    function OhMyPSgbsg{ & git bisect good $args }
    New-Alias -Name gbsg -Value OhMyPSgbsg
    function OhMyPSgbsr{ & git bisect reset $args }
    New-Alias -Name gbsr -Value OhMyPSgbsr
    function OhMyPSgbss{ & git bisect start $args }
    New-Alias -Name gbss -Value OhMyPSgbss
    function OhMyPSgcc{ & git commit -v $args }
    New-Alias -Name gcc -Value OhMyPSgcc
    function OhMyPSgc!{ & git commit -v --amend $args }
    New-Alias -Name gc! -Value OhMyPSgc!
    function OhMyPSgcn!{ & git commit -v --no-edit --amend $args }
    New-Alias -Name gcn! -Value OhMyPSgcn!
    function OhMyPSgca{ & git commit -v -a $args }
    New-Alias -Name gca -Value OhMyPSgca
    function OhMyPSgca!{ & git commit -v -a --amend $args }
    New-Alias -Name gca! -Value OhMyPSgca!
    function OhMyPSgcan!{ & git commit -v -a --no-edit --amend $args }
    New-Alias -Name gcan! -Value OhMyPSgcan!
    function OhMyPSgcans!{ & git commit -v -a -s --no-edit --amend $args }
    New-Alias -Name gcans! -Value OhMyPSgcans!
    function OhMyPSgcam{ & git commit -a -m $args }
    New-Alias -Name gcam -Value OhMyPSgcam
    function OhMyPSgcsm{ & git commit -s -m $args }
    New-Alias -Name gcsm -Value OhMyPSgcsm
    function OhMyPSgcbr{ & git checkout -b $args }
    New-Alias -Name gcbr -Value OhMyPSgcbr
    function OhMyPSgcf{ & git config --list $args }
    New-Alias -Name gcf -Value OhMyPSgcf
    function OhMyPSgcl{ & git clone --recurse-submodules $args }
    New-Alias -Name gcl -Value OhMyPSgcl
    function OhMyPSgclean{ & git clean -id $args }
    New-Alias -Name gclean -Value OhMyPSgclean
    function OhMyPSgpristine{ & git reset --hard && git clean -dffx $args }
    New-Alias -Name gpristine -Value OhMyPSgpristine
    function OhMyPSgcmaster{ & git checkout master $args }
    New-Alias -Name gcmaster -Value OhMyPSgcmaster
    function OhMyPSgcd{ & git checkout develop $args }
    New-Alias -Name gcd -Value OhMyPSgcd
    function OhMyPSgcmsg{ & git commit -m $args }
    New-Alias -Name gcmsg -Value OhMyPSgcmsg
    function OhMyPSgco{ & git checkout $args }
    New-Alias -Name gco -Value OhMyPSgco
    function OhMyPSgcount{ & git shortlog -sn $args }
    New-Alias -Name gcount -Value OhMyPSgcount
    function OhMyPSgcp{ & git cherry-pick $args }
    New-Alias -Name gcp -Value OhMyPSgcp
    function OhMyPSgcpa{ & git cherry-pick --abort $args }
    New-Alias -Name gcpa -Value OhMyPSgcpa
    function OhMyPSgcpc{ & git cherry-pick --continue $args }
    New-Alias -Name gcpc -Value OhMyPSgcpc
    function OhMyPSgcsave{ & git commit -S $args }
    New-Alias -Name gcsave -Value OhMyPSgcsave
    function OhMyPSgd{ & git diff $args }
    New-Alias -Name gd -Value OhMyPSgd
    function OhMyPSgdca{ & git diff --cached $args }
    New-Alias -Name gdca -Value OhMyPSgdca
    function OhMyPSgdcw{ & git diff --cached --word-diff $args }
    New-Alias -Name gdcw -Value OhMyPSgdcw
    function OhMyPSgdct{ & git describe --tags $(git rev-list --tags --max-count=1) $args }
    New-Alias -Name gdct -Value OhMyPSgdct
    function OhMyPSgds{ & git diff --staged $args }
    New-Alias -Name gds -Value OhMyPSgds
    function OhMyPSgdt{ & git diff-tree --no-commit-id --name-only -r $args }
    New-Alias -Name gdt -Value OhMyPSgdt
    function OhMyPSgdw{ & git diff --word-diff $args }
    New-Alias -Name gdw -Value OhMyPSgdw
    function OhMyPSgf{ & git fetch $args }
    New-Alias -Name gf -Value OhMyPSgf
    function OhMyPSgfa{ & git fetch --all --prune $args }
    New-Alias -Name gfa -Value OhMyPSgfa
    function OhMyPSgfo{ & git fetch origin $args }
    New-Alias -Name gfo -Value OhMyPSgfo
    function OhMyPSgg{ & git gui citool $args }
    New-Alias -Name gg -Value OhMyPSgg
    function OhMyPSgga{ & git gui citool --amend $args }
    New-Alias -Name gga -Value OhMyPSgga
    function OhMyPSggpur{ & ggu $args }
    New-Alias -Name ggpur -Value OhMyPSggpur
    function OhMyPSghh{ & git help $args }
    New-Alias -Name ghh -Value OhMyPSghh
    function OhMyPSgignore{ & git update-index --assume-unchanged $args }
    New-Alias -Name gignore -Value OhMyPSgignore
    function OhMyPSgit-svn-dcommit-push{ & git svn dcommit && git push github master:svntrunk $args }
    New-Alias -Name git-svn-dcommit-push -Value OhMyPSgit-svn-dcommit-push
    function OhMyPSgk{ & gitk --all --branches $args }
    New-Alias -Name gk -Value OhMyPSgk
    function OhMyPSgll{ & git pull $args }
    New-Alias -Name gll -Value OhMyPSgll
    function OhMyPSglg{ & git log --stat $args }
    New-Alias -Name glg -Value OhMyPSglg
    function OhMyPSglgp{ & git log --stat -p $args }
    New-Alias -Name glgp -Value OhMyPSglgp
    function OhMyPSglgg{ & git log --graph $args }
    New-Alias -Name glgg -Value OhMyPSglgg
    function OhMyPSglgga{ & git log --graph --decorate --all $args }
    New-Alias -Name glgga -Value OhMyPSglgga
    function OhMyPSglgmm{ & git log --graph --max-count=10 $args }
    New-Alias -Name glgmm -Value OhMyPSglgmm
    function OhMyPSglo{ & git log --oneline --decorate $args }
    New-Alias -Name glo -Value OhMyPSglo
    function OhMyPSglog{ & git log --oneline --decorate --graph $args }
    New-Alias -Name glog -Value OhMyPSglog
    function OhMyPSgloga{ & git log --oneline --decorate --graph --all $args }
    New-Alias -Name gloga -Value OhMyPSgloga
    function OhMyPSgmm{ & git merge $args }
    New-Alias -Name gmm -Value OhMyPSgmm
    function OhMyPSgmom{ & git merge origin/master $args }
    New-Alias -Name gmom -Value OhMyPSgmom
    function OhMyPSgmt{ & git mergetool --no-prompt $args }
    New-Alias -Name gmt -Value OhMyPSgmt
    function OhMyPSgmtvim{ & git mergetool --no-prompt --tool=vimdiff $args }
    New-Alias -Name gmtvim -Value OhMyPSgmtvim
    function OhMyPSgmum{ & git merge upstream/master $args }
    New-Alias -Name gmum -Value OhMyPSgmum
    function OhMyPSgma{ & git merge --abort $args }
    New-Alias -Name gma -Value OhMyPSgma
    function OhMyPSgpp{ & git push $args }
    New-Alias -Name gpp -Value OhMyPSgpp
    function OhMyPSgpd{ & git push --dry-run $args }
    New-Alias -Name gpd -Value OhMyPSgpd
    function OhMyPSgpf{ & git push --force-with-lease $args }
    New-Alias -Name gpf -Value OhMyPSgpf
    function OhMyPSgpf!{ & git push --force $args }
    New-Alias -Name gpf! -Value OhMyPSgpf!
    function OhMyPSgpoat{ & git push origin --all && git push origin --tags $args }
    New-Alias -Name gpoat -Value OhMyPSgpoat
    function OhMyPSgpu{ & git push upstream $args }
    New-Alias -Name gpu -Value OhMyPSgpu
    function OhMyPSgpvv{ & git push -v $args }
    New-Alias -Name gpvv -Value OhMyPSgpvv
    function OhMyPSgr{ & git remote $args }
    New-Alias -Name gr -Value OhMyPSgr
    function OhMyPSgra{ & git remote add $args }
    New-Alias -Name gra -Value OhMyPSgra
    function OhMyPSgrb{ & git rebase $args }
    New-Alias -Name grb -Value OhMyPSgrb
    function OhMyPSgrba{ & git rebase --abort $args }
    New-Alias -Name grba -Value OhMyPSgrba
    function OhMyPSgrbc{ & git rebase --continue $args }
    New-Alias -Name grbc -Value OhMyPSgrbc
    function OhMyPSgrbd{ & git rebase develop $args }
    New-Alias -Name grbd -Value OhMyPSgrbd
    function OhMyPSgrbi{ & git rebase -i $args }
    New-Alias -Name grbi -Value OhMyPSgrbi
    function OhMyPSgrbm{ & git rebase master $args }
    New-Alias -Name grbm -Value OhMyPSgrbm
    function OhMyPSgrbs{ & git rebase --skip $args }
    New-Alias -Name grbs -Value OhMyPSgrbs
    function OhMyPSgrev{ & git revert $args }
    New-Alias -Name grev -Value OhMyPSgrev
    function OhMyPSgrh{ & git reset $args }
    New-Alias -Name grh -Value OhMyPSgrh
    function OhMyPSgrhh{ & git reset --hard $args }
    New-Alias -Name grhh -Value OhMyPSgrhh
    function OhMyPSgrm{ & git rm $args }
    New-Alias -Name grm -Value OhMyPSgrm
    function OhMyPSgrmc{ & git rm --cached $args }
    New-Alias -Name grmc -Value OhMyPSgrmc
    function OhMyPSgrmv{ & git remote rename $args }
    New-Alias -Name grmv -Value OhMyPSgrmv
    function OhMyPSgrrm{ & git remote remove $args }
    New-Alias -Name grrm -Value OhMyPSgrrm
    function OhMyPSgrs{ & git restore $args }
    New-Alias -Name grs -Value OhMyPSgrs
    function OhMyPSgrset{ & git remote set-url $args }
    New-Alias -Name grset -Value OhMyPSgrset
    function OhMyPSgrss{ & git restore --source $args }
    New-Alias -Name grss -Value OhMyPSgrss
    function OhMyPSgru{ & git reset -- $args }
    New-Alias -Name gru -Value OhMyPSgru
    function OhMyPSgrup{ & git remote update $args }
    New-Alias -Name grup -Value OhMyPSgrup
    function OhMyPSgrv{ & git remote -v $args }
    New-Alias -Name grv -Value OhMyPSgrv
    function OhMyPSgsb{ & git status -sb $args }
    New-Alias -Name gsb -Value OhMyPSgsb
    function OhMyPSgsd{ & git svn dcommit $args }
    New-Alias -Name gsd -Value OhMyPSgsd
    function OhMyPSgsh{ & git show $args }
    New-Alias -Name gsh -Value OhMyPSgsh
    function OhMyPSgsi{ & git submodule init $args }
    New-Alias -Name gsi -Value OhMyPSgsi
    function OhMyPSgsps{ & git show --pretty=short --show-signature $args }
    New-Alias -Name gsps -Value OhMyPSgsps
    function OhMyPSgsr{ & git svn rebase $args }
    New-Alias -Name gsr -Value OhMyPSgsr
    function OhMyPSgss{ & git status -s $args }
    New-Alias -Name gss -Value OhMyPSgss
    function OhMyPSgst{ & git status $args }
    New-Alias -Name gst -Value OhMyPSgst
    function OhMyPSgstaa{ & git stash apply $args }
    New-Alias -Name gstaa -Value OhMyPSgstaa
    function OhMyPSgstc{ & git stash clear $args }
    New-Alias -Name gstc -Value OhMyPSgstc
    function OhMyPSgstd{ & git stash drop $args }
    New-Alias -Name gstd -Value OhMyPSgstd
    function OhMyPSgstl{ & git stash list $args }
    New-Alias -Name gstl -Value OhMyPSgstl
    function OhMyPSgstp{ & git stash pop $args }
    New-Alias -Name gstp -Value OhMyPSgstp
    function OhMyPSgsts{ & git stash show --text $args }
    New-Alias -Name gsts -Value OhMyPSgsts
    function OhMyPSgstu{ & git stash --include-untracked $args }
    New-Alias -Name gstu -Value OhMyPSgstu
    function OhMyPSgstall{ & git stash --all $args }
    New-Alias -Name gstall -Value OhMyPSgstall
    function OhMyPSgsu{ & git submodule update $args }
    New-Alias -Name gsu -Value OhMyPSgsu
    function OhMyPSgts{ & git tag -s $args }
    New-Alias -Name gts -Value OhMyPSgts
    function OhMyPSgtv{ & git tag | sort -V $args }
    New-Alias -Name gtv -Value OhMyPSgtv
    function OhMyPSgunignore{ & git update-index --no-assume-unchanged $args }
    New-Alias -Name gunignore -Value OhMyPSgunignore
    function OhMyPSgup{ & git pull --rebase $args }
    New-Alias -Name gup -Value OhMyPSgup
    function OhMyPSgupv{ & git pull --rebase -v $args }
    New-Alias -Name gupv -Value OhMyPSgupv
    function OhMyPSgupa{ & git pull --rebase --autostash $args }
    New-Alias -Name gupa -Value OhMyPSgupa
    function OhMyPSgupav{ & git pull --rebase --autostash -v $args }
    New-Alias -Name gupav -Value OhMyPSgupav
    function OhMyPSglum{ & git pull upstream master $args }
    New-Alias -Name glum -Value OhMyPSglum
    function OhMyPSgwch{ & git whatchanged -p --abbrev-commit --pretty=medium $args }
    New-Alias -Name gwch -Value OhMyPSgwch
    ```
3. Enjoy git alias in PowerShell!
