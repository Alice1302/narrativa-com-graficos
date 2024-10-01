{
  "Instagram": 16.5,
  "WhatsApp": 16.1,
  "Facebook": 12.8,
  "WeChat": 12.8,
  "TikTok": 7.4,
  "DouYin": 6.6,
  "Twitter": 3.2,
  "Telegram": 2.4,
  "FB Messenger": 2.3,
  "LINE": 1.7
}
<script type="module" src="graficos/redesFavoritasMundo.js"></script>
console.log('deu certo');
async function redesFavoritasMundo() {
    const url = 'https://raw.githubusercontent.com/guilhermeonrails/api/main/redes-favoritas.json'
    const res = await fetch(url)
    const dados = await res.json()
    console.log(dados);
}

redesFavoritasMundo()
{Instagram: 16.5, WhatsApp: 16.1, Facebook: 12.8, WeChat: 12.8, TikTok: 7.4, _}
async function redesFavoritasMundo() {
    const url = 'https://raw.githubusercontent.com/guilhermeonrails/api/main/redes-favoritas.json'
    const res = await fetch(url)
    const dados = await res.json()
    const redes = Object.keys(dados)
    const valores = Object.values(dados)

    const data = [
        {
            values: valores,
            labels: redes,
            type: 'pie',
            textinfo: 'label+percent'
        }
    ]
}

redesFavoritasMundo()
const layout = {
    plot_bgcolor: getCSS('--bg-color'),
    paper_bgcolor: getCSS('--bg-color'),
    title: {
        text: 'Redes sociais com mais usuários no mundo',
        x: 0,
        font: {
            color: getCSS('--primary-color'),
            family: getCSS('--font'),
            size: 30
        }
    },
    xaxis: {
        tickfont: tickConfig,
        title: {
            text: 'nome das redes sociais',
            font: {
                color: getCSS('--secondary-color')
            }
        }
    },
    yaxis: {
        tickfont: tickConfig,
        title: {
            text: 'bilhões de usuários ativos',
            font: {
                color: getCSS('--secondary-color')
            }
        }
    }
}
// código omitido

const layout = {
    plot_bgcolor: getCSS('--bg-color'),
    paper_bgcolor: getCSS('--bg-color'),
    title: {
        text: 'Redes sociais que os usuários mais gostam',
        x: 0,
        font: {
            color: getCSS('--primary-color'),
            family: getCSS('--font'),
            size: 30
        }
    },
    legend: {
        font: {
            color: getCSS('--primary-color'),
            size: 16
        }
    }
}
import { getCSS } from "./common.js"

async function redesFavoritasMundo() {
    const url = 'https://raw.githubusercontent.com/guilhermeonrails/api/main/redes-favoritas.json'
    const res = await fetch(url)
    const dados = await res.json()
    const redes = Object.keys(dados)
    const valores = Object.values(dados)

    const data = [
        {
            values: valores,
            labels: redes,
            type: 'pie',
            textinfo: 'label+percent'
        }
    ]

    const layout = {
        plot_bgcolor: getCSS('--bg-color'),
        paper_bgcolor: getCSS('--bg-color'),
        title: {
            text: 'Redes sociais que os usuários mais gostam',
            x: 0,
            font: {
                color: getCSS('--primary-color'),
                family: getCSS('--font'),
                size: 30
            }
        },
        legend: {
            font: {
                color: getCSS('--primary-color'),
                size: 16
            }
        }
    }

    const grafico = document.createElement('div')
    grafico.className = 'grafico'
    document.getElementById('graficos-container').appendChild(grafico)
    Plotly.newPlot(grafico, data, layout)
}

redesFavoritasMundo()
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redes Sociais</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://cdn.plot.ly/plotly-2.27.0.min.js" charset="utf-8"></script>
</head>
<body>
    <header>
        <h1>Relatório das redes sociais</h1>
        <nav>
            <a href="index.html">Mundo</a>
            <a href="#">Minha escola</a>
        </nav>
    </header>
    <main class="graficos-section">
        <section id="graficos-container" class="graficos-container">
            <!-- crie os gráficos/texto aqui -->
        </section>
    </main>
    <footer>
        <p>Desenvolvido por Gui Lima</p>
    </footer>
    <script type="module" src="graficos/common.js"></script>
    <script type="module" src="graficos/informacoesGlobais.js"></script>
    <script type="module" src="graficos/quantidadeUsuarios.js"></script>
    <script type="module" src="graficos/redesFavoritasMundo.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redes Sociais - Minha escola</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://cdn.plot.ly/plotly-2.27.0.min.js" charset="utf-8"></script>
</head>
<body>
    <header>
        <h1>Relatório das redes sociais</h1>
        <nav>
            <a href="index.html">Mundo</a>
            <a href="minha-escola.html">Minha escola</a>
        </nav>
    </header>
    <main class="graficos-section">
        <section id="graficos-container" class="graficos-container">
            <!-- crie os gráficos/texto aqui -->
        </section>
    </main>
    <footer>
        <p>Desenvolvido por Gui Lima</p>
    </footer>
    <script type="module" src="graficos/common.js"></script>
</body>
</html>
const data = [
  {
    values: valores,
    labels: redes,
    type: 'pie',
    textinfo: 'label+percent'
  }
]

const layout = {
  plot_bgcolor: getCSS('--bg-color'),
  paper_bgcolor: getCSS('--bg-color'),
  height: 700,
  title: {
    text: 'Redes sociais que os usuários mais gostam',
    x: 0,
    font: {
      color: getCSS('--primary-color'),
      family: getCSS('--font'),
      size: 30
    }
  },
  legend: {
    font: {
      color: getCSS('--primary-color'),
      size: 16
    }
  }
}

criarGrafico(data, layout)


