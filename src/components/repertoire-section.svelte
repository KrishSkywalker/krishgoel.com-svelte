<script>
    let arrayOfTwo = [0,1];
    let arrayOfFour = [0, 1, 2, 3];
    let repertoireCards = [
		{
            title: "Artificial Intelligence", 
            pretext: "I am currently learning to teach the machines to think with <a href='https://www.udemy.com/artificial-intelligence-az'>this Udemy course</a>.",
            completion: 10
        },
        {
            title: "Python", 
            pretext: "Being my first programming language, Python has always been my go-to for competitive programming and quick-dev.",
            completion: 40
        },
        {
            title: "Structural Web Dev", 
            pretext: "Web development being my forte, I am adept at working with web langauges including Pug and Stylus.",
            completion: 100
        },
        {
            title: "IoT and automation", 
            pretext: "I have developed home automation solutions with Alexa and worked with an IT startup that aimed at developing an IoT ecosystem of luxury products.",
            completion: 30
        },
        {
            title: "JavaScript and frameworks", 
            pretext: "I am well versed with JavaScript, JQuery and TypeScript, not much to say here. Though it's worth mentioning, I can work in a myriad of frameworks including Svelte, VueJS and ReactJS",
            completion: 60
        },
        {
            title: "Hardware and robotics",
            pretext: "I can work with Arduinos, TI Launchpads and a myriad of sensors to make basic robots, I acquired most of this know-how while interning in an IoT startup.",
            completion: 30
        },
        {
            title: "Node.JS",
            pretext: "I am fluent in Node.JS and I'm currently learning backend with Node.JS and MongoDB with<a href='https://www.udemy.com/course/complete-back-end-development-with-nodejs-projects/'>this Udemy course</a>.",
            completion: 50
        },
        {
            title: "C++",
            pretext: "I am a real dum dum when it comes to C++ mostly because I have only used it for scripting the hardware and robots that I build.",
            completion: 10
        }
	];
</script>

<section class="repertoire-section">
    <h1 class="mono">📄 My Repertoire</h1>
    
	<!-- Mobile Screen Layout -->
	<div class="small-screen">
        {#each repertoireCards as repertoire, index}
            <div class="card">
                <div class="width-restriction">
                    <h2>{repertoire.title}</h2>
                    <p>{@html repertoire.pretext}</p>
                    <div class="progress-bar-container">
                        <div class="progress-bar blue-green" style="width: {repertoire.completion}%"></div>
                    </div>
                </div>
            </div>
        {/each}
    </div>

    <!-- Mid Screen Layout -->
    <div class="mid-screen">
        <div class="col-container">
            {#each arrayOfTwo as i, index}
                <div class="col-2">
                    {#each repertoireCards as repertoire, index}
                        {#if index%2 == i}
                            <div class="card">
                                <div class="width-restriction">
                                    <h2>{repertoire.title}</h2>
                                    <p>{@html repertoire.pretext}</p>
                                    <div class="progress-bar-container">
                                        <div class="progress-bar blue-green" style="width: {repertoire.completion}%"></div>
                                    </div>
                                </div>
                            </div>
                        {/if}
                    {/each}
                </div>
            {/each}
        </div>
    </div>

    <!-- Large Screen Layout -->
    <div class="large-screen">
        <div class="col-container">
            {#each arrayOfFour as i, index}
                <div class="col-4">
                    {#each repertoireCards as repertoire, index}
                        {#if index%4 == i}
                            <div class="card">
                                <div class="width-restriction">
                                    <h2>{repertoire.title}</h2>
                                    <p>{@html repertoire.pretext}</p>
                                    <div class="progress-bar-container">
                                        <div class="progress-bar blue-green" style="width: {repertoire.completion}%"></div>
                                    </div>
                                </div>
                            </div>
                        {/if}
                    {/each}
                </div>
            {/each}
        </div>
    </div>

</section>