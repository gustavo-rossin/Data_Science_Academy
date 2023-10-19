Finalização do setup do ```Jupyter Notebook``` em darkmode com o [jupyterthemes](https://github.com/dunovank/jupyter-themes).

Escolhi as seguintes configs:

tema onedork, com fontsize 11, text fontsize 14, notebook (titulo do notebook) fontsize 16, output fontsize 10.
Além disso, com a toolbar, kernel e nome visíveis (-T -kl -N).
~~~python
jt -t onedork -fs 11  -tfs 14 -nfs 16 -ofs 10 -cellw 88% -T -kl -N
~~~

Aprendi também a deixar os plots com o estilo darkmode, usando a própria lib jupyterthemes, importando o jtplot.

Exemplo:
~~~python
import seaborn as sns
from jupyterthemes import jtplot

jtplot.style(theme='onedork')

x = [0, 1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10, 12]

sns.lineplot(x=x, y=y).set(title='Exemplo de como fica o gráfico com jtplot')
~~~
