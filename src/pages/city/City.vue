<template>
    <div>
        <city-header></city-header>
        <city-search :cities="cities"></city-search>
        <city-list
            :cities="cities"
            :hotCities="hotCities"
            :letter="letter"
        ></city-list>
        <city-alpabet
            :cities="cities"
            @change="handleLetterChange"
        ></city-alpabet>
    </div>
</template>

<script>
    import axios from "axios"
    import CityHeader from "./components/Header"
    import CitySearch from "./components/Search"
    import CityList from "./components/List"
    import CityAlpabet from "./components/Alphabet"

    export default {
        name: "City",
        components: {
            CityHeader,
            CitySearch,
            CityList,
            CityAlpabet
        },
        data() {
            return {
                cities: {},
                hotCities: [],
                letter: ""
            }
        },
        methods: {
            getCityInfo() {
                axios.get("/api/city.json")
                // axios.get("http://47.98.251.187/api/city.json")
                    .then(this.handleGetCityInfoSucc)
            },
            handleGetCityInfoSucc(res) {
                res = res.data
                if (res.ret && res.data) {
                    const data = res.data
                    this.cities = data.cities
                    this.hotCities = data.hotCities
                }
            },
            handleLetterChange(letter) {
                this.letter = letter
            }
        },
        mounted() {
            this.getCityInfo()
        }
    }
</script>

<style lang="stylus" scoped>
</style>
