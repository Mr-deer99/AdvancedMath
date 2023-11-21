### 公式标记与查看公式 

使用MathJax时，需要用一些适当的标记告诉MathJax某段文本是公式代码。此外，MathJax中的公式排版有两种方式，inline和displayed。inline表示公式嵌入到文本段中，displayed表示公式独自成为一个段落。例如，$f(x)=3×x$这是一个inline公式，而下面$$f(x)=3×xf(x)=3×x$$


则是一个displayed公式。

在MathJax中，默认的displayed公式分隔符有 `$$...$$` 和`\[...\]`，而默认的inline公式分隔符为`\(...)\`，当然这些都是可以自定义的，具体配置请参考[文档](http://docs.mathjax.org/en/latest/start.html#tex-and-latex-input)。下文中，使用`$$...$$`作为displayed分隔符，`$...$`作为inline分隔符。

此外，可以在渲染完成的公式上方右键点击，唤出右键菜单。在菜单中提供了查看公式代码、设置显示效果和渲染模式的选项。

### 希腊字母

请参见下表：

**名称**               **大写**               **Tex**               **小写**               **Tex**

alpha             AA                   A                  αα              ` \alpha`

beta              BB                   B                   ββ               `\beta`

gamma          ΓΓ                  `\Gamma `        γγ               ` \gamma`

delta             ΔΔ                  `\Delta`             δδ                `\delta`

epsilon          EE                    E                  ϵϵ                 `\epsilon`

zeta              ZZ                    Z                  ζζ                \`zeta`

eta               HH                    H                  ηη               `\eta`

theta            ΘΘ                  ` \Theta`             θθ               `\theta`

iota              II                      I                   ιι                 `\iota`

kappa           KK                    K                  κκ                 `\kappa`

lambda         ΛΛ                   `\Lambda`          λλ                ` \lambda`

mu               MM                    M                  μμ                 `\mu`

nu                NN                    N                   νν                 `\nu`

xi                 ΞΞ                   `\Xi`                  ξξ                  `\xi`

omicron        OO                     O                  οο                  `\omicron`

pi                 ΠΠ                    `\Pi`                 ππ                 ` \pi`

rho               PP                     P                  ρρ                   \`rho`

sigma           ΣΣ                   `\Sigma`            σσ                  `\sigma`

tau               TT                     T                   ττ                  \`tau`

upsilon         ΥΥ                  ` \Upsilon`           υυ                  \`upsilon`

phi               ΦΦ                   `\Phi`                 ϕϕ                 ` \phi`

chi               XX                     X                   χχ                  `\chi`

psi               ΨΨ                    `\Psi`                ψψ                   `\psi`

omega          ΩΩ                  `\Omega`            ωω                  ` \omega `

### 上标与下标

上标和下标分别使用^与_，例如x_i^2: x2ixi2。默认情况下，上下标符号仅对下一个组起作用。一个组即单个字符或者使用{...}包裹起来的内容。也就是说，如果使用10^10，会得到10101010，而10^{10}才是10101010。同时，大括号还能消除二义性，如`x^5^6`将得到一个错误，必须使用大括号来界定^的结合性，如`{x^5}^6`: ${x^5}^6$或者`x^{5^6}`: $x^{5^6}$

### 括号

1. 小括号与方括号：使用原始的`()`，`[]`即可，如`(2+3)[4+4]`: `(2+3)[4+4](2+3)[4+4]`

2. 大括号：由于大括号{}被用来分组，因此需要使用\{和\}表示大括号，也可以使用`\lbrace`和`\rbrace`来表示。如`\{a*b\}`: {a∗b}{a∗b}，`\lbrace a*b \rbrace `: {a∗b}{a∗b}

3. 尖括号：使用`\langle`和`\rangle`表示左尖括号和右尖括号。如`\langle x \rangle` : ⟨x⟩⟨x⟩

4. 上取整：使`\lceil`和`\rceil`表示。如`\lceil x \rceil`：⌈x⌉⌈x⌉

5. 下取整：使用`\lfloor`和`\rfloor`表示。如`\lfloor x \rfloor`：⌊x⌋⌊x⌋

6. 不可见括号：使用.表示

需要注意的是，原始符号并不会随着公式大小缩放，可以使用`\left(...\right)`来自适应地调整括号大小。

### 求和与积分

`\sum`用来表示求和符号，其下标表示求和下限，上标表示上限。如`\sum_1^n`: $\sum_1^n$。

`\int`用来表示积分符号，同样地，其上下标表示积分的上下限。如`\int_1^\infty`: $\int_1^\infty$。

与此类似的符号还有：`\prod`:$\prod$ , `\bigcup`: $\bigcup$ , `\bigcap`:$\bigcap$ ,`\iint`:$\iint$。

### 分式和根式

分式的表示：

-   第一种，使用`\frac ab` , `\frac`作用于其后的两个组a , b ，结果为$\frac ab$。如果你的分子或分母不是单个字符，请使用{...}来分组。
-   第二种，使用`\over`来分隔一个组的前后两部分，如 `{a+1 \over b+1}`: ${a+1 \over b+1}$

根式使用`\sqrt`表示，如：`\sqrt[4]{\frac xy}\sqrt[4]{\frac xy}`:$\sqrt[4]{\frac xy}$

### 字体

1. 使用`\mathbb`或`\Bbb`显示黑板粗体字，此字体经常用来表示实数、整数、有理数、复数。如 $\mathbb {CHNQRZCHNQRZ}$

2. 使用`\mathbf`显示黑体字，如 $\mathbf {ABCDEFGHIJKLMNOPQRSTUVWXYZABCDEFGHIJKLMNOPQRSTUVWXYZ}$，

abcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyz

3. 使用`\mathtt`显示打印机字体，如 ABCDEFGHIJKLMNOPQRSTUVWXYZABCDEFGHIJKLMNOPQRSTUVWXYZ，

abcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyz

4. 使用`\mathrm`显示罗马字体，如 ABCDEFGHIJKLMNOPQRSTUVWXYZABCDEFGHIJKLMNOPQRSTUVWXYZ，

abcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyz

5. 使用`\mathscr`显示手写体，如，

ABCDEFGHIJKLMNOPQRSTUVWXYZABCDEFGHIJKLMNOPQRSTUVWXYZ

6. 使用`\mathfrak`显示Fraktur字母（一种德国字体），如

ABCDEFGHIJKLMNOPQRSTUVWXYZABCDEFGHIJKLMNOPQRSTUVWXYZ

，

abcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyz

### 特殊函数和符号

1.  常见的三角函数，如 $sinx$:`$sin⁡x$` , `$arctanx$`:$arctanx$ , $$\lim_{x \rightarrow \infty}\frac{\sin x}{x} = 1$$
 

2. 比较运算符：`\lt \gt \le \ge \neq` : << >> ≤≤ ≥≥ ≠≠。可以在这些运算符前面加上`\not`，如`\not\lt `: ≮≮

3. `\times \div \pm \mp `表示：×× ÷÷ ±± ∓∓，`\cdot`表示居中的点，`x \cdot y` ：x⋅yx⋅y

4. 集合关系与运算：`\cup \cap \setminus \subset \subseteq \subsetneq \supset \in \notin \emptyset \varnothing` : ∪∪ ∩∩ ∖∖ ⊂⊂ ⊆⊆ ⊊⊊ ⊃⊃ ∈∈ ∉∉ ∅∅ ∅∅

5. 表示排列使用`\binom{n+1}{2k}`或`{n+1 \choose 2k}`

6. 箭头：`\to` `\rightarrow` `\leftarrow` `\Rightarrow` `\Leftarrow` `\mapsto`: → → ← ⇒ ⇐ ↦

7. 逻辑运算符：`\land` `\lor` `\lnot` `\forall` `\exists` `\top` `\bot`` \vdash` `\vDash`：∧∧ ∨∨ ¬¬ ∀∀ ∃∃ ⊤⊤ ⊥⊥ ⊢⊢ ⊨⊨

8. `\star` `\ast` `\oplus` `\circ` `\bullet` : ⋆⋆ ∗∗ ⊕⊕ ∘∘ ∙∙

9. `\approx` `\sim` `\cong` `\equiv` `\prec` : ≈≈ ∼∼ ≅≅ ≡≡ ≺≺

10.`\infty` `\aleph_o` `\nabla` `\partial` `\Im` `\Re` : ∞ ℵoℵo ∇∇ ∂∂ Iℑ Rℜ

11. 模运算 `\pmode` , 如`a \equiv b \pmod n` : $a \equiv b \pmod n$

12. `\ldots`与`\cdots`，其区别是dots的位置不同，ldots位置稍低，cdots位置居中。



13. 一些希腊字母具有变体形式，如`\epsilon` `\varepsilon` : ϵϵ εε , `\phi` `\varphi `: ϕϕ φφ

使用[Detexify](http://detexify.kirelabs.org/classify.html)，你可以在网页上画出符号，Detexify会给出相似的符号及其代码。这是一个方便的功能，但是不能保证它给出的符号可以在MathJax中使用，你可以参考[supported-latex-commands](http://docs.mathjax.org/en/latest/tex.html#supported-latex-commands)确定MathJax是否支持此符号。

### 空间

通常MathJax通过内部策略自己管理公式内部的空间，因此a...b与a......b( . 表示空格)都会显示为abab。可以通过在ab间加入`\,`增加些许间隙，`\;`增加较宽间隙，`\quad`与`\qquad`会增加更大的间隙，如 $ab\,ab$

### 顶部符号

对于单字符，`\hat` :  x^x^ ;

对于多字符，`\widehat` : xyˆxy^

类似的还有 `\overline` ,` \vec` ,` \overrightarrow` , `\dot` , `\ddot` : xyz¯¯¯¯¯¯¯¯xyz¯ a⃗ a→ x→x→ x˙x˙ x¨x¨

角度$60^\circ$  :  `60^\circ`
角$\angle$      `\angle`

# 分段函数
使用`\begin{cases}表达式1\\表达式2\end{cases}`来表示，当中使用`\\`来换行，例如
```LaTex
$$f(x)=\begin{cases}2x+1\qquad 0<x<3\\3x+4\qquad x\ge3\end{cases}$$
```
$$f(x)=\begin{cases}2x+1\qquad 0<x<3\\3x+4\qquad x\ge3\end{cases}$$
# 设置对齐
使用`\begin{aligned}表达式1 & 条件\\表达式2 & 条件\end{aligned}`来进入对齐模式
当中`&`表示对齐标志，使用`\\`换行后，在下一行需要对齐的地方加上`&`会让其对齐上面一行同样的部份
比如
```LaTex
$$\begin{aligned}x=a\qquad&x\not=0\\x^2+2x+b+C&x=0\end{aligned}$$
```
$$\begin{aligned}x=a&\qquad x\not=0\\x^2+2x+b+C=0&\qquad x=0\end{aligned}$$
# 矩阵
参考[知乎-半个冯博士-如何用LaTex编写矩阵](https://zhuanlan.zhihu.com/p/266267223)
以下代码表示剪切矩阵
```LaTex
$$\begin{matrix}1&0\\0&1\end{matrix}$$
```
$$\begin{matrix}1&0\\0&1\end{matrix}$$
用`\begin{matrix}  \end{matrix}`表示进入矩阵模式
`&`表示元素间间隔
`\\`表示换行

## array模式
也可以使用array模式来表示矩阵，他提供了更多的自定义选项
- 使用`\begin{arrary}\end{array}`进入array模式，
- 后面加上一个中括号，可以在里面写上每一列的对齐方式，如`\begin{array}\end{array}{clr}`，表示矩阵有三列，第一列左对齐，第二列居中对齐，第三列右对齐
- 使用`\left[`和`\right]`让括号自适应大小
```Latex
$$\left[
\begin{array}{cc}
1&0\\0&1
\end{array}\right]$$
```
$$\left[
\begin{array}{cc}
1&0\\0&1
\end{array}\right]$$

## 方括号矩阵
使用`{bmatrix}`表示方括号矩阵
```LaTex
$$\begin{bmatrix}1&0\\0&1\end{bmatrix}$$
```
$$\begin{bmatrix}1&0\\0&1\end{bmatrix}$$

## 圆括号矩阵
使用`{pmatrix}`表示方括号矩阵
```LaTex
$$\begin{pmatrix}1&0\\0&1\end{pmatrix}$$
```
$$\begin{pmatrix}1&0\\0&1\end{pmatrix}$$

## 行列式
使用`{vmatrix}`表示方括号矩阵
```LaTex
$$\begin{vmatrix}1&0\\0&1\end{vmatrix}$$
```
$$\begin{vmatrix}1&0\\0&1\end{vmatrix}$$

## 矩阵的省略
使用`\ddots`表示斜着的三点，`\cdots`表示横着的三点，`\vdots`表示数着的三点
```LaTex
$$\begin{bmatrix}1&\cdots&0\\0&1\end{bmatrix}$$
```
$$\begin{bmatrix}1&\cdots&0\\\vdots&\ddots&\vdots\\0&\cdots&1\end{bmatrix}$$
## 矩阵里划线
要在矩阵里划线，要使用[[LaTeX语法#array模式|array模式]]
### 竖线
在对齐方式中加上竖线`{cc|c}`表示在该列中添加竖线
```
$$\left[
\begin{array}{cc|c}
1&0&1\\
0&1&1
\end{array}
\right]$$
```
$$\left[
\begin{array}{cc|c}
1&0&1\\
0&1&1
\end{array}
\right]$$
冒号`{cc:c}`表示竖虚线
```Latex
$$\left[
\begin{array}{cc:c}
1&0&1\\
0&1&1
\end{array}
\right]$$
```
$$\left[
\begin{array}{cc:c}
1&0&1\\
0&1&1
\end{array}
\right]$$
### 横线
在行尾加上`\hline`可以添加横线
```latex
$$\left[
\begin{array}{ccc}
1&0&1\\ \hline
0&1&1
\end{array}
\right]$$
```
$$\left[
\begin{array}{ccc}
1&0&1\\ \hline
0&1&1
\end{array}
\right]$$
`\hdashline`表示横虚线
```latex
$$\left[
\begin{array}{ccc}
1&0&1\\ \hdashline
0&1&1
\end{array}
\right]$$
```
$$\left[
\begin{array}{ccc}
1&0&1\\ \hdashline
0&1&1
\end{array}
\right]$$
