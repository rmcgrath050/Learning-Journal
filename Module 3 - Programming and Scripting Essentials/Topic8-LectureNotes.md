
### Devops


<img width="796" height="576" alt="image" src="https://github.com/user-attachments/assets/45723c54-6447-4ec4-b0c6-50c26fdcc8b4" />

If there was no Devops development, teams silos. 

### Three Stages
- coding 
- building
- releasing 

### Continuous Integration

<img width="778" height="616" alt="image" src="https://github.com/user-attachments/assets/520f956e-ea1a-4d1e-9d5b-09406a461574" />

- once your code is on local computer ,
- put into a pacakge for github , shared local reposibisty with Bank?
- Compile the code, linting the code (structing code so it follows certain standards)
- Can be a painful process sometimes , as it can take a while to compile code and spit out error
- Testing takes the longest part of this,
- integration hell 'long live branches' -  if developers dont merge often , merging a long lived branch into the main branch takes a long time and creates
  sigificent conflicts
  

  ### To help: 
- Moduralrisation : break down applications into smaller independant components
- running unit tests on their local machine before commiting to main repositary
- if local device passes and mainline fails - could be misaligned dependancies, missing libaries or different verisons local vrs live
- Commit at least daily - small commits
- Automate the build  - once stats have been colleted automatic this for less manual intervention
- Every bug has a test - feedback for furture and intoduces learning / error handling
- Transparent builds , shoundnt be a guess game


### Disavantages of continuos integration
- Creating tests is time consuming (although should save time in long run)
- build system needs maintained (like the staging to commit on repo)


## Continous Delivery 
- After your packages has went though integration , it has to be possibly ready to go any any time (releasable)
- Think of integration as airport secuirty (problems caught early) , delivery on the other hand has all the nesscary checks complete
  and can deploy. The flight hasnt started until we are completely ready.
- still testing involved here, but in shorter cycles, shorter sprints , smaller quicker changes
- These quick releases are easy to manage and take feedback from?
- Improved customer saisfaction, improved quality, imporved productivity and reduced release risk 
- CD usually is continuous delivery 

Netflix uses the CI/CD approach
- uses canary deployment
- 
<br>
<br>


## Continuous deployment 
- team lead approves final push to production
- if code passes all tests goes live automatically
- ready to lanch and launch - no ticket to raise
- Lot of quality assurance is need, pipleine must be robust for this
- Give true responsivess - released in real time
- Blast radius , less dramtic downtime
- Banks/finance dont use this due to secuirty
- https://www.henricodolfing.ch/case-study-4-the-440-million-software-error-at-knight-capital/ example 


## Sumarry of ci/cd 
The three different steps are split into coding building and releasing through  continuous Integration, continuous delivery and continuous deployment. 

In a CI/CD pipeline it uses continuous delivery, automation pauses when developers push to production. On the other hand, continuous deployment automates the entire release process
Benefits include : 
- Ongoing feedback to stakeholders, with smaller changes
* Automated, continuous testing means systems remain stable 
* CI begins with shared repos , so easier to keep track over different versions and easier to collaborate 
* Easier transparency , though logs and build in tooling easier to troubleshoot
* Ensuring scalability
* More consistency


## Containers 


<img width="737" height="573" alt="image" src="https://github.com/user-attachments/assets/4cf44f5b-ebd2-408c-942f-efb4135d754e" />

benefits:
- OS agnostic - doesnt care what operating system you use, 
- portable across systems, as long as host can run dockor
- simualr to virtual machines but better! - they dont carry an entire operating system 
- easier to scale , easier to maitain compared to virtual machines

<img width="762" height="651" alt="image" src="https://github.com/user-attachments/assets/31bd9ded-c9f3-4bba-a4bb-907c8843a021" />

## Infrasturture as code 



  
