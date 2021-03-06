# map-gen
Procedural map generation with AnsProlog and answer set programming.

## NOTE: SOME ASSETS WILL NOT LOAD PROPERLY WHEN VIEWED ON GitHub, PLEASE OPEN IT IN GOOGLE COLAB WITH CLINGO IMPORTED.
* https://colab.research.google.com/drive/1T9DikhvhDm2Hv9MH4wIyTceEgj3KiFWk?usp=sharing

## Summary
The program infers facts and state of the world given constraints. Thus it makes choices about how and where to place assets to eventually form a full map. 

* For example, a house will have rules where no two doors should be constructed and placed right next to one another. 
* This program is using Answer Set programming which is a declarative programming paradigm in contrast to the more widely used imperative programming paradigm. Whereas the latter is clearly coded and defined to tell the program what to do, in declarative programming the computer generates a desired result given a prescribed solution or constraints - similar to how SQL works..

## Example
* Constraints

![smallconstraints](https://i.imgur.com/1Emp3rg.png?raw=true)

* One Possible Output

![outputie](https://i.imgur.com/VKFVkmO.png?raw=true)
