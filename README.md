<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Robert Nester Odhiambo's GitHub Profile</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      background-color: #f0f0f0;
      padding: 20px;
    }
    .container {
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      padding: 20px;
      margin-bottom: 20px;
    }
    h2 {
      text-align: center;
    }
    h3 {
      text-align: center;
      margin-bottom: 10px;
    }
    p {
      text-align: center;
      margin-bottom: 20px;
    }
    ul {
      list-style-type: none;
      padding: 0;
    }
    ul li {
      margin-bottom: 10px;
    }
    ul li a {
      text-decoration: none;
      color: #0366d6;
    }
    ul li a:hover {
      text-decoration: underline;
    }
    .social-links {
      text-align: center;
      margin-top: 20px;
    }
    .social-links a {
      margin: 0 10px;
      font-size: 24px;
      color: #0366d6;
    }
    .github-stats {
      text-align: center;
      margin-top: 20px;
    }
    .github-stats img {
      margin: 10px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Hi there, I'm Robert Nester Odhiambo 👋</h2>
    <p>I'm a passionate developer from Kenya, specializing in web development, data science, and machine learning.</p>
  </div>

  <div class="container">
    <h3>🛠 Skills and Technologies</h3>
    <p>
      <img src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white" />
      <img src="https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
      <img src="https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
      <img src="https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
      <img src="https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" />
      <img src="https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white" />
    </p>
  </div>

  <div class="container">
    <h3>🚀 Projects</h3>
    <ul id="projects-list">
      <!-- Projects will be dynamically added here -->
    </ul>
    <script>
      // Fetching your GitHub repositories using GitHub API
      fetch('https://api.github.com/users/robertnesterodhiambo/repos')
        .then(response => response.json())
        .then(repos => {
          const projectsList = document.getElementById('projects-list');
          repos.slice(0, 3).forEach(repo => {
            const listItem = document.createElement('li');
            const link = document.createElement('a');
            link.href = repo.html_url;
            link.textContent = repo.name;
            listItem.appendChild(link);
            listItem.innerHTML += ` - ${repo.description || 'No description provided.'}`;
            projectsList.appendChild(listItem);
          });
        })
        .catch(error => console.error('Error fetching GitHub repositories:', error));
    </script>
  </div>

  <div class="container">
    <h3>📫 How to reach me</h3>
    <p>
      Email: <a href="mailto:robertnesterodhiambo@gmail.com">robertnesterodhiambo@gmail.com</a><br>
      Twitter: <a href="https://twitter.com/RstudioStat">@RstudioStat</a><br>
      LinkedIn: <a href="https://www.linkedin.com/in/robert-nestar-odhiambo-094422237/">Robert Nestar Odhiambo</a>
    </p>
  </div>

  <div class="container">
    <h3>📊 GitHub Stats</h3>
    <div class="github-stats">
      <a href="#">
        <img height=200 src="https://my-stats-43gk.vercel.app/api?username=robertnesterodhiambo&show_icons=true&theme=radical&hide=contribs,issues&show=discussions_answered&rank_icon=github&include_all_commits=true&card_width=150" />
      </a>
      <a href="#">
        <img height=200 src="https://my-stats-43gk.vercel.app/api/top-langs/?username=robertnesterodhiambo&hide=html,scss,css&langs_count=8&layout=compact&theme=radical&card_width=150" />
      </a>
    </div>
  </div>

  <div class="container">
    <h3>🔗 Social Links</h3>
    <div class="social-links">
      <a href="mailto:robertnesterodhiambo@gmail.com">✉️</a>
      <a href="https://twitter.com/RstudioStat">Twitter</a>
      <a href="https://www.linkedin.com/in/robert-nestar-odhiambo-094422237/">LinkedIn</a>
    </div>
  </div>
</body>
</html>
