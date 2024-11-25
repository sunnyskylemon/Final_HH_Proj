# Final_HH_Proj
Final Project for the discipline "Python for Data Analysis" (MEPHI)
ссылка на gitignore-файл:
https://drive.google.com/drive/u/1/folders/1D7fICoKSprlF28YOlIYg9zW0QpbUimuP

Визуализация для задания 1:
Гистограмма:
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="age_histogram"></div>
    <script>
        var data = [
            {
                "type": "histogram",
                "x": [/* Вставьте данные по возрастам */],
                "nbinsx": 30
            }
        ];
        var layout = {
            "title": "Распределение возраста соискателей",
            "xaxis": {"title": "Возраст"},
            "yaxis": {"title": "Частота"},
            "bargap": 0.1
        };
        Plotly.newPlot("age_histogram", data, layout);
    </script>
</body>
</html>

Боксплот:
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="age_boxplot"></div>
    <script>
        var data = [
            {
                "type": "box",
                "x": [/* Вставьте данные по возрастам */],
                "name": "Возраст",
                "boxmean": true
            }
        ];
        var layout = {
            "title": "Коробчатая диаграмма возраста соискателей",
            "xaxis": {"title": "Возраст"}
        };
        Plotly.newPlot("age_boxplot", data, layout);
    </script>
</body>
</html>

Визуализация для задания 2:
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="hist_experience"></div>
    <script>
        var data = [
            {
                "type": "histogram",
                "x": [/* Вставьте данные опыта работы (в месяцах) */],
                "nbinsx": 30,
                "name": "Опыт работы (в месяцах)",
                "marker": {"color": "blue"}
            }
        ];
        var layout = {
            "title": "Распределение опыта работы (в месяцах)",
            "xaxis": {"title": "Опыт работы (месяц)"},
            "yaxis": {"title": "Частота"},
            "bargap": 0.1
        };
        Plotly.newPlot("hist_experience", data, layout);
    </script>
</body>
</html>

Визуализация для задания 3:
Гистограмма:
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="salary_histogram"></div>
    <script>
        var data = [
            {
                "type": "histogram",
                "x": [/* Вставьте данные по заработной плате (в рублях) */],
                "nbinsx": 50,
                "name": "Заработная плата (руб)",
                "marker": {"color": "blue"},
                "yaxis": "y2"
            }
        ];
        var layout = {
            "title": "Распределение заработной платы (в рублях) (логарифмическая шкала)",
            "xaxis": {"title": "Заработная плата (руб)"},
            "yaxis": {"title": "Частота (логарифмическая шкала)", "type": "log"},
            "bargap": 0.1
        };
        Plotly.newPlot("salary_histogram", data, layout);
    </script>
</body>
</html>

Боксплот:
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="salary_boxplot"></div>
    <script>
        var data = [
            {
                "type": "box",
                "x": [/* Вставьте данные по заработной плате (в рублях) */],
                "name": "Заработная плата (руб)",
                "boxmean": "true",
                "marker": {"color": "orange"}
            }
        ];
        var layout = {
            "title": "Коробчатая диаграмма заработной платы (в рублях)",
            "xaxis": {"title": "Заработная плата (руб)"}
        };
        Plotly.newPlot("salary_boxplot", data, layout);
    </script>
</body>
</html>

Визуализация для задания 4:
HTML для графика:
# Save as HTML file for GitHub
file_path = "/mnt/data/education_salary_chart.html"
fig.write_html(file_path)

file_path

<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="plot"></div>
    <script>
        var data = [{
            x: ["Высшее", "Неоконченное высшее", "Среднее специальное", "Среднее"],
            y: [120000, 100000, 85000, 60000],
            type: "bar",
            text: ["120000", "100000", "85000", "60000"],
            textposition: "outside",
            marker: {
                color: ["#08306b", "#2171b5", "#6baed6", "#c6dbef"],
                colorscale: "Blues"
            }
        }];

        var layout = {
            title: "Медианная желаемая заработная плата в зависимости от уровня образования",
            xaxis: {
                title: "Уровень образования",
                categoryorder: "total ascending"
            },
            yaxis: {
                title: "Медианная ЗП (руб)"
            },
            showlegend: false
        };

        Plotly.newPlot("plot", data, layout);
    </script>
</body>
</html>

Визуализация для задания 5:
HTML для GitHub:

<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="plot"></div>
    <script>
        var data = [{
            x: ["Москва", "Санкт-Петербург", "город-миллионник", "другие"],
            y: [[80000, 120000, 90000], [70000, 100000, 85000], [65000, 95000, 87000], [50000, 60000, 70000]],
            type: "box",
            name: "Город",
            boxpoints: "all",  // Show all data points
            marker: {color: "#2171b5"}
        }];

        var layout = {
            title: "Распределение желаемой заработной платы по городам",
            xaxis: {
                title: "Город",
                tickangle: 45
            },
            yaxis: {
                title: "Заработная плата (руб)"
            }
        };

        Plotly.newPlot("plot", data, layout);
    </script>
</body>
</html>

Визуализация для задания 6:
Диаграмма для гитхаба:
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="plot"></div>
    <script>
        var data = [
            {
                type: 'bar',
                orientation: 'h',
                x: [50000, 55000, 60000, 65000],  // Replace with your 'ЗП (руб)' values
                y: [
                    'True, True', 
                    'True, False', 
                    'False, True', 
                    'False, False'
                ],  // Replace with 'Готовность к переезду' and 'Готовность к командировкам'
                name: 'Готовность к командировкам: True',
                marker: {color: '#1f77b4'}
            },
            {
                type: 'bar',
                orientation: 'h',
                x: [48000, 53000, 58000, 63000],  // Replace with your 'ЗП (руб)' values
                y: [
                    'True, True', 
                    'True, False', 
                    'False, True', 
                    'False, False'
                ],  // Replace with 'Готовность к переезду' and 'Готовность к командировкам'
                name: 'Готовность к командировкам: False',
                marker: {color: '#ff7f0e'}
            }
        ];

        var layout = {
            title: 'Медианная з/п по готовности к командировкам/переезду',
            xaxis: {
                title: 'Медианная заработная плата (руб)'
            },
            yaxis: {
                title: 'Готовность к переезду и командировкам',
                automargin: true
            },
            barmode: 'group'
        };

        Plotly.newPlot('plot', data, layout);
    </script>
</body>
</html>

Визуализация для задания 7:
HTML для гитхаба:
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="plot"></div>
    <script>
        var data = [
            {
                type: 'bar',
                orientation: 'h',
                x: [50000, 55000, 60000, 65000],  // Replace with your 'ЗП (руб)' values
                y: [
                    'True, True', 
                    'True, False', 
                    'False, True', 
                    'False, False'
                ],  // Replace with 'Готовность к переезду' and 'Готовность к командировкам'
                name: 'Готовность к командировкам: True',
                marker: {color: '#1f77b4'}
            },
            {
                type: 'bar',
                orientation: 'h',
                x: [48000, 53000, 58000, 63000],  // Replace with your 'ЗП (руб)' values
                y: [
                    'True, True', 
                    'True, False', 
                    'False, True', 
                    'False, False'
                ],  // Replace with 'Готовность к переезду' and 'Готовность к командировкам'
                name: 'Готовность к командировкам: False',
                marker: {color: '#ff7f0e'}
            }
        ];

        var layout = {
            title: 'Медианная з/п по готовности к командировкам/переезду',
            xaxis: {
                title: 'Медианная заработная плата (руб)'
            },
            yaxis: {
                title: 'Готовность к переезду и командировкам',
                automargin: true
            },
            barmode: 'group'
        };

        Plotly.newPlot('plot', data, layout);
    </script>
</body>
</html>

Вывод графика для задания 8:
HTML для GitHub:

<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="scatter-plot"></div>
    <script>
        var data = [
            {
                x: [20, 25, 30, 35, 40, 45, 50],  // Replace with real 'Возраст' data
                y: [1.5, 2, 3, 4, 5, 6, 7],      // Replace with real 'Опыт работы (год)' data
                mode: 'markers',
                type: 'scatter',
                name: 'Данные соискателей',
                opacity: 0.6,
                marker: { size: 10 }
            },
            {
                x: [0, 100],
                y: [0, 100],
                mode: 'lines',
                name: 'Прямая y = x',
                line: { color: 'red', dash: 'dash' }
            }
        ];

        var layout = {
            title: 'Зависимость опыта работы от возраста',
            xaxis: {
                title: 'Возраст (годы)',
                range: [0, 100]
            },
            yaxis: {
                title: 'Опыт работы (годы)',
                range: [0, 100]
            },
            legend: {
                title: { text: 'Обозначения' },
                font: { size: 10 }
            }
        };

        Plotly.newPlot('scatter-plot', data, layout);
    </script>
</body>
</html>


ХТМЛ для задания с доп. баллами:

Код для Гитхаба:
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <!-- График 1: Распределение заработной платы по готовности к переезду -->
    <div id="salary-relocation"></div>
    <script>
        var relocation_data = [
            {
                y: [30000, 45000, 60000, 80000, 100000],  // Replace with actual salary data for ready to relocate
                name: 'Готов к переезду',
                type: 'box',
                marker: { color: 'blue' },
                boxpoints: 'all'
            },
            {
                y: [25000, 40000, 55000, 70000, 85000],  // Replace with actual salary data for not ready to relocate
                name: 'Не готов к переезду',
                type: 'box',
                marker: { color: 'orange' },
                boxpoints: 'all'
            }
        ];

        var relocation_layout = {
            title: 'Распределение желаемой заработной платы по готовности к переезду',
            xaxis: { title: 'Готовность к переезду', tickvals: [1, 2], ticktext: ['Готов', 'Не готов'] },
            yaxis: { title: 'Заработная плата (руб)' },
            showlegend: false
        };

        Plotly.newPlot('salary-relocation', relocation_data, relocation_layout);
    </script>

    <!-- График 2: Влияние возраста на медианную заработную плату -->
    <div id="age-salary"></div>
    <script>
        var age_salary_data = [
            {
                x: [25, 30, 35, 40, 45, 50],  // Replace with actual age data
                y: [40000, 50000, 60000, 70000, 80000, 90000],  // Replace with actual median salary data
                mode: 'markers',
                name: 'Данные',
                marker: { size: 10, color: 'blue' }
            },
            {
                x: [20, 60],  // Replace with trendline x-coordinates
                y: [35000, 95000],  // Replace with trendline y-coordinates
                mode: 'lines',
                name: 'Тренд',
                line: { color: 'red', dash: 'dash' }
            }
        ];

        var age_salary_layout = {
            title: 'Влияние возраста на медианную заработную плату',
            xaxis: { title: 'Возраст (годы)' },
            yaxis: { title: 'Медианная Заработная Плата (руб)' },
            legend: { title: { text: 'Обозначения' } }
        };

        Plotly.newPlot('age-salary', age_salary_data, age_salary_layout);
    </script>
</body>
</html>
Последняя диаграмма:

HTML для Гитхаба:
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>
    <div id="log-age-distribution"></div>
    <script>
        var clear_df = {
            x: [/* Replace with clear_df['log_Возраст'] values */],  // Логарифмы возраста
            type: 'histogram',
            nbinsx: 20,
            name: 'Логарифм возраста',
            marker: { color: '#1f77b4' }
        };

        // Среднее значение и стандартное отклонение
        var mean_log_age = /* Replace with mean_log_age */;
        var std_log_age = /* Replace with std_log_age */;

        var layout = {
            title: 'Распределение логарифма возраста соискателей',
            xaxis: { title: 'Логарифм возраста' },
            yaxis: { title: 'Частота' },
            shapes: [
                {
                    type: 'line',
                    x0: mean_log_age,
                    x1: mean_log_age,
                    y0: 0,
                    y1: 1,
                    yref: 'paper',
                    line: {
                        color: 'black',
                        width: 2
                    },
                    name: 'Среднее'
                },
                {
                    type: 'line',
                    x0: mean_log_age - 3 * std_log_age,
                    x1: mean_log_age - 3 * std_log_age,
                    y0: 0,
                    y1: 1,
                    yref: 'paper',
                    line: {
                        color: 'red',
                        width: 2,
                        dash: 'dash'
                    },
                    name: '-3σ'
                },
                {
                    type: 'line',
                    x0: mean_log_age + 4 * std_log_age,
                    x1: mean_log_age + 4 * std_log_age,
                    y0: 0,
                    y1: 1,
                    yref: 'paper',
                    line: {
                        color: 'red',
                        width: 2,
                        dash: 'dash'
                    },
                    name: '+4σ'
                }
            ]
        };

        Plotly.newPlot('log-age-distribution', [clear_df], layout);
    </script>
</body>
</html>
