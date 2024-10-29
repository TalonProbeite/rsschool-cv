Artsiom Panamartsau
===================

Beginner Developer
---
### Contact information:
Phone: +375 29 555-73-42\
E-mail: siionunstoppable@gmail.com\
Telegram: @art0371
___
### A little about myself
My name is Artsiom Panamartsau, and I am a university student majoring in a field closely related to programming. During my studies, I was introduced to the C language, which was my first serious step into the world of programming. Despite its complexity, it was C that sparked my interest in this field and inspired me to continue learning.

At first, I immersed myself in Python, as it seemed like a powerful and flexible language, especially for automation and working with data. However, over time, I discovered an interest in creating web applications. This led me to study front-end technologies: HTML, CSS, and JavaScript, to understand how to create user-friendly interfaces.

I am currently actively developing in the front-end, as it opens up a lot of opportunities for designing reliable server parts. I like the idea of ​​creating projects that can be useful to others, and I believe that in the future, my experience and knowledge will help me implement interesting and useful projects in a team of professionals.
___
### Skills and Proficiency:
  * CSS3, HTML5
  * JavaScript Basics
  * Python3
  * VS Code, Qt Creator
____
### Code example:
**Find the most adjacent integers of the same value in a grid  from CODEWARS:** Find the size s of the largest group of adjacent integers that all have the same value v. Return these 2 results as a tuple (v, s).

If there are several largest groups corresponding to the same size s, return the tuple with the lowest possible value of v.

Integers in the grid are considered part of an adjacent group if they can be reached by moving through other integers of the same value horizontally or vertically, but not diagonally.
```
   function findMostAdjacent(grid) {
   const n = grid.length;
    const directions = [[1, 0], [-1, 0], [0, 1], [0, -1]]; 
    let maxGroupSize = 0;
    let minValue = Infinity;

    function dfs(x, y, value) {
        const stack = [[x, y]];
        let size = 0;

        while (stack.length) {
            const [i, j] = stack.pop();

            if (i < 0 || i >= n || j < 0 || j >= n || grid[i][j] !== value) continue;

            size++;
            grid[i][j] = null; 

            for (const [di, dj] of directions) {
                const ni = i + di;
                const nj = j + dj;
                stack.push([ni, nj]);
            }
        }

        return size;
    }

    for (let i = 0; i < n; i++) {
        for (let j = 0; j < n; j++) {
            if (grid[i][j] !== null) {
                const value = grid[i][j];
                const size = dfs(i, j, value);

               
                if (size > maxGroupSize || (size === maxGroupSize && value < minValue)) {
                    maxGroupSize = size;
                    minValue = value;
                }
            }
        }
    }

    return [minValue, maxGroupSize];}
 ```
___
### Languages:
  * Russian - Native
  * Belorussian - Intermediate
  * English -Basic
