---
# Leave the homepage title empty to use the site title
title: "Hang Gao"
date: 2024-10-13
type: landing

design:
  # Default section spacing
  spacing: "1rem"

sections:
  - block: resume-biography-3
    content:  
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: |-
          Hang Gao is a student researcher at the School of Artificial Intelligence, Jilin University. 
          His research interests include AI security, vehicle engineering, and mechanical engineering. 
          He built a sand-box platform for testing and evaluating the security of autonomous driving systems. 
          Right now, he is looking for a PhD opportunity in AI security.
          <div style="margin-top: 20px;">
            <a class="btn btn-primary" href="uploads/cv_en.pdf">[The updated CV]</a>
            <a class="btn btn-primary" href="uploads/past_research_github.pdf">[Past Researches]</a>
            <a class="btn btn-primary" href="background/">[Edu Background]</a>
            <a class="btn btn-primary" href="uploads/PhD_Plans.pdf">[PhD Plans]</a>
          </div>
    design:
      # css_class: "bg-primary-700"
      # css_style: "color:#FFFFFF;" # set as black
      card:
        css_class: "bg-primary-700"
        css_style: "background-color: rgba(0, 0, 0, 0.8);"
      spacing:
        padding: [0, 0, 0, 0]
      # background:
      #   color: black
      #   image:
      #     # Add your image background to `assets/media/`.
      #     filename: school-new.svg
      #     filters:
      #       brightness: 1.0
      #     size: cover
      #     position: center
      #     parallax: false
  - block: markdown
    content:
      title: '📚 My Research'
      subtitle: '' 
      text: |-
        <div class='justify-text'>
          My research interests mainly focus on the application of machine learning and deep learning in the field of vehicle engineering. 
          I am also interested in embodied intelligence. 
          ROS (Robot Operating System) and RTOS (Real Time Operating System) are closely related to my past research and I have a solid foundation in these areas.
          I have a knowledge base of rule-based reasoning and knowledge representation in controlling, like classic PID, and modern-control like MPC, Robust control, RL.
          Furthermore, I am also familiar with the design of deep learning models. 
          More interesting things about me can be found in past researches, education background, and future plans.
          Some files may be unavailable yet, please mail to me at herbert_gao@outlook.com if you are interested.
          </div>
    design:
      columns: '1'
      css_class: "justify-text"

  - block: collection
    id: papers
    content:
      title: Recent Publications
      filters:
        folders:
          - publication
        # exclude_featured: false
    design:
      view: citation
  - block: collection
    id: talks
    content:
      title: Recent Talks
      filters:
        folders:
          - event
    design:
      view: article-grid
      columns: 1
  - block: collection
    id: news
    content:
      title: Recent News
      subtitle: ''
      text: ''
      # Page type to display. E.g. post, talk, publication...
      page_type: post
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: date-title-summary
      # Reduce spacing
      spacing:
        padding: [0, 0, 0, 0]
  - block: cta-card
    demo: true # Only display this section in the Hugo Blox Builder demo site
    content:
      title: 👉 Build your own academic website like this
      text: |-
        

        <a class="github-button" href="https://github.com/HugoBlox/hugo-blox-builder" data-color-scheme="no-preference: light; light: light; dark: dark;" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star HugoBlox/hugo-blox-builder on GitHub">Star</a>

        Easily build anything with blocks - no-code required!
        
        From landing pages, second brains, and courses to academic resumés, conferences, and tech blogs.
      button:
        text: Get Started
        url: https://hugoblox.com/templates/
    design:
      card:
        # Card background color (CSS class)
        css_class: "bg-primary-700"
        css_style: ""

  - block: markdown
    content:
      title: "👋 Self Validation"
      subtitle: "This is Hang Gao's homepage, maintained by Hang Gao."
      text: |-
        <div class='justify-text'>
        I prefer to challenge myself. I like trying new things. Security will be the next big thing with AI. I've been learning about it since 2020 and I want to make a difference. 
        I'm self-motivated and I learn quickly. For example, when there are needs for ROS, I learn about it and write a document for others to learn from. 
        I like to learn new things and use them in my research. I like sports and music. Books are good for solving problems. AI can help us searching in the limited time.

        This site has not been fully completed yet. I will update it later.
        </div>
      design:
        css_class: "justify-text"
---
