<template>
    <div class="circle_noshadow absolute flex items-center justify-center lg:w-56 lg:h-56 w-32 h-32 rounded-full hover:border-2 cursor-pointer">
        <div class="circle lg:w-48 lg:h-48 w-28 h-28 rounded-full bg-white bg-opacity-95 hover:bg-red flex items-center justify-center px-10 shadow-around hover:shadow-none text-red hover:text-white transition duration-200 ease-in-out">
            <h2 class="lg:text-xl text-sm text-center font-bold">{{title}}</h2>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppCircle',
    props:{
        title:{
            type: String,
            default:''
        }
    }
}
</script>

<style>
    .circle{
        animation: float 6s ease-in-out infinite;
    }
    .circle_noshadow {
        animation: float_noshadow 6s ease-in-out infinite;
    }

    @keyframes float_noshadow {
        0% {
            transform: translatey(0px);
        }
        50% {
            transform: translatey(-10px);
        }
        100% {
            transform: translatey(0px);
        }
    }
    @keyframes float {
        0% {
            box-shadow: 0 5px 15px 0px rgba(0,0,0,0.6);
            transform: translatey(0px);
        }
        50% {
            box-shadow: 0 25px 15px 0px rgba(0,0,0,0.2);
            transform: translatey(-20px);
        }
        100% {
            box-shadow: 0 5px 15px 0px rgba(0,0,0,0.6);
            transform: translatey(0px);
        }
    }

</style>