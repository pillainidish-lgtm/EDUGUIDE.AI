 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EduGuide.ai | The Ultimate AI Study Architect</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&display=swap');

        :root {
            --primary: #2563eb;
            --primary-dark: #1e3a8a;
            --secondary: #64748b;
            --accent: #f59e0b;
            --bg: #f8fafc;
            --surface: #ffffff;
            --text: #0f172a;
            --gold-gradient: linear-gradient(135deg, #d4af37, #f1d592, #d4af37);
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        /* --- Header & Nav --- */
        .top-bar {
            background: var(--text);
            color: #fff;
            padding: 10px;
            text-align: center;
            font-size: 0.75rem;
            font-weight: 600;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        nav {
            padding: 20px 8%;
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(10px);
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(0,0,0,0.05);
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            text-decoration: none;
            color: var(--text);
        }

        .logo-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.3);
        }

        .brand-name {
            font-size: 1.5rem;
            font-weight: 800;
            letter-spacing: -1px;
        }

        /* --- Hero Section --- */
        .hero {
            padding: 100px 8% 60px;
            text-align: center;
            background: radial-gradient(circle at 50% 0%, #e0e7ff 0%, transparent 50%);
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            letter-spacing: -2.5px;
            line-height: 1.1;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: var(--primary);
        }

        .hero p {
            font-size: 1.25rem;
            color: var(--secondary);
            max-width: 700px;
            margin: 0 auto 40px;
        }

        /* --- The Guarantee Seal --- */
        .seal-container {
            max-width: 850px;
            margin: 0 auto 60px;
            background: white;
            border-radius: 24px;
            padding: 40px;
            border: 1px solid #e2e8f0;
            box-shadow: 0 20px 50px rgba(0,0,0,0.04);
            position: relative;
            overflow: hidden;
        }

        .seal-container::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 4px;
            background: var(--gold-gradient);
        }

        .seal-tag {
            background: #fef3c7;
            color: #92400e;
            padding: 6px 16px;
            border-radius: 100px;
            font-size: 0.8rem;
            font-weight: 700;
            display: inline-block;
            margin-bottom: 15px;
        }

        /* --- Main Tool --- */
        .main-app {
            max-width: 900px;
            margin: 0 auto 100px;
            background: white;
            padding: 40px;
            border-radius: 32px;
            box-shadow: 0 40px 100px rgba(15, 23, 42, 0.1);
        }

        .drop-zone {
            border: 2px dashed #cbd5e1;
            background: #f8fafc;
            border-radius: 20px;
            padding: 80px 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .drop-zone:hover {
            border-color: var(--primary);
            background: #f0f7ff;
            transform: scale(1.01);
        }

        .action-btn {
            width: 100%;
            padding: 22px;
            background: var(--primary);
            color: white;
            border: none;
            border-radius: 16px;
            font-size: 1.25rem;
            font-weight: 700;
            cursor: pointer;
            transition: 0.3s;
            margin-top: 30px;
            box-shadow: 0 10px 20px rgba(37, 99, 235, 0.2);
        }

        .action-btn:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 15px 30px rgba(37, 99, 235, 0.3);
        }

        /* --- Capabilities Grid --- */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            padding: 0 8% 100px;
        }

        .feature-card {
            background: white;
            padding: 30px;
            border-radius: 20px;
            border: 1px solid #f1f5f9;
            transition: 0.3s;
        }

        .feature-card:hover { transform: translateY(-5px); border-color: var(--primary); }

        .feature-card i { font-size: 2rem; color: var(--primary); margin-bottom: 20px; }

        /* --- Founder Section --- */
        .founder-section {
            background: #0f172a;
            color: white;
            padding: 100px 8%;
            display: flex;
            justify-content: center;
        }

        .founder-card {
            background: white;
            color: var(--text);
            max-width: 650px;
            padding: 60px;
            border-radius: 40px;
            text-align: center;
            position: relative;
        }

        .founder-img {
            width: 120px;
            height: 120px;
            background: var(--primary);
            border-radius: 50%;
            margin: -120px auto 30px;
            border: 8px solid #0f172a;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .signature {
            font-family: 'Brush Script MT', cursive;
            font-size: 2.5rem;
            color: var(--primary);
            margin-top: 30px;
        }

        footer {
            padding: 60px 8%;
            text-align: center;
            color: var(--secondary);
            font-size: 0.9rem;
        }

        #file-input { display: none; }
    </style>
</head>
<body>

    <div class="top-bar">Now Optimized with GPT-4o Study Architect Intelligence</div>

    <nav>
        <a href="#" class="logo">
            <div class="logo-icon"><i class="fa-solid fa-bolt"></i></div>
            <span class="brand-name">EduGuide.ai</span>
        </a>
        <div style="font-size: 0.8rem; font-weight: 700; color: var(--secondary);">V. 2.04 PROFESSIONAL</div>
    </nav>

    <header class="hero">
        <h1>Engineering Academic <span>Victory.</span></h1>
        <p>Turn static documents into high-retention study assets. Built for medical, law, and engineering professionals.</p>

        <div class="seal-container">
            <div class="seal-tag"><i class="fa-solid fa-circle-check"></i> QUALITY ASSURANCE</div>
            <h2 style="font-size: 2rem; margin: 10px 0;">The 1,000 Marks Guarantee</h2>
            <p style="color: var(--secondary); margin: 0 auto; max-width: 600px;">
                Nidish Pillai’s proprietary AI architecture is specifically tuned to maximize cognitive recall. We guarantee that active use of our generated materials provides a direct path to a 1,000-mark profile.
            </p>
        </div>
    </header>

    <section class="main-app">
        <div class="drop-zone" onclick="document.getElementById('file-input').click()">
            <i class="fa-solid fa-cloud-arrow-up" style="font-size: 3rem; color: var(--primary); margin-bottom: 20px;"></i>
            <h3 style="margin: 0;">Upload Research & Assets</h3>
            <p style="color: var(--secondary);">Drag & Drop PDF, JPG, or PNG</p>
            <input type="file" id="file-input" multiple accept=".pdf, .jpg, .jpeg, .png">
            <div id="file-status" style="margin-top: 15px; color: var(--primary); font-weight: 700;"></div>
        </div>

        <button class="action-btn" onclick="startAI()">
            Generate Study Infrastructure
        </button>
    </section>

    <section class="features-grid">
        <div class="feature-card">
            <i class="fa-solid fa-microchip"></i>
            <h3>Neural OCR</h3>
            <p>Advanced recognition for complex handwritten notes and diagrams.</p>
        </div>
        <div class="feature-card">
            <i class="fa-solid fa-brain"></i>
            <h3>Active Recall</h3>
            <p>AI designed to force cognitive engagement, not just passive reading.</p>
        </div>
        <div class="feature-card">
            <i class="fa-solid fa-shield-halved"></i>
            <h3>Data Integrity</h3>
            <p>Your research is encrypted. We value academic privacy above all.</p>
        </div>
    </section>

    <section class="founder-section">
        <div class="founder-card">
            <div class="founder-img"><i class="fa-solid fa-user-tie"></i></div>
            <h2 style="font-size: 2rem; margin-bottom: 10px;">A Note from the Founder</h2>
            <div style="font-weight: 700; color: var(--primary); margin-bottom: 30px; letter-spacing: 1px;">NIDISH PILLAI</div>
            <p style="color: var(--secondary); font-style: italic;">
                "I engineered EduGuide.ai to solve a fundamental problem: the gap between reading and mastering. My AI system is designed to act as your digital study architect, building the framework you need to hit peak performance. Welcome to the future of education."
            </p>
            <div class="signature">Nidish Pillai</div>
        </div>
    </section>

    <footer>
        <p>© 2026 EduGuide Intelligence Inc. | Engineered by <strong>Nidish Pillai</strong></p>
    </footer>

    <script>
        const fileInput = document.getElementById('file-input');
        const status = document.getElementById('file-status');

        fileInput.onchange = () => {
            if(fileInput.files.length > 0) {
                status.innerHTML = `✅ ${fileInput.files.length} Secure Asset(s) Synchronized.`;
            }
        };

        function startAI() {
            if (fileInput.files.length === 0) {
                alert("Please provide a document to begin the architecture process.");
                return;
            }
            alert("Success: Nidish Pillai's AI has been deployed. Analyzing your assets...");
        }
    </script>
</body>
</html>
