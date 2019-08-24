<template>
    <section id="aboutContainer">
        <h4>About the Project</h4>
        <p>
			Seatsmart offers a convenient way to implement classroom
			participation guidance by the Department of English at Fort Hays State University for
			courses conducted at campuses in China.
		</p>
		<p>
			Participation is considered an essential part of student performance and can impact final
			course grades. A student begins the semester at the level of a 'C' letter grade for participation.
			The instructor regularly adjusts the grade throughout the semester, making it visible on Blackboard.
			This is intended to motivate students to make positive contributions during class sessions.  A
			course syllabus should define how the instructor calculates the score, spelling out what behaviors
			are encouraged and discouraged.
		</p>
		<p>
			FHSU policies related to technology use and information security were carefully considered in the
			development of Seatsmart.  Essential features of Seatsmart do not require Internet access.  All data is stored 
			locally on your computer.  This data is intended to remain on your local hard drive and not transfered to any cloud storage system.  This helps ensure that data related to students remains confidential.  Records in Seatsmart relate to students' academic performance and therefore should be protected just as any other student information.
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
</style>
