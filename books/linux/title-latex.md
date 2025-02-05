---
header-includes:
  - \usepackage[nodayofweek]{datetime}
  - \usepackage[margin=2cm,includehead=true,includefoot=true,centering]{geometry}
  - \usepackage[english]{babel}
  - \usepackage[utf8]{inputenc}
  - \usepackage[scaled]{helvet}
  - \usepackage[T1]{fontenc}
  - \renewcommand\familydefault{\sfdefault}
  - \usepackage{fancyhdr}
  - \pagestyle{fancy}
  - \rfoot{Page \thepage}
  - \cfoot{}
  - \lhead{}  
  - \usepackage{xcolor}
  - \usepackage{mdframed}
  - \definecolor{light-gray}{gray}{0.95}
  - \usepackage{listings}
  - \lstset{language=bash,numbers=left,numbersep=1em,numberstyle=\tiny,xleftmargin=.25in,xrightmargin=.25in,basicstyle=\ttfamily\footnotesize,breaklines=true,commentstyle=\color[rgb]{0.13,0.54,0.13},backgroundcolor=\color{gray!10}}
  - \lstset{backgroundcolor=\color{gray}}
  - \usepackage{fontawesome}
  - \let\origurl\url
  - \renewcommand{\url}[1]{\href{#1}{\color{blue}\origurl{#1}}}
  - \let\orighref\href
  - \renewcommand{\href}[2]{\orighref{#1}{\color{blue}#2~\faExternalLink}}
  - \usepackage{graphicx}
  - \graphicspath{ {./images/} }
...