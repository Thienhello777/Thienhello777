<h1>Bonjour 👋, It's me again, Albert!</h1>
<p>Data Scientist & Quant Trader</p>
<h2>🚀 Languages and Tools I Use</h2>
<p><a target="_blank" href="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" style="display: inline-block;"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="42" height="42" /></a>
<a target="_blank" href="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" style="display: inline-block;"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="c" width="42" height="42" /></a>
<a target="_blank" href="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" style="display: inline-block;"><img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="42" height="42" /></a>
<a target="_blank" href="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" style="display: inline-block;"><img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="42" height="42" /></a>
<a target="_blank" href="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" style="display: inline-block;"><img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="42" height="42" /></a>
<a target="_blank" href="https://www.vectorlogo.zone/logos/pytorch/pytorch-icon.svg" style="display: inline-block;"><img src="https://www.vectorlogo.zone/logos/pytorch/pytorch-icon.svg" alt="pytorch" width="42" height="42" /></a>
<a target="_blank" href="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" style="display: inline-block;"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="42" height="42" /></a>
<a target="_blank" href="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" style="display: inline-block;"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="postgresql" width="42" height="42" /></a>
<a target="_blank" href="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" style="display: inline-block;"><img src="https://www.vectorlogo.zone/logos/sqlite/sqlite-icon.svg" alt="sqlite" width="42" height="42" /></a>
<a target="_blank" href="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" style="display: inline-block;"><img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="42" height="42" /></a>
<a target="_blank" href="https://www.vectorlogo.zone/logos/unity3d/unity3d-icon.svg" style="display: inline-block;"><img src="https://www.vectorlogo.zone/logos/unity3d/unity3d-icon.svg" alt="unity" width="42" height="42" /></a></p>
<h2>⚡️ Where to find me</h2>
<p><a target="_blank" href="https://www.linkedin.com/in/www.linkedin.com/in/albert-tran-3a810a248" style="display: inline-block;"><img src="https://img.shields.io/badge/linkedin-logo?style=for-the-badge&logo=linkedin&logoColor=white&color=#0a77b6" alt="linkedin" /></a></p>
<h2 align="center"> 🇻🇳 Hồ Chí Minh City's Weather ⛅ </h2>
<table align="center" style="width:50%" id="weatherTable">
    <tr style="text-align:center">
        <th>Weather</th>
        <th>Temperature</th>
        <th>Sunrise</th>
        <th>Sunset</th>
        <th>Humidity</th>
    </tr>
    <tr style="text-align:center" id="weatherData">
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>

<script>
    const latitude = 10.7626; // Vĩ độ của TP. Hồ Chí Minh
    const longitude = 106.6602; // Kinh độ của TP. Hồ Chí Minh
    const apiUrl = `https://api.open-meteo.com/v1/forecast?latitude=${latitude}&longitude=${longitude}&current_weather=true&hourly=temperature_2m,relativehumidity_2m`;

    function updateWeather() {
        fetch(apiUrl)
            .then(response => response.json())
            .then(data => {
                const weatherCode = data.current_weather.weathercode;
                const weatherDescription = getWeatherDescription(weatherCode);
                const weatherIconUrl = getWeatherIconUrl(weatherCode);
                const temperature = Math.round(data.current_weather.temperature);
                const sunrise = new Date(data.daily.sunrise[0]).toLocaleTimeString();
                const sunset = new Date(data.daily.sunset[0]).toLocaleTimeString();
                const humidity = Math.round(data.hourly.relativehumidity_2m[0]);

                document.getElementById('weatherData').innerHTML = `
                    <td>${weatherDescription}<img width="15" src="${weatherIconUrl}"></td>
                    <td>${temperature}°C</td>
                    <td>${sunrise}</td>
                    <td>${sunset}</td>
                    <td>${humidity}%</td>
                `;
            })
            .catch(error => console.error('Error fetching weather data:', error));
    }

    function getWeatherDescription(weatherCode) {
        // ... (Ánh xạ mã thời tiết sang mô tả bằng tiếng Việt, bạn có thể tự định nghĩa)
    }

    function getWeatherIconUrl(weatherCode) {
        // ... (Ánh xạ mã thời tiết sang URL biểu tượng thời tiết, bạn có thể tự định nghĩa hoặc sử dụng dịch vụ bên ngoài)
    }

    // Cập nhật thời tiết ban đầu
    updateWeather();

    // Cập nhật thời tiết sau mỗi 15 phút (900000 milliseconds)
    setInterval(updateWeather, 900000);
</script>

<p><img align="center" src="https://github-readme-stats.vercel.app/api?username=Thienhello777&show_icons=true&locale=en" alt="Thienhello777" /></p>
<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=Thienhello777&" alt="Thienhello777" /></p>
<p><img src="https://github-readme-stats.vercel.app/api/top-langs?username=Thienhello777&show_icons=true&locale=en&layout=compact" alt="Thienhello777" /></p>
<img align="right" height="150" src="https://giphy.com/gifs/capcom-mega-man-x-megamanx-jPHUl95YP4sFl24O1z"  />

