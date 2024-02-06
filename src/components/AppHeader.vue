<script>
export default {

}
</script>

<template>
    <header class="p-5 d-flex justify-content-between align-items-center">
        <section id="light" class="d-flex gap-2 align-items-start">
            <div class="rounded-circle big blue"></div>
            <div class="rounded-circle small red"></div>
            <div class="rounded-circle small yellow"></div>
            <div class="rounded-circle small green"></div>
        </section>

        <section id="select-type">
            <select class="form-select" aria-label="Default select example">
                <option selected>Open this select menu</option>
                <option value="1">One</option>
                <option value="2">Two</option>
                <option value="3">Three</option>
            </select>
        </section>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/_vars.scss' as *;

header {
    background-color: $bg-color;
}

.big {
    height: 50px;
    width: 50px;
    border: 2px solid white;
}

.small {
    height: 25px;
    width: 25px;
    border: 2px solid white;
}

.blue {
    background-color: $circle-blue;
    // background-size: 50px 50px;
    // background-color: linear-gradient(to bottom right, white, $circle-blue);
}

.red {
    background-color: $circle-red;
}

.yellow {
    background-color: $circle-yellow;
}

.green {
    background-color: $circle-green;
}
</style>