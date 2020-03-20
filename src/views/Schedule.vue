<template>
    <div class="schedual">
        <h1>מערכת שעות</h1>
        <div class="days">
            <div v-for="(day, index) in days" :key.sync="index" class="frame-day">
                <a v-on:click="updateSelectedDay">
                    <div class="day">
                        {{day}}
                    </div>
                </a>
            </div>
        </div>
        <div class="schedual-details-container">
            <h2>{{this.selectedDay}}</h2>
            <div v-if="this.selectedDay === 'ראשון'" class="schedual-details">
                <TrainAndTime v-for="(trainTime, index) in trainTimeSunday" :train="trainTime.train" :time="trainTime.time" :key.sync="index">
                </TrainAndTime>
            </div>
            <div v-else-if="this.selectedDay === 'שני'" class="schedual-details">
                <TrainAndTime v-for="(trainTime, index) in trainTimeMonday" :train="trainTime.train" :time="trainTime.time" :key.sync="index">
                </TrainAndTime>
            </div>
            <div v-else-if="this.selectedDay === 'שלישי'" class="schedual-details">
                <TrainAndTime v-for="(trainTime, index) in trainTimeTuesday" :train="trainTime.train" :time="trainTime.time" :key.sync="index">
                </TrainAndTime>
            </div>
            <div v-else-if="this.selectedDay === 'רביעי'" class="schedual-details">
                <TrainAndTime v-for="(trainTime, index) in trainTimeWednesday" :train="trainTime.train" :time="trainTime.time" :key.sync="index">
                </TrainAndTime>
            </div>
            <div v-else-if="this.selectedDay === 'חמישי'" class="schedual-details">
                <TrainAndTime v-for="(trainTime, index) in trainTimeThursday" :train="trainTime.train" :time="trainTime.time" :key.sync="index">
                </TrainAndTime>
            </div>
            <div v-else-if="this.selectedDay === 'שישי'" class="schedual-details">
                <TrainAndTime v-for="(trainTime, index) in trainTimeFriday" :train="trainTime.train" :time="trainTime.time" :key.sync="index">
                </TrainAndTime>
            </div>
            <div v-else class="schedual-details">
                <TrainAndTime v-for="(trainTime, index) in trainTimeSaturday" :train="trainTime.train" :time="trainTime.time" :key.sync="index">
                </TrainAndTime>
            </div>
        </div>
        <Footer></Footer>
    </div>
</template>

<script>
import TrainAndTime from "@/components/TrainAndTime.vue";
import Footer from "@/components/Footer.vue";

export default {
    name: "schedule",
    components: {
        TrainAndTime,
        Footer
    },
     data(){
        return{
            days: ["ראשון", "שני", "שלישי", "רביעי", "חמישי", "שישי", "שבת"],
            selectedDay: "ראשון",
            trainTimeSunday: [
                {
                    train: "CrossFit", 
                    time: "06:00"
                },
                {
                    train: "Open Gym",
                    time: "06:00"
                },
                {
                    train: "CrossFit", 
                    time: "07:00"
                },
                {
                    train: "Open Gym",
                    time: "07:00"
                },
                {
                    train: "Yoga", 
                    time: "07:00"
                },
                {
                    train: "Burn", 
                    time: "08:00"
                },
                {
                    train: "Open Gym",
                    time: "08:00"
                },
                {
                    train: "CrossFit", 
                    time: "09:00"
                },
                {
                    train: "Open Gym",
                    time: "09:00"
                },
                {
                    train: "Burn",
                    time: "09:30"
                },
                {
                    train: "Open Gym",
                    time: "10:00"
                },
                {
                    train: "CrossFit", 
                    time: "11:00"
                },
                {
                    train: "Burn",
                    time: "11:30"
                },
                {
                    train: "CrossFit", 
                    time: "12:00"
                },
                {
                    train: "Open Gym",
                    time: "13:00"
                },
                {
                    train: "CrossFit", 
                    time: "14:00"
                },
                {
                    train: "CrossFit", 
                    time: "15:00"
                },
                {
                    train: "CrossFit", 
                    time: "16:00"
                },
                {
                    train: "CrossFit", 
                    time: "17:00"
                },
                {
                    train: "Burn", 
                    time: "18:00"
                },
                {
                    train: "Burn", 
                    time: "19:00"
                },
                {
                    train: "CrossFit", 
                    time: "19:00"
                },
                {
                    train: "Body Power", 
                    time: "20:00"
                },
                {
                    train: "Yoga", 
                    time: "20:00"
                },
                {
                    train: "Open Gym", 
                    time: "21:00"
                }
            ],
            trainTimeMonday: [
                {
                    train: "CrossFit", 
                    time: "06:00"
                },
                {
                    train: "Open Gym",
                    time: "06:00"
                },
                {
                    train: "Body Shape", 
                    time: "07:00"
                },
                {
                    train: "Open Gym",
                    time: "07:00"
                },
                {
                    train: "Yoga", 
                    time: "07:00"
                },
                {
                    train: "Burn", 
                    time: "08:00"
                },
                {
                    train: "Open Gym",
                    time: "08:00"
                },
                {
                    train: "Body Shape", 
                    time: "09:00"
                },
                {
                    train: "Open Gym",
                    time: "09:00"
                },
                {
                    train: "Zumba",
                    time: "09:30"
                },
                {
                    train: "Open Gym",
                    time: "10:00"
                },
                {
                    train: "Zumba", 
                    time: "11:00"
                },
                {
                    train: "Burn",
                    time: "11:30"
                },
                {
                    train: "CrossFit", 
                    time: "12:00"
                },
                {
                    train: "Open Gym",
                    time: "13:00"
                },
                {
                    train: "Body Power", 
                    time: "14:00"
                },
                {
                    train: "CrossFit", 
                    time: "15:00"
                },
                {
                    train: "CrossFit", 
                    time: "16:00"
                },
                {
                    train: "Trampoline ", 
                    time: "17:00"
                },
                {
                    train: "Trampoline ", 
                    time: "18:00"
                },
                {
                    train: "Trampoline ", 
                    time: "19:00"
                },
                {
                    train: "CrossFit", 
                    time: "19:00"
                },
                {
                    train: "Body Power", 
                    time: "20:00"
                },
                {
                    train: "Yoga", 
                    time: "20:00"
                },
                {
                    train: "Open Gym", 
                    time: "21:00"
                }
            ],
            trainTimeTuesday: [
                {
                    train: "Pilates Mattress", 
                    time: "06:00"
                },
                {
                    train: "Open Gym",
                    time: "06:00"
                },
                {
                    train: "Pilates Mattress", 
                    time: "07:00"
                },
                {
                    train: "Open Gym",
                    time: "07:00"
                },
                {
                    train: "Pilates Mattress", 
                    time: "07:00"
                },
                {
                    train: "Burn", 
                    time: "08:00"
                },
                {
                    train: "Open Gym",
                    time: "08:00"
                },
                {
                    train: "Body Shape", 
                    time: "09:00"
                },
                {
                    train: "Open Gym",
                    time: "09:00"
                },
                {
                    train: "Zumba",
                    time: "09:30"
                },
                {
                    train: "Open Gym",
                    time: "10:00"
                },
                {
                    train: "Zumba", 
                    time: "11:00"
                },
                {
                    train: "Kickbox",
                    time: "11:30"
                },
                {
                    train: "Open Gym", 
                    time: "12:00"
                },
                {
                    train: "Kickbox",
                    time: "13:00"
                },
                {
                    train: "Body Power", 
                    time: "14:00"
                },
                {
                    train: "Kickbox", 
                    time: "15:00"
                },
                {
                    train: "Body Power", 
                    time: "16:00"
                },
                {
                    train: "Trampoline ", 
                    time: "17:00"
                },
                {
                    train: "Trampoline ", 
                    time: "18:00"
                },
                {
                    train: "Trampoline ", 
                    time: "19:00"
                },
                {
                    train: "Body Power", 
                    time: "19:00"
                },
                {
                    train: "Body Power", 
                    time: "20:00"
                },
                {
                    train: "Body Power", 
                    time: "20:00"
                },
                {
                    train: "Open Gym", 
                    time: "21:00"
                }
            ],
            trainTimeWednesday: [
                {
                    train: "Pilates Mattress", 
                    time: "06:00"
                },
                {
                    train: "Open Gym",
                    time: "06:00"
                },
                {
                    train: "Pilates Mattress", 
                    time: "07:00"
                },
                {
                    train: "Open Gym",
                    time: "07:00"
                },
                {
                    train: "Pilates Mattress", 
                    time: "07:00"
                },
                {
                    train: "Burn", 
                    time: "08:00"
                },
                {
                    train: "Open Gym",
                    time: "08:00"
                },
                {
                    train: "Pilates Machine", 
                    time: "09:00"
                },
                {
                    train: "Open Gym",
                    time: "09:00"
                },
                {
                    train: "Zumba",
                    time: "09:30"
                },
                {
                    train: "Open Gym",
                    time: "10:00"
                },
                {
                    train: "Zumba", 
                    time: "11:00"
                },
                {
                    train: "Pilates Machine",
                    time: "11:30"
                },
                {
                    train: "Open Gym", 
                    time: "12:00"
                },
                {
                    train: "Pilates Machine",
                    time: "13:00"
                },
                {
                    train: "Body Power", 
                    time: "14:00"
                },
                {
                    train: "Kickbox", 
                    time: "15:00"
                },
                {
                    train: "Kickbox", 
                    time: "16:00"
                },
                {
                    train: "Trampoline ", 
                    time: "17:00"
                },
                {
                    train: "Trampoline ", 
                    time: "18:00"
                },
                {
                    train: "Trampoline ", 
                    time: "19:00"
                },
                {
                    train: "Body Power", 
                    time: "19:00"
                },
                {
                    train: "Body Power", 
                    time: "20:00"
                },
                {
                    train: "Body Power", 
                    time: "20:00"
                },
                {
                    train: "Open Gym", 
                    time: "21:00"
                }
            ],
            trainTimeThursday: [
                {
                    train: "Pilates Mattress", 
                    time: "06:00"
                },
                {
                    train: "Open Gym",
                    time: "06:00"
                },
                {
                    train: "Pilates Mattress", 
                    time: "07:00"
                },
                {
                    train: "Open Gym",
                    time: "07:00"
                },
                {
                    train: "Pilates Mattress", 
                    time: "07:00"
                },
                {
                    train: "Burn", 
                    time: "08:00"
                },
                {
                    train: "Open Gym",
                    time: "08:00"
                },
                {
                    train: "Yoga", 
                    time: "09:00"
                },
                {
                    train: "Open Gym",
                    time: "09:00"
                },
                {
                    train: "Yoga",
                    time: "09:30"
                },
                {
                    train: "Open Gym",
                    time: "10:00"
                },
                {
                    train: "Body Power", 
                    time: "11:00"
                },
                {
                    train: "Pilates Machine",
                    time: "11:30"
                },
                {
                    train: "Open Gym", 
                    time: "12:00"
                },
                {
                    train: "Pilates Machine",
                    time: "13:00"
                },
                {
                    train: "Body Power", 
                    time: "14:00"
                },
                {
                    train: "Kickbox", 
                    time: "15:00"
                },
                {
                    train: "Kickbox", 
                    time: "16:00"
                },
                {
                    train: "Trampoline ", 
                    time: "17:00"
                },
                {
                    train: "Trampoline ", 
                    time: "18:00"
                },
                {
                    train: "Trampoline ", 
                    time: "19:00"
                },
                {
                    train: "Burn", 
                    time: "19:00"
                },
                {
                    train: "Burn", 
                    time: "20:00"
                },
                {
                    train: "CrossFit", 
                    time: "20:00"
                },
                {
                    train: "CrossFit", 
                    time: "21:00"
                }
            ],
            trainTimeFriday: [
                {
                    train: "Body Shape", 
                    time: "06:00"
                },
                {
                    train: "Open Gym",
                    time: "06:00"
                },
                {
                    train: "Body Power", 
                    time: "07:00"
                },
                {
                    train: "Open Gym",
                    time: "07:00"
                },
                {
                    train: "Zumba", 
                    time: "07:00"
                },
                {
                    train: "Zumba", 
                    time: "08:00"
                },
                {
                    train: "Open Gym",
                    time: "08:00"
                },
                {
                    train: "Yoga", 
                    time: "09:00"
                },
                {
                    train: "Open Gym",
                    time: "09:00"
                },
                {
                    train: "Yoga",
                    time: "09:30"
                },
                {
                    train: "Open Gym",
                    time: "10:00"
                },
                {
                    train: "Kikbox", 
                    time: "11:00"
                },
                {
                    train: "Pilates Machine",
                    time: "11:30"
                },
                {
                    train: "Open Gym", 
                    time: "12:00"
                },
                {
                    train: "Pilates Machine",
                    time: "13:00"
                },
                {
                    train: "Body Power", 
                    time: "14:00"
                }
            ],
            trainTimeSaturday: [
                {
                    train: "Open Gym",
                    time: "10:00"
                },
                {
                    train: "Yoga", 
                    time: "11:00"
                },
                {
                    train: "Burn",
                    time: "11:30"
                },
                {
                    train: "Open Gym", 
                    time: "12:00"
                },
                {
                    train: "Yoga",
                    time: "13:00"
                },
                {
                    train: "Zumba", 
                    time: "14:00"
                },
                {
                    train: "Kickbox", 
                    time: "15:00"
                },
                {
                    train: "Kickbox", 
                    time: "16:00"
                },
                {
                    train: "Trampoline ", 
                    time: "17:00"
                },
                {
                    train: "Trampoline ", 
                    time: "18:00"
                },
                {
                    train: "Trampoline ", 
                    time: "19:00"
                },
                {
                    train: "Burn", 
                    time: "19:00"
                },
                {
                    train: "Burn", 
                    time: "20:00"
                },
                {
                    train: "CrossFit", 
                    time: "20:00"
                }
            ]
        }
    },
    methods: {
        updateSelectedDay: function(event){
            this.selectedDay = event.target.innerHTML.replace(/\s+/g, '');
        }
    }
};
</script>

<style scoped>

    h1{
        font-size: 3rem;
        margin-top: 3rem;
    }

    .days{
        display: flex;
        flex-wrap: wrap;
        flex-direction: row-reverse;
        justify-content: center;
        margin: 2rem auto;
    }

    .frame-day{
        border: 0.3rem solid #2c3e50;
        width: 6.1rem;
        height: 4.5rem;
        margin: 0.3rem;
        pointer-events: none;
    }

    .day{
        border: 0.3rem solid rgb(230, 24, 24);
        width: 4.5rem;
        padding: 0.5rem;
        margin: 0.5rem auto;
        pointer-events: all;
    }

    a{
        cursor: pointer;
    }

    a:hover{
        font-weight: bold;
        background-color: cornsilk;
    }

    h2{
        margin: 1rem auto;
    }

    .schedual-details-container{
        width: 90%;
        margin: auto;
        max-width: 30rem;
    }

    .schedual-details{
        margin: 2rem auto 4rem auto;
    }
    @media (min-width: 51rem)
    {
        .frame-day{
            border: 0.5rem solid #2c3e50;
            width: 7rem;
            height: 5.3rem;
            margin: 0.3rem; 
        }

        .day{
            border: 0.5rem solid rgb(230, 24, 24);
            width: 5rem;
            padding: 0.5rem;
            margin: 0.5rem auto;
        }
    }

</style>