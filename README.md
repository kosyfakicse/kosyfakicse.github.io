<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chrysanthi Kosyfaki</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f5f5f5;
        }

        .masthead {
            background-color: #001f3f;
            border-bottom: 1px solid #e0e0e0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }

        .masthead__inner {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .site-nav {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 1rem 0;
        }

        .site-title {
            font-size: 1.5rem;
            font-weight: 600;
            color: #fff;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
            align-items: center;
        }

        .nav-links li {
            margin: 0;
            padding: 0;
        }

        .nav-links a {
            color: #fff;
            text-decoration: none;
            font-size: 0.95rem;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #4da6ff;
        }

        #main {
            max-width: 1280px;
            margin: 2rem auto;
            padding: 0 1rem;
            display: flex;
            gap: 2rem;
        }

        .sidebar {
            flex: 0 0 280px;
            background-color: #fff;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
            height: fit-content;
            position: sticky;
            top: 90px;
        }

        .author__avatar {
            width: 100%;
            border-radius: 50%;
            margin-bottom: 1.5rem;
        }

        .author__name {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            text-align: center;
        }

        .author__bio {
            color: #666;
            font-size: 0.9rem;
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .follow-btn {
            width: 100%;
            padding: 0.75rem;
            background-color: #001f3f;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.95rem;
            margin-bottom: 1rem;
            transition: background-color 0.3s;
        }

        .follow-btn:hover {
            background-color: #003d7a;
        }

        .social-icons {
            list-style: none;
        }

        .social-icons li {
            margin-bottom: 0.75rem;
        }

        .social-icons a {
            color: #555;
            text-decoration: none;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: color 0.3s;
        }

        .social-icons a:hover {
            color: #001f3f;
        }

        .social-icons i {
            width: 20px;
        }

        .page-content {
            flex: 1;
            background-color: #fff;
            padding: 2.5rem;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }

        .page-content p {
            margin-bottom: 1.5rem;
        }

        .page-content a {
            color: #001f3f;
            text-decoration: none;
        }

        .page-content a:hover {
            text-decoration: underline;
        }

        .section-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            font-style: italic;
        }

        .news-section {
            margin-top: 2.5rem;
        }

        .news-section h2 {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            font-style: italic;
        }

        .news-section ul {
            list-style: none;
            padding-left: 0;
        }

        .news-section li {
            padding: 0.75rem 0;
            border-bottom: 1px solid #f0f0f0;
            line-height: 1.7;
        }

        .news-section li:last-child {
            border-bottom: none;
        }

        .news-date {
            font-weight: 600;
            color: #666;
            margin-right: 0.5rem;
        }

        .publication-item {
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid #f0f0f0;
        }

        .publication-title {
            font-weight: 600;
            color: #001f3f;
            margin-bottom: 0.5rem;
        }

        .publication-authors {
            font-style: italic;
            color: #666;
            margin-bottom: 0.3rem;
        }

        .publication-venue {
            color: #555;
        }

        .student-item {
            margin-bottom: 1.5rem;
        }

        .student-name {
            font-weight: 600;
            color: #001f3f;
        }

        .page-footer {
            background-color: #001f3f;
            color: #fff;
            padding: 2rem 1rem;
            margin-top: 3rem;
        }

        .footer-content {
            max-width: 1280px;
            margin: 0 auto;
            text-align: center;
        }

        .footer-links {
            margin-bottom: 1rem;
        }

        .footer-links a {
            color: #fff;
            text-decoration: none;
            margin: 0 1rem;
        }

        .footer-copyright {
            font-size: 0.85rem;
            color: #aaa;
        }

        @media (max-width: 968px) {
            #main {
                flex-direction: column;
            }

            .sidebar {
                position: static;
                flex: 1;
            }

            .nav-links {
                gap: 1rem;
                font-size: 0.85rem;
            }
        }

        @media (max-width: 640px) {
            .nav-links {
                display: none;
            }

            .page-content {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="masthead">
        <div class="masthead__inner">
            <nav class="site-nav">
                <a href="#home" class="site-title">Chrysanthi Kosyfaki</a>
                <ul class="nav-links">
                    <li><a href="#publications">Publications</a></li>
                    <li><a href="#students">Students</a></li>
                    <li><a href="#talks">Talks</a></li>
                    <li><a href="#teaching">Teaching</a></li>
                    <li><a href="#cv">CV</a></li>
                </ul>
            </nav>
        </div>
    </div>

    <div id="main">
        <div class="sidebar">
            <img src="me.jpg" alt="Chrysanthi Kosyfaki" class="author__avatar">
            <h3 class="author__name">Chrysanthi Kosyfaki</h3>
            <p class="author__bio">Postdoctoral Research Fellow at Hong Kong University of Science and Technology</p>
            
            <button class="follow-btn">Follow</button>
            
            <ul class="social-icons">
                <li><a href="mailto:ckosyfaki@cse.ust.hk"><i class="fas fa-envelope"></i> Email</a></li>
                <li><a href="https://scholar.google.com/citations?user=t5qphlwAAAAJ&hl=en"><i class="fas fa-graduation-cap"></i> Google Scholar</a></li>
                <li><a href="https://github.com/kosyfakicse"><i class="fab fa-github"></i> Github</a></li>
                <li><a href="https://www.linkedin.com/in/chrysanthi-kosyfaki-88b84b158/"><i class="fab fa-linkedin"></i> LinkedIn</a></li>
                <li><a href="https://www.researchgate.net/profile/Chrysanthi-Kosyfaki-2?ev=hdr_xprf"><i class="fab fa-researchgate"></i> ResearchGate</a></li>
            </ul>
        </div>

        <article class="page-content" id="home">
            <section>
                <h2 class="section-title">ABOUT ME</h2>
                <p>I am a postdoctoral research fellow in the <a href="https://cse.hkust.edu.hk/">Department of Computer Science and Engineering</a> at Hong Kong University of Science and Technology.</p>
                <p>Previously, I was a postdoctoral research associate at the University of Hong Kong. I obtained my Ph.D. degree from University of Ioannina, Computer Science and Engineering Department, working with Prof. Nikos Mamoulis.</p>
            </section>

            <section class="news-section">
                <h2>RESEARCH INTERESTS</h2>
                <p>My research interests lie in the area of spatiotemporal data management and flow analytics in large graphs, with a particular focus on a new class of networks called Temporal Interaction Networks (TINs). These networks model dynamic systems where entities exchange quantities, such as financial transactions, transportation flows, or communication data.</p>
                <p>Over the past few years, I have been developing efficient solutions to optimize classical problems, such as max-flow computation, by introducing the temporal dimension. Currently, my work focuses on data provenance analytics in large graphs, with an emphasis on designing techniques to trace the origin of transmitted quantities in graph-structured data.</p>
                <p>Recently, I have also started exploring the Text-to-SQL domain, focusing on addressing challenges related to text ambiguity in natural language database queries.</p>
            </section>

            <section class="news-section">
                <h2>RECENT NEWS</h2>
                <ul>
                     <li><span class="news-date">2026-02:</span> Serving as PC member for PVLDB 2027</li>
                    <li><span class="news-date">2026-01:</span> One tutorial accepted to SIGMOD 2026</li>
                    <li><span class="news-date">2025-12:</span> One paper accepted to ICDE 2026</li>
                    <li><span class="news-date">2025-11:</span> I will serve as publicity chair for @MDM 2026</li>
                    <li><span class="news-date">2025-06:</span> One paper accepted to SSTD 2025.</li>
                    <li><span class="news-date">2025-05:</span> Serving as PC member for PVLDB 2026 and ICDE 2026, and as a co-chair for TKDE Poster track @ICDE 2026.</li>
                    <li><span class="news-date">2025-05:</span> Started position as Postdoctoral Research Fellow at HKUST.</li>
                    <li><span class="news-date">2024-06:</span> One paper accepted to PVLDB 2024 - "A Sampling-based Framework for Hypothesis Testing on Large Attributed Graphs".</li>
                    <li><span class="news-date">2023-04:</span> Successfully defended Ph.D. thesis on "Flow Analytics in Large Graphs".</li>
                    <li><span class="news-date">2022-04:</span> Paper accepted to ICDE 2022 - "Provenance in Temporal Interaction Networks".</li>
                </ul>
            </section>

            <section id="publications" class="news-section">
                <h2>SELECTED PUBLICATIONS</h2>
                  <div class="publication-item">
                    <div class="publication-title">BEACON: A Benchmark for Efficient and Accurate Counting of Subgraphs</div>
                    <div class="publication-authors">Xiangju Zhu, Mohammad Matin Najafi, Chrysanthi Kosyfaki, Xiaodong Li, Reynold Cheng, Laks V.S. Lakshmanan</div>
                    <div class="publication-venue"> @ICDE 2026</div>
                </div>

                <div class="publication-item">
                    <div class="publication-title">A Sampling-based Framework for Hypothesis Testing on Large Attributed Graphs</div>
                    <div class="publication-authors">Yun Wang, Chrysanthi Kosyfaki, Sihem Amer-Yahia, Reynold Cheng</div>
                    <div class="publication-venue">PVLDB 2024</div>
                </div>

                <div class="publication-item">
                    <div class="publication-title">Provenance in Temporal Interaction Networks</div>
                    <div class="publication-authors">Chrysanthi Kosyfaki, Nikos Mamoulis</div>
                    <div class="publication-venue">ICDE 2022</div>
                </div>

                <div class="publication-item">
                    <div class="publication-title">Flow Computation in Temporal Interaction Networks</div>
                    <div class="publication-authors">Chrysanthi Kosyfaki, Nikos Mamoulis, Evaggelia Pitoura, Panayiotis Tsaparas</div>
                    <div class="publication-venue">ICDE 2021</div>
                </div>

                <div class="publication-item">
                    <div class="publication-title">Flow Motifs in Interaction Networks</div>
                    <div class="publication-authors">Chrysanthi Kosyfaki, Nikos Mamoulis, Evaggelia Pitoura, Panayiotis Tsaparas</div>
                    <div class="publication-venue">EDBT 2019</div>
                </div>
            </section>

            <section id="talks" class="news-section">
                <h2>INVITED TALKS</h2>
                
                <div class="publication-item">
                    <div class="publication-title">Temporal Provenance in Temporal Interaction Networks</div>
                    <div class="publication-authors">University of Amsterdam, INDE lab</div>
                    <div class="publication-venue">October 2025</div>
                </div>

                <div class="publication-item">
                    <div class="publication-title">Flow Analytics in Large-Scale Networks</div>
                    <div class="publication-authors">Hong Kong University of Science and Technology, CSE Department</div>
                    <div class="publication-venue">November 2024</div>
                </div>
            </section>

            <section id="students" class="news-section">
                <h2>STUDENT SUPERVISION</h2>
                
                <h3 style="margin-top: 1.5rem; margin-bottom: 1rem; color: #001f3f;">PhD Students (HKUST)</h3>
                <div class="student-item">
                    <span class="student-name">Sau Lai YIP</span> - Working on Text-to-SQL problems
                </div>
                <div class="student-item">
                    <span class="student-name">Nujibieke Shabuerjiang</span> - Working on spatiotemporal data management topics
                </div>
                <h3 style="margin-top: 1.5rem; margin-bottom: 1rem; color: #001f3f;">PhD Students (HKU)</h3>
                <div class="student-item">
                    <span class="student-name">Yun (Carrie) Wang</span> - Working on hypothesis testing on graphs
                </div>
                <div class="student-item">
                    <span class="student-name">Xiangju Zhu</span> - Working on subgraph counting problems
                </div>
                <div class="student-item">
                    <span class="student-name">Mohammad Matin Najafi</span> - Worked on subgraph counting problems, now a researcher at Huawei, Hong Kong
                </div>

                <h3 style="margin-top: 1.5rem; margin-bottom: 1rem; color: #001f3f;">Bachelor Students (University of Ioannina)</h3>
                <div class="student-item">
                    <span class="student-name">Ioanna Papayianni (2020)</span> - Thesis: Developing efficient algorithms for analyzing flow patterns in large networks
                </div>
                <div class="student-item">
                    <span class="student-name">Dimitris Zervas (2021)</span> - Thesis: Detecting the origin of transactions in the Bitcoin Network
                </div>
                <div class="student-item">
                    <span class="student-name">Sotiria Kastana (2021)</span> - Thesis: Design and development of a synthetic indoor movement generator
                </div>
                <div class="student-item">
                    <span class="student-name">Vasileios Georgoulas (2023)</span> - Thesis: A web application for passenger movement with public transport
                </div>
            </section>

            <section id="teaching" class="news-section">
                <h2>TEACHING EXPERIENCE</h2>
                 <div class="publication-item">
                    <div class="publication-title">Network Data Analytics</div>
                    <div class="publication-authors">Guest lecturer, The University of Hong Kong</div>
                    <div class="publication-venue">Spring 2026</div>
                </div>

                
                <div class="publication-item">
                    <div class="publication-title">Network Data Analytics</div>
                    <div class="publication-authors">Instructor, The University of Hong Kong</div>
                    <div class="publication-venue">Spring 2025</div>
                </div>

                <div class="publication-item">
                    <div class="publication-title">Complex Data Management</div>
                    <div class="publication-authors">Teaching Assistant, University of Ioannina</div>
                    <div class="publication-venue">Spring 2019-2023</div>
                </div>

                <div class="publication-item">
                    <div class="publication-title">Object Oriented Programming</div>
                    <div class="publication-authors">Teaching Assistant, University of Ioannina</div>
                    <div class="publication-venue">Spring 2018</div>
                </div>

                <div class="publication-item">
                    <div class="publication-title">Introduction to Programming</div>
                    <div class="publication-authors">Teaching Assistant, University of Ioannina</div>
                    <div class="publication-venue">Fall 2017-2022</div>
                </div>
            </section>

            <section id="cv" class="news-section">
                <h2>CURRICULUM VITAE</h2>
                <p><a href="kosyfaki_cv.pdf" download style="font-weight: 600;"><i class="fas fa-download"></i> Download Full CV (PDF)</a></p>
            </section>
        </article>
    </div>

    <div class="page-footer">
        <div class="footer-content">
            <div class="footer-links">
                <a href="#home">Home</a>
                <a href="https://github.com/kosyfakicse"><i class="fab fa-github"></i> GitHub</a>
                <a href="https://kosyfakicse.github.io"><i class="fas fa-globe"></i> Website</a>
            </div>
            <div class="footer-copyright">
                © 2025 Chrysanthi Kosyfaki. Last updated February 2026
            </div>
        </div>
    </div>
</body>
</html>
