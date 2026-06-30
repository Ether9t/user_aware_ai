<script lang="ts">
    import "../app.css";
    import { base } from '$app/paths';

    const team = [
        {
            name: "Karin de Langis",
            avatar: `${base}/members/karin-de-langis.jpg`,
            link: "https://karinjd.github.io/",
        },
        {
            name: "Khanh Chi Le",
            avatar: `${base}/members/khanh-chi-le.jpg`,
            link: "https://chile2706.github.io/",
        },
        {
            name: "Ruizi Wang",
            avatar: `${base}/members/ruizi-wang.jpg`,
            link: "https://ether9t.github.io/",
        },
        {
            name: "Shirley Anugrah Hayati",
            avatar: `${base}/members/shirley-anugrah-hayati.jpg`,
            link: "https://www.shirley.id/",
        },
        {
            name: "Andy J. Phu",
            avatar: `${base}/members/andy-phu.png`,
            link: "https://andyphu.com/",
        },
        {
            name: "Dongyeop Kang",
            avatar: `${base}/members/dongyeop-kang.jpg`,
            link: "https://dykang.github.io/",
        },
    ];
</script>

<svelte:head>
    <title>User-Aware AI</title>
</svelte:head>

<div class="page">
    <header class="nav-wrapper">
        <nav class="nav">
            <div class="logo">USER-AWARE AI</div>

            <div class="links">
                <a href="#overview" class="underline-animate">Overview</a>
                <a href="#data" class="underline-animate">Data</a>
                <a href="#annotation" class="underline-animate">Annotation</a>
                <a href="#recruitment" class="underline-animate">Recruitment</a>
                <a href="#team" class="underline-animate">Team</a>
            </div>

            <button class="ghost-btn">Contact Us</button>
        </nav>
    </header>

    <section id="overview" class="section">
        <div>
            <div class="badge">
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="14"
                    height="14"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="1.75"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="lucide lucide-sparkles size-3"
                    aria-hidden="true"
                >
                    <path
                        d="M11.017 2.814a1 1 0 0 1 1.966 0l1.051 5.558a2 2 0 0 0 1.594 1.594l5.558 1.051a1 1 0 0 1 0 1.966l-5.558 1.051a2 2 0 0 0-1.594 1.594l-1.051 5.558a1 1 0 0 1-1.966 0l-1.051-5.558a2 2 0 0 0-1.594-1.594l-5.558-1.051a1 1 0 0 1 0-1.966l5.558-1.051a2 2 0 0 0 1.594-1.594z"
                    ></path>
                    <path d="M20 2v4"></path><path d="M22 4h-4"></path>
                    <circle cx="4" cy="20" r="2"></circle>
                </svg>Research preview
            </div>

            <h1>User-Aware AI</h1>
            <h3>Overview</h3>
            <p>
                User Workflow Modeling(UWM) asks a different question - not what
                users say they want, but how their goals and decisions unfold
                over time. We investigate computational models of user workflows
                to support the personalized AI agents.
            </p>
            <img
                src={`${base}/user aware figures.png`}
                alt="user aware figures"
                style="width: 1080px; height: auto"
            />
        </div>
        <h4>UWM Framework</h4>
        <p>
            The UWM consists of three primary components: Observer, Memory, and
            Planner. Together, these modules maintain a structured
            representation of user workflows and support personalized assistant
            behavior.
        </p>
        <img
            src={`${base}/roposed major modules.png`}
            alt="roposed major modules"
            style="width: 1080px; height: auto"
        />
    </section>

    <section id="data" class="section">
        <div class="data-layout">
            <div>
                <h3>Data</h3>

                <p>
                    We collected an initial pool of videos from YouTube across
                    two challenging workflow domains. These domains were
                    selected because they involve long-horizon, open-ended
                    activities rather than simple procedural tasks.
                </p>
            </div>

            <div class="domain-grid">
                <div class="domain-card">
                    <span>Case Study 1</span>

                    <h4>Programming</h4>

                    <p>
                        Live problem-solving and programming workflows involving
                        iterative debugging, testing, and reasoning.
                    </p>
                </div>

                <div class="domain-card">
                    <span>Case Study 2</span>

                    <h4>Manual Crafting</h4>

                    <p>
                        Workshop activities involving machine assembly,
                        troubleshooting, repair, and testing.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section id="annotation" class="section">
        <h3>Annotation</h3>
        <h4>Annotation Pipeline</h4>
        <p>
            Videos are first segmented into distinct user actions, then
            processed to generate intent chains. Human annotators subsequently
            review and refine the outputs to ensure annotation quality and
            consistency.
        </p>

        <img
            src={`${base}/casestudy_process.png`}
            alt="casestudy_process"
            style="width: 1080px; height: auto"
        />

        <h4>Annotation Examles</h4>
        <img
            src={`${base}/leetcode_example.png`}
            alt="leetcode_example"
            style="width: 1080px; height: auto"
        />
    </section>

    <section id="recruitment" class="section">
        <h3>Recruitment</h3>

        <div class="wide-card">
            <p>
                We are recruiting participants for data collection and
                annotation studies!
            </p>

            <button class="primary-btn">Apply to Participate</button>
        </div>
    </section>

    <section id="team">
        <h3>Team Member</h3>
        <div class="feature-grid">
            {#each team as member}
                <div class="member-card">
                    <a
                        href={member.link}
                        target="_blank"
                        rel="noopener noreferrer"
                        class="member-link"
                    >
                        <img
                            src={member.avatar}
                            alt={member.name}
                            class="member-avatar"
                        />

                        <span class="underline-animate">
                            {member.name}
                        </span>
                    </a>
                </div>
            {/each}
        </div>
    </section>

    <section id="sponsor">
        <h3>Sponsor</h3>
        <div class="side-card sponsor-card" style="margin-top: 30px;">
            <a
                href="https://research.google/"
                target="_blank"
                rel="noopener noreferrer"
                class="sponsor-link"
            >
                <img
                    src={`${base}/google.png`}
                    alt="Google Research"
                    style="width: 140px; height: auto; display: block;"
                />
            </a>
        </div>
    </section>

    <footer>© 2026 Minnesota NLP Lab</footer>
</div>
