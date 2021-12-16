// Sequência introdutória
1.1 

    git commit; 
    git commit; 

1.2 

    git branch bugFix; 
    git checkout bugFix; 

1.3 

    git checkout -b bugFix; 
    git commit; 
    git checkout main; 
    git commit; 
    git merge bugFix; 

1.4

    git checkout -b bugFix; 
    git commit; 
    git checkout main; 
    git commit; 
    git checkout bugFix; 
    git rebase main; 

    // Acelerando

2.1 

    git checkout c4; 

2.2 

    git checkout c4^; 

2.3 

    git branch -f main c6; 
    git branch -f bugFix C0; 
    git checkout c1; 

2.4 

    git reset local~1; 
    git checkout pushed; 
    git revert pushed; 

//Movendo trabalho por ai

3.1 

    git cherry-pick c3 c4 c7; 

3.2 

    git rebase -i main~4 --aboveAll; 
ordenar os commit c3, c5, c4. e omitir o que sobrou

// Sortidos
4.1 

    git checkout main; 
    git cherry-pick c4; 

4.2 

    git rebase -i caption~2 --aboveAll; 
    git commit --amend; 
    git rebase -i caption~2 --aboveAll; 
    git branch -f main caption; 
1) ordena os  commits as c3, c2. 
2) ordena os commits as c2'', c3'. 

4.3 

    git checkout main; 
    git cherry-pick c2; 
    git commit --amend; 
    git cherry-pick c3; 

4.4 

    git tag v0 c1; 
    git tag v1 c2; 
    git checkout c2; 

4.5 

git commit; 

// temas avançados

5.1 

    git rebase main bugFix; 
    git rebase bugFix side; 
    git rebase side another; 
    git rebase another main; 

5.2

git branch bugWork main~^2~; 

5.3 

    git checkout one;   
    git cherry-pick c4 c3 c2; 
    git checkout two; 
    git cherry-pick c5 c4 c3 c2; 
    git branch -f three c2;