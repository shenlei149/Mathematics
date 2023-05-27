# 三角函数与反三角函数

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

# 双曲函数

## 定义
参考 [7.3 小节](/010-Calculus/070-Integrals-and-Transcendental-Functions/030-Hyperbolic-Functions.md)
$$\sinh x=\frac{e^x-e^{-x}}{2}$$
$$\cosh x=\frac{e^x+e^{-x}}{2}$$
$$\tanh x=\frac{\sinh x}{\cosh x}=\frac{e^x-e^{-x}}{e^x+e^{-x}}$$
$$\coth x=\frac{\cosh x}{\sinh x}=\frac{e^x+e^{-x}}{e^x-e^{-x}}$$
$$\operatorname{sech} x=\frac{1}{\cosh x}=\frac{2}{e^x+e^{-x}}$$
$$\operatorname{csch} x=\frac{1}{\sinh x}=\frac{2}{e^x-e^{-x}}$$

## 恒等式
参考 [7.3 小节](/010-Calculus/070-Integrals-and-Transcendental-Functions/030-Hyperbolic-Functions.md)
$$\cosh^2 x-\sinh^2 x=1$$
$$\sinh 2x=2\sinh x\cosh x$$
$$\cosh 2x=\cosh^2 x+\sinh^2 x$$
$$\cosh^2 x=\frac{\cosh 2x+1}{2}$$
$$\sinh^2 x=\frac{\cosh 2x-1}{2}$$
$$\tanh^2 x=1-\operatorname{sech}^2 x$$
$$\coth^2 x=1+\operatorname{csch}^2 x$$

## 微分
参考 [7.3 小节](/010-Calculus/070-Integrals-and-Transcendental-Functions/030-Hyperbolic-Functions.md)
$$\frac{d}{dx}\sinh u=\cosh u\frac{du}{dx}$$
$$\frac{d}{dx}\cosh u=\sinh y\frac{du}{dx}$$
$$\frac{d}{dx}\tanh u=\operatorname{sech}^2 u\frac{du}{dx}$$
$$\frac{d}{dx}\coth u=-\operatorname{csch}^2 u\frac{du}{dx}$$
$$\frac{d}{dx}\operatorname{sech} u=-\operatorname{sech} u\tanh u\frac{du}{dx}$$
$$\frac{d}{dx}\operatorname{csch} u=-\operatorname{csch} u\coth u\frac{du}{dx}$$

## 积分
参考 [7.3 小节](/010-Calculus/070-Integrals-and-Transcendental-Functions/030-Hyperbolic-Functions.md)
$$\int\sinh udu=\cosh u+C$$
$$\int\cosh udu=\sinh u+C$$
$$\int\operatorname{sech}^2 udu=\tanh u+C$$
$$\int\operatorname{csch}^2 udu=-\coth u+C$$
$$\int\operatorname{sech} u\tanh udu=-\operatorname{sech} u+C$$
$$\int\operatorname{csch} u\coth udu=-\operatorname{csch} u+C$$
