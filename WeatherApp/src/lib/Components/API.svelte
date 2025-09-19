<script>

  

    async function loadWeather() 
    {
        const response = await fetch ("https://api.open-meteo.com/v1/forecast?latitude=45.8795&longitude=170.5006&daily=weather_code&current=temperature_2m,rain,relative_humidity_2m&timezone=Pacific%2FAuckland");
        const allWeather = await response.json();
        
       
            const card=document.getElementById("currentWeather");
            card.innerHTML=`
            <h2>Current Weather</h2>
            <h3>Latitude</h3>
            <p>${allWeather.latitude}</p>
            <h3>Longitude</h3>
            <p>${allWeather.longitude}</p>
            <h3>Generation Time</h3>
            <p>${allWeather.generationtime_ms}</p>
            <h3>UTC Offset</h3>
            <p>${allWeather.utc_offset_seconds}</p>
            <h3>Timezone</h3>
            <p>${allWeather.timezone_abbreviation}</p>
            <h3>Elevation</h3>
            <p>${allWeather.elevation}</p>
            <h3>Temperature</h3>
            <p>${allWeather.current.temperature_2m}</p>
            <h3>Humidity</h3>
            <p>${allWeather.current.relative_humidity_2m}</p>
           
            `
 
        }
        loadWeather();
    </script>
        
    
    	
