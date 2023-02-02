<template>
  <div >
    <div class="page-title">
        <h1><span></span> Weather</h1>
    </div>
    <div class="weatherApp">
    <div class="weather pt-3 pb-3">
      <div class="weather-header">
        <input
          type="search"
          class="search-box m-1"
          autocomplete="on"
          placeholder="search for a city..."
          v-model="cityName"
        />
        <button
          type="button"
          @click="getCityWeather(cityName)"
          class="btn bg-light "
        >
          <i class="fa-solid fa-magnifying-glass"></i>
        </button>
        <button
          type="button"
          @click="getLocationWeather()"
          class="btn bg-light"
        >
          <i class="fas fa-map-marker-alt"></i>
        </button>
      </div>
      <div class="weather-body" v-if="weather.name">
        <section class="location">
          <div class="city">{{ weather.name }}, {{ weather.sys.country }}</div>
          <div class="date">{{ dateBuilder(weather.dt) }}</div>
        </section>
        <div class="current">
          <div class="temp">
            {{ Math.round(weather.main.temp) }}<span>°C</span>
          </div>
          <div class="weather-status">{{ weather.weather[0].main }}</div>
          <div class="hi-low">
            {{ Math.round(weather.main.temp_min) }}°C /
            {{ Math.round(weather.main.temp_max) }}°C ...feels like :
            {{ Math.round(weather.main.feels_like) }}°C
          </div>
          <div class="weather-humidity">
            <span> humidity</span>
            {{ weather.main.humidity }} %
          </div>
          <div class="weather-wind">
            wind speed
            {{ weather.wind.speed }} Meters/sec
          </div>

          <div></div>
        </div>
      </div>
      <div v-else class="error-msg">{{ errorMsg }}</div>
    </div>
  </div>
</div>
</template>
<script>
export default {
  name: "Weather",
  data() {
    return {
      weather: {},
      api: {
        key: "b0a850e4b20d81310003353b66ffe05a",
        base: "https://api.openweathermap.org/data/2.5/",
      },
      cityName: "Arnhem",
      errorMsg: null,
    };
  },
  created() {
    this.getCityWeather()
  },
  methods: {
    
    getCityWeather() {
      this.weather = {};
      if (this.cityName) {
        this.fetchData(`${this.api.base}weather?q=${this.cityName}&units=metric&APPID=${this.api.key}`);
      }
    },
    getLocationWeather() {
      this.weather = {};
      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(this.displayWeather, this.showError);
      } else {
        this.errorMsg = "Geolocation is not supported by this browser.";
      }
    },
    displayWeather(position) {
      let lat = position.coords.latitude;
      let lon = position.coords.longitude;
      this.fetchData(`${this.api.base}weather?&units=metric&lat=${lat}&lon=${lon}&appid=${this.api.key}`);
    },
    showError(error) {
      switch (error.code) {
        case error.PERMISSION_DENIED:
          this.errorMsg = "User denied the request for Geolocation.";
          break;
        case error.POSITION_UNAVAILABLE:
          this.errorMsg = "Location information is unavailable.";
          break;
        case error.TIMEOUT:
          this.errorMsg = "The request to get user location timed out.";
          break;
        case error.UNKNOWN_ERROR:
          this.errorMsg = "An unknown error occurred.";
          break;
      }
    },
    fetchData(URL) {
       
      fetch(URL)
        .then((weather) => {
          return weather.json();
        })
        .then(this.DisplayResult);
    },
    DisplayResult(weather) {
      if (weather.name) {
        this.weather = weather;
      }
      if (weather.message) this.errorMsg = weather.message;
    },

    dateBuilder(d) {
      let months = [
        "January",
        "February",
        "March",
        "April",
        "May",
        "June",
        "July",
        "August",
        "September",
        "October",
        "November",
        "December",
      ];
      let days = [
        "Sunday",
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday",
      ];
      var dt = new Date(d * 1000);
      let day = days[dt.getDay()];
      let date = dt.getDate();
      let month = months[dt.getMonth()];
      let year = dt.getFullYear();

      return `${day} ${date} ${month} ${year}`;
    },
  },
};
</script>
<style>
.weatherApp {
  margin: 0;
  padding: 0;
  background: url("@/assets/img/bg-weather.jpg") no-repeat;
  background-size: cover;
  background-position: center;
}
.weather {
  font-size: 0.8em;
  margin-top: 20px;
  flex-direction: column;
  border-radius: 5px;
  border: 3px solid #66a8ea58;;
  background-image: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0.3),
    rgba(0, 0, 0, 0.6)
  );
}
.weather-header {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 50px 15px 15px;
}

.weather-header input {
  width: 100%;
  max-width: 280px;
  padding: 10px 15px;
  border: none;
  outline: none;

  border-radius: 16px 0px 16px 0px;
  border-bottom: 3px solid #df8e00;

  color: #313131;
  font-size: 20px;
  font-weight: 300;
  transition: 0.2s ease-out;
}

.weather-header input:focus {
  background-color: rgba(255, 255, 255, 0.6);
}
.weather .btn {
  margin: 5px;
  padding: 10px 15px;
}
.weather-body {
  flex: 1 1 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.location .city {
  color: #fff;
  font-size: 4.5em;
  font-weight: 500;
  margin-bottom: 5px;
}

.location .date {
  color: #fff;
  font-size: 2.5em;
}

.current .temp {
  color: #fff;
  font-size: 4em;
  font-weight: 4em;
  margin: 30px 0px;
  text-shadow: 2px 10px rgba(0, 0, 0, 0.6);
}

.current .temp span {
  font-weight: 50;
}

.current .weather-status {
  color: #fff;
  font-size: 3em;
  font-weight: 70;
  font-style: italic;
  margin-bottom: 15px;
  text-shadow: 0px 3px rgba(0, 0, 0, 0.4);
}

.current .hi-low,
.weather-humidity,
.weather-wind {
  color: #fff;
  font-size: 3em;
  font-weight: 500;
  text-shadow: 0px 4px rgba(0, 0, 0, 0.4);
}
.error-msg {
  font-size: 1.5em;
  color: red;
  text-align: center;
}
@media (max-width: 480px) {
  .weather{
    font-size: 0.5em;
  }
  }
</style>
