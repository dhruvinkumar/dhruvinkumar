# 💻 Tech Stack:
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white)  ![Bootstrap](https://img.shields.io/badge/bootstrap-%23563D7C.svg?style=for-the-badge&logo=bootstrap&logoColor=white) ![jQuery](https://img.shields.io/badge/jquery-%230769AD.svg?style=for-the-badge&logo=jquery&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white) 	![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white) ![Canva](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=for-the-badge&logo=Canva&logoColor=white)
<h3 align="left">Coding Platforms:</h3>
<p align="left">
<a href="https://www.hackerrank.com/bj1542" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/hackerrank.svg" alt="bj1542" height="30" width="40" /></a>
<a href="https://www.leetcode.com/dhruvinkumar_bhatt11" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/leet-code.svg" alt="dhruvinkumar_bhatt11" height="30" width="40" /></a>
<a href="https://auth.geeksforgeeks.org/user/dhruvinbhatt11" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/geeks-for-geeks.svg" alt="dhruvinbhatt11" height="30" width="40" /></a>
</p>

# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=dhruvinkumar&theme=dark&hide_border=false&include_all_commits=false&count_private=false)<br/>
![](https://github-readme-streak-stats.herokuapp.com/?user=dhruvinkumar&theme=dark&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=dhruvinkumar&theme=dark&hide_border=false&include_all_commits=false&count_private=false&layout=compact)

### ✍️ Random Dev Quote
![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical)

---
![](https://visitcount.itsvg.in/api?id=dhruvinkumar&icon=0&color=0)
![](https://github-readme-activity-graph.cyclic.app/graph?username=dhruvinkumar&theme=nightowl)
<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
![C](https://img.shields.io/badge/Python3-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
```
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
struct job
{
    int deadLine;
    int profit;
};
int compare(const void *x,const void *y)
{
    return (((struct job*)y)->profit) - (((struct job*)x)->profit);
}
int main() 
{
    int testCases;
    scanf("%d",&testCases);//Reading the value of testcases
    
    while(testCases--)
    {
        int n;
        scanf("%d",&n);//Reading total number of job records
        
        struct job jobDetails[n];
        int i, maximumDeadline = 0;
        //Reading job deadline
        for(i=0;i<n;i++)
        {
            scanf("%d",&jobDetails[i].deadLine);
            if(maximumDeadline < jobDetails[i].deadLine)
                maximumDeadline = jobDetails[i].deadLine;
        }
        //Reading profit values
        for(i=0;i<n;i++)
            scanf("%d",&jobDetails[i].profit);
        
        qsort(jobDetails,n,sizeof(struct job),compare);
        
        int task[1001] = {0}, j, maxProfit = 0;
        for(i=0;i<n;i++)
        {
            if(task[jobDetails[i].deadLine] == 0)
            {
                task[jobDetails[i].deadLine] = jobDetails[i].profit;
                maxProfit += jobDetails[i].profit;
            }
                
            else
            {
                int temp = jobDetails[i].profit;
                for(j=jobDetails[i].deadLine;j>0;j--)
                {
                    if(task[j]<temp)
                    {
                        task[j] = temp;
                        maxProfit += temp;
                        break;
                    }
                }
            }
        }
        printf("%d\n",maxProfit);        
    }
    
    return 0;
}
```
