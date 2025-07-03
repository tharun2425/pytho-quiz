<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Pages 404 Solution</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto+Mono:wght@400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #24292e;
            --secondary: #0366d6;
            --accent: #28a745;
            --light: #f6f8fa;
            --dark: #1b1f23;
            --danger: #d73a49;
            --warning: #ffd33d;
            --gray: #6a737d;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0d1117, #161b22);
            color: #c9d1d9;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .container {
            max-width: 1000px;
            width: 100%;
            background: rgba(22, 27, 34, 0.9);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid #30363d;
        }
        
        header {
            background: var(--primary);
            padding: 30px;
            text-align: center;
            border-bottom: 1px solid #30363d;
        }
        
        header h1 {
            font-size: 2.5rem;
            color: white;
            margin-bottom: 15px;
        }
        
        header p {
            font-size: 1.2rem;
            color: #8b949e;
            max-width: 700px;
            margin: 0 auto;
        }
        
        .error-code {
            font-family: 'Roboto Mono', monospace;
            background: var(--dark);
            color: var(--danger);
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 1.4rem;
            display: inline-block;
            margin: 20px 0;
        }
        
        .content {
            display: flex;
            padding: 0;
        }
        
        .diagnosis {
            flex: 1;
            padding: 30px;
            border-right: 1px solid #30363d;
        }
        
        .solution {
            flex: 1;
            padding: 30px;
            background: rgba(13, 17, 23, 0.5);
        }
        
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 25px;
            color: white;
            display: flex;
            align-items: center;
        }
        
        .section-title i {
            margin-right: 15px;
            font-size: 1.5rem;
        }
        
        .problem-list {
            list-style: none;
            margin-bottom: 30px;
        }
        
        .problem-item {
            padding: 15px;
            background: rgba(48, 54, 61, 0.3);
            margin-bottom: 15px;
            border-radius: 6px;
            border-left: 4px solid var(--danger);
            transition: all 0.3s;
        }
        
        .problem-item:hover {
            background: rgba(48, 54, 61, 0.5);
            transform: translateX(5px);
        }
        
        .solution-steps {
            counter-reset: step-counter;
            list-style: none;
        }
        
        .solution-step {
            margin-bottom: 25px;
            position: relative;
            padding-left: 50px;
        }
        
        .solution-step:before {
            counter-increment: step-counter;
            content: counter(step-counter);
            position: absolute;
            left: 0;
            top: 0;
            width: 36px;
            height: 36px;
            background: var(--secondary);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-family: 'Roboto Mono', monospace;
        }
        
        .code-block {
            background: #0d1117;
            border: 1px solid #30363d;
            border-radius: 6px;
            padding: 15px;
            margin: 15px 0;
            font-family: 'Roboto Mono', monospace;
            font-size: 0.9rem;
            overflow-x: auto;
        }
        
        .terminal {
            color: var(--accent);
        }
        
        .command {
            color: var(--warning);
        }
        
        .comment {
            color: var(--gray);
        }
        
        .success-badge {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 5px 10px;
            border-radius: 4px;
            font-size: 0.9rem;
            margin-top: 10px;
        }
        
        footer {
            text-align: center;
            padding: 30px;
            background: var(--primary);
            border-top: 1px solid #30363d;
            font-size: 0.9rem;
            color: #8b949e;
        }
        
        .github-link {
            color: var(--secondary);
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            margin-top: 10px;
        }
        
        .github-link:hover {
            text-decoration: underline;
        }
        
        @media (max-width: 768px) {
            .content {
                flex-direction: column;
            }
            
            .diagnosis, .solution {
                border-right: none;
                border-bottom: 1px solid #30363d;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>GitHub Pages 404 Error</h1>
            <p>The site configured at this address does not contain the requested file</p>
            <div class="error-code">404: File Not Found</div>
        </header>
        
        <div class="content">
            <div class="diagnosis">
                <h2 class="section-title">Common Causes</h2>
                <ul class="problem-list">
                    <li class="problem-item">
                        <strong>Missing index.html</strong> - Your repository doesn't have an index.html file in the root or selected folder
                    </li>
                    <li class="problem-item">
                        <strong>Branch misconfiguration</strong> - GitHub Pages is not set to the correct branch (gh-pages or main)
                    </li>
                    <li class="problem-item">
                        <strong>Case sensitivity issues</strong> - Filename case doesn't match the URL (GitHub is case-sensitive)
                    </li>
                    <li class="problem-item">
                        <strong>Build errors</strong> - Jekyll build failed due to errors in your configuration
                    </li>
                    <li class="problem-item">
                        <strong>Incorrect folder structure</strong> - Files are not in the root of the repository or selected docs folder
                    </li>
                </ul>
            </div>
            
            <div class="solution">
                <h2 class="section-title">Step-by-Step Solution</h2>
                <ol class="solution-steps">
                    <li class="solution-step">
                        <h3>Create index.html in root folder</h3>
                        <p>Your repository must have an index.html file at the root:</p>
                        <div class="code-block">
                            <span class="terminal">~/repository/</span><br>
                            ├── <span style="color: var(--accent);">index.html</span><br>
                            ├── styles.css<br>
                            └── script.js
                        </div>
                    </li>
                    
                    <li class="solution-step">
                        <h3>Configure GitHub Pages</h3>
                        <p>In your repository Settings → Pages:</p>
                        <div class="code-block">
                            Source: <span class="command">Branch: main</span><br>
                            Folder: <span class="command">/(root)</span> or <span class="command">/docs</span>
                        </div>
                    </li>
                    
                    <li class="solution-step">
                        <h3>Check file naming</h3>
                        <p>Ensure filenames match exactly (case-sensitive):</p>
                        <div class="code-block">
                            <span class="comment"># Incorrect:</span><br>
                            https://user.github.io/repo/MyFile.html<br><br>
                            
                            <span class="comment"># Correct:</span><br>
                            https://user.github.io/repo/myfile.html
                        </div>
                    </li>
                    
                    <li class="solution-step">
                        <h3>Verify Jekyll settings</h3>
                        <p>Add a .nojekyll file to disable Jekyll processing:</p>
                        <div class="code-block">
                            <span class="terminal">~/repository/</span><br>
                            touch .nojekyll
                        </div>
                    </li>
                    
                    <li class="solution-step">
                        <h3>Check deployment status</h3>
                        <p>Go to Actions tab to see build status:</p>
                        <div class="code-block">
                            <span class="terminal">Repository → Actions</span><br>
                            View latest GitHub Pages deployment
                        </div>
                        <div class="success-badge">Deployment should show green checkmark</div>
                    </li>
                </ol>
            </div>
        </div>
        
        <footer>
            <p>GitHub Pages Documentation • Status: <span style="color: var(--accent);">Operational</span></p>
            <a href="https://docs.github.com/en/pages" class="github-link" target="_blank">
                View GitHub Pages Documentation
            </a>
        </footer>
    </div>
</body>
</html>
