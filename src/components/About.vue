<template>
    <section id="aboutContainer">
        <h4>About the Project</h4>
        <p>
			Seatsmart offers a convenient way to to manage classrooms by encouraging learners to make positive contributions during a lesson. 
		</p>
		<p>
			Instructors can use the application to track each student's participation throughout the course.  This makes feedback to students more transparent and actionable.
		</p>
		<p>
			Information security was carefully considered in the development of Seatsmart.  The basic features of the application do not require Internet access.  All data is stored locally on your computer.  This data is intended to remain on your local hard drive and not transfered to any cloud storage system.  This helps ensure that data related to students remains confidential.  Records in Seatsmart may relate to a student's academic performance and therefore should be protected just as any other grades.
		</p>
    </section>
</template>

<script>
export default {
    name: 'About'
}
</script>

<style scoped>
#aboutContainer {
    padding: 100px 25px;
}

h4 {
    text-align: center;
    margin: 0 0 20px 0;
}

p {
    line-height: 1.8;
    margin: 15px auto;
    max-width: 800px;
}

a {
    color: var(--black);
}
</style>
