# 辗转相除法的证明以及最小公倍数求法的理解
一.定理：两个整数的最大公约数等于其中较小的那个数和两数的相除余数的最大公约数。
  最大公约数（greatest common divisor）缩写为gcd。

二.从集合角度理解（直观体验）

例子：求gcd(20,16)
20 和 16 的公约数的集合为{1，2，4}.
16 和 4 (20 % 16)的公约数的集合为{1，2，4}
4 和 0 (16 % 4)的公约数的集合为{1，2，4}
可以见得，它们的公约数集合都相等，所以最大公约数相等。

三.证明
整数a,b,n,m,x,y,r.
欲求gcd(a,b).
设 a = nb + r.

(1)证明a,b的公约数也是r的公约数\n
设m是a,b的任意公约数。
其中a = xm ; b = ym;
则r = a - nb = xm - nym.
可得 m|r  ,   证毕.

但是这样并不能证明a,b的最大公约数也是b,r的最大公约数，所以需要证明第二步。

(2)证明b,r的公约数也是a的公约数
设m'是b,r的任意公约数。
其中b = x'm' ; r = y'm';
则a = nb + r = nx'm' + y'm'.
可得 m'|a  ,   证毕.

综合上述，a,b与b,r公约数的集合相等，最大公约数也相等。


为什么两个数的最小公倍数等于两数相乘除以两数最大公约数？
a,b,a',b'均为整数。
假设求lcm(a,b);
如果最小公倍数等于a*b'(c<=b)，那么需要满足从a里面拿出一个数与b'相乘等于b，为了使整体更小，就意味着从a中拿出的数越大越好，
所以拿出他们的最大公约数是最好的。
所以有a=gcd(a,b)*a';
     c * gcd(a,b) = b';
最小公倍数等于 a'b'*gcd(a,b);
也就是a*b/gcd(a,b);
