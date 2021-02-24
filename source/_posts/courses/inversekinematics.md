Inverse Kinematics, IK, is to understand how a robot arm could move to a specific position. When I took the computer animation course, only a small amount of time were spent on discussing it. A lot of details are missed, and it could be a bit confusing for newbies.



CCD

CCD is based a simple idea. That is, we rotate one joints at a time and in each step, the tip of our arm would move closer to the target.





The Jacobian Matrix describes how the velocity in the Euler space can be mapped to the velocity in the joints space. To put it simpler, a Jacobian Matrix would reflect how the rotation of the joints would affect the velocity of the tip. So we just need to find the inverse of the Jacob Matrix, that way we can find the required joint rotation. There are 3 problems to solve, what's the velocity of the tip? How to find the Jacob. Matrix? How to find inverse of Jacob Matrix(You will soon see Jacob matrix is NOT a square matrix).



The velocity is simple, each time we find an apprioriate velocity that would bring the tip closer to the end. Normally the shortest path form tip to target would be a straight line. Therefore, we have make sure each step, we are not drifting to far from the straight line. The maximum accaptable deviation distance, we call it $\epsilon$. The algorithm would look be like binary search:

1. TODO



The next question is, how to find a Jacob matrix. That would broght us back to high school physics. ....





Finally, we need to solve the inverse of Jacob Matrix. Actually this is a Least Mean Square. Let me explain how these things correlated.

The least mean square problem is as follows:
$$
LMS = \underset{k, b}{\operatorname{argmin}}\sum_i (kx_i+b-y_i)^2
$$
The expression can also be viewed as the distance of two high dimensional points. That is:
$$
\vec{v_1}= 
$$
If we look carefully, we would see that the second point is described by 2 varible. These means that the second point is located in a plane on a high dimensional space. So, the problems is now finding a point on a plane that is closest to a certain point in space. That would be easy as we just need to find a projection of the point on the plane. That would be high school geometry.









## Reference

- [（数学）最小二乘的几何意义及投影矩](https://www.cnblogs.com/AndyJee/p/5053354.html)
- [矩阵的逆、伪逆、左右逆，最小二乘，投影矩阵](https://blog.csdn.net/baidu_38172402/article/details/82931879)

