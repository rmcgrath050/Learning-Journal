
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
- 
