<template>
    <section id="features">
        <div class="feature">
            <h4>Easily Change Seating</h4>
            <img src="@/assets/rearrange.gif" alt="rearrange screen recording">
        </div>
        <div class="feature">
            <h4>Track Participation Trends</h4>
            <img src="@/assets/trends.gif" alt="trend recording">
        </div>
        <div class="feature">
            <h4>Customize</h4>
            <img src="@/assets/customize.gif" alt="customize settings recording">
        </div>
        <div class="feature">
            <h4>Control with a Mobile Device</h4>
            <img src="@/assets/remote.gif" alt="remote recording">
        </div>
        <div class="feature">
            <h4>Engage Students with Activities</h4>
            <img src="@/assets/activities.gif" alt="formative assessment activities">
        </div>
    </section>
</template>

<script>
export default {
    name: 'Features'
}
</script>

<style scoped>
#features {
    background: var(--black);
    padding: 150px 0;
}

.feature {
    text-align: center;
    margin-top: 200px;
}

.feature:first-child {
    margin-top: 0;
}

.feature > h4 {
    color: var(--white);
    margin: 25px 0;
}

.feature > img {
    width: 85%;
    margin: 0;
    border: 3px solid var(--yellow);
}
</style>
