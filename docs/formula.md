# 微积分

## 三角函数导数
参考 [3.5 小节](/010-Calculus/030-Derivatives/050-Derivatives-of-Trigonometric-Functions.md)
$$\frac{d}{dx}\sin x=\cos x$$
$$\frac{d}{dx}\cos x=-\sin x$$
$$\frac{d}{dx}\tan x=\sec^2 x$$
$$\frac{d}{dx}\cot x=-\csc^2 x$$
$$\frac{d}{dx}\sec x=\sec x\tan x$$
$$\frac{d}{dx}\csc x=-\csc x\cot x$$

## 反三角函数导数
参考 [3.9 小节](/010-Calculus/030-Derivatives/090-Inverse-Trigonometric-Functions.md)
$$\frac{d}{dx}\sin^{-1}x=\frac{1}{\sqrt{1-x^2}},|x|<1$$
$$\frac{d}{dx}\cos^{-1}x=-\frac{1}{\sqrt{1-x^2}},|x|<1$$
$$\frac{d}{dx}\tan^{-1}x=\frac{1}{1+x^2}$$
$$\frac{d}{dx}\cot^{-1}x=-\frac{1}{1+x^2}$$
$$\frac{d}{dx}\sec^{-1}x=\frac{1}{|x|\sqrt{x^2-1}},|x|>1$$
$$\frac{d}{dx}\csc^{-1}x=-\frac{1}{|x|\sqrt{x^2-1}},|x|>1$$

## 三角函数积分
参考 [5.5 小节](/010-Calculus/050-Integrals/050-Indefinite-Integrals-and-the-Substitution-Method.md)
$$\int\tan xdx=\ln|\sec x|+C$$
$$\int\cot xdx=\ln|\sin x|+C$$
$$\int\sec xdx=\ln|\sec x+\tan x|+C$$
$$\int\csc xdx=-\ln|\csc x+\cot x|+C$$
$$\int\sin^2x dx=\frac{x}{2}-\frac{\sin 2x}{4}+C$$
$$\int\cos^2x dx=\frac{x}{2}+\frac{\sin 2x}{4}+C$$
