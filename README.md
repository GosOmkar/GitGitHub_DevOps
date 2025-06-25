# History how does git came what is Git?
to basically kya hua ekdin linux k founder Linux storeworls    was making some code and next day he changed on that that but fre days lates thought ki yaar mera tho previous version code was good but unke paas tho purana code tha nehi so unhoine ekdin ekdin ek tracking system banaya jiska naam unone diya Global  information Tracking so that he can get the code changes using a version 2,version 2 type system this global information traccking in known as Git which is use as a versioncontrol system.
 So git is tracker tool wo aapki code code ho histry ko maintain karne deta h.
 Fir duniya is cheez ko dekha and bataya ki linux master Linus dstoreworld ne tho badiya ekta system nikala av hum log v isko use karke aapna aapna platform banayenge named github,gitlab,bitbucket,AWX code commit , Asure repo jiska main hub technology tha git.
 Git is version coltrol system.mujko agar kaviv purane version m jana h tho through this git VCM we can easiuly do that.
 

 # File System vs Version Control System
 File system - local m store hota h , kab banaya uska date aata h , author created by aata h,but kisne edit kiya wo nehi rehta,agar edit kiya h tho uska version deta h , kuch delet hota h wo recover nehi kar sakte h 
 VCS - Yea sab kuch deta h ,local and remote dono p hi raksakta hu , history bata deta h 


## file system to version control system :
 mere file system m ek folder h jihar kuchg text file or some importan files is there. av yea sab file system m h cz version control m kudh se nehi ho pata uske liye kuch samajna pedega.. lets start
 file system m ek folder ko directory bolta h but vcs m ek folder tho repository bola jata h 

 So aap ko jis directory or folder ko vcs m dalna h pehle us directry or folder k andar jao using cd /DirName 
 fir aapko git initialized karna perega using git init [git init matlab initialized an empty git repo]
 iske baad aap dekhenge terminal p Initislized empty git repo in <aapka folder k path k baad .git naam se ek aur folder rehega iska matlab wo ek git repo ban jata h >
aagar aap ls -a kerenge tho aapko wo dikhe ga

so avi m vcs m ek khali repo banadi h using git init. avi mere filesystem k folder m jo sab files and all h usko aagar vcs m leke jana h tho mujko kuch stages ko par karna perega.
stage 1 -  untrack (yea generally laal hota h )
stage 2 -  stage (green rehti h)
stage 3 - tracked hota h 


agar aapko aapni git vcs ka statuys dekhna h to uska command h git status
so the first step is git add <filename> untracked se stagede m jane k liye . agar aapko staged se untracked m bapas aana h then uska command h git rm --cached <filename>
iske baas aap ko to commit karna perega for the Tracked but aap tho aise commit nehi de payenge uskeliye aapko ek commit m,esage v dena h so stage se Tracked m jane k liye humko karna perega
git commit -"yout message for commiting the file" 


## Branch in Git whats master branch what the another branch we use WHY WE USE whats the purpose of using that 
branch is basically seperate line of development.
whats is branch it seems like a tree uska uuch branches h kuch leaf h so gi is also like same the tree branching concepts.
jo pehla branch rehta h wo hota h initial branch and wo agar aap local p batate ho by deafult it becam the master branch. ab yea jo master h wo future m aur aapne jaisa branched banayega . branch basically copy jaisa hota h from a master. example agar aapke master branch gayeb ho gaya tho na tho aap na tho code payenge  to hum log industry m branches use karte h 
git checkout -b <branch name>
isme kya hiota h suppose maine command likha git checkout -b dev to maine ek branch banaya and uska naam hua dev aur main us dev branch m hi chala gaya. agar maine  is time pe ls karta hu meko dikhega jo sab file mere master branch m tha wohi sab idhar matlab mere dev branch m v aa gaya . so the most important thing is ki main jis situation koi perticular branch se ek aur branch banayunga us naye branch main wo sab file automatically aa jayega jis branch se maine wo branch banaya.
agar aap git branch command daalte ho to aapko pata chelega kitne branch sab h aur correntlu aap kon se branch m ho.
isse faida kya hota h ? - jab agar koi company m code likhte ho aur wo production m chal rehi h but aap ke ceo ne bola application m kuch changes karna h fir aap change karke usi branch m code likh k usko production m chala sakte ho but but agar wo code fat gaya then u have to suffer for that . So what we do we just created another branch named dev then uspe aap code banake uko production m chalake dekh sakte ho agar koi issue h tho ukso aap fix karke fir master branch m usko add karsakte ho so thats the main reason for using branches.


## Merge 
aap ko jis branch k ander kisi aur branches ki files ko add karwana h to fir pehle aap us branch p aa jao then run a comman
git merge dev (here in dev I have made some changes and i want to merge it to master, so what will happen the the latest commit happens in dev will come to my master branch )



## Local to remote & remote o local (Git Repo)

first make an accout to an any platform it cloudbe gitHub or GitLab,bitbucket any thing.
after creating to an account lets jump to the new stuffds.
so i will chose github , there using GUI its very easy to create an repo. that repo is known as remote git Repo.
what repo we are doing since is know as local git repo.
as a Devops Engineer we need to creat a bridge from local to remote and remote to loacl then things will be much easier.


Local Repo to Remote repo
there are two ways to assess
1.PAT
2.SSH

first we will see the PAT - Its abn one time token. 
steps global settings>developer seetings > pat > token classic > generate new tocken > classic > then give a token name > repo access dedo > generate token > then copy the token and paste it any notepad 

then we need to run git remote -v isse pata chal jata h ki mera local git repo koi remote se connect hai ya nehi

then what repo we have created there we will take the https link 

then git remote add origin <the url of the https link>  origin kya na origin ek variable h jo mere url ko hold karta h yea ek industry standared hai. 

then if we wanted to run "git push origin master" it will ask me the github id then it will ask me my github passwod which is not right because github ki doc m likkha hua h ki github koiv platform se passwod nehi lega(just check it if i am wrong)
so avi kya karna perega hum logoko us pat ka access isko dedena perega.
git remote set-url origin https://<PAT>@github.com/my githubname/repo ka naam jisko hum ne connect kartna tha from local or jo repo humne github p banaya tha.
iske baad if we run git push origin master
we will see we are able to connect and able to push the file from local to remote.
ab yea local se remote ka safar ho gaya now we will do the reverse first create any file inside the remote github repo which is connected to our local.
fir hum logoko run karna pedega "git pull origin master"


through ssh
the main funda in ssh that that private and public key if we have a keypair then we do not need to create but if we do not have a key pair then we need to create using ssh-keygen
then the private key will be kept in local and the public key will kept in github. Now how to set the public key in github for that first go to global setting then > ssh and gpg key > new ssh key > then paste the public key and add thats all.
and then use git clone <the ssh link for that perticular folder> and thats it.

git diff se hum dekh sakte h ki pehle hum kya kiye the avi kar ho raha hai. like agar main koi repo ko clone karke aapne local m kuch change karta hu tho very ovious it will show in my remote tab we can check through "git diff"