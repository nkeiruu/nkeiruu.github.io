---
title: 'Home'
date: 2023-10-24
type: landing
#id has to be outside the content subheading e.g. directly under block: and then in menu.yaml written as url: '#events'
sections:
  - block: resume-biography
    content:
      # The user's folder name in content/authors/
      username: admin
    design:
      spacing:
        padding: [0, 0, 0, 0]
      biography:
        style: 'text-align: justify; font-size: 0.8em;'

  - block: collection
    content:
      filters:
        folders:
          - blog
    design:
      spacing:
        padding: ['3rem', 0, '6rem', 0]
        view: card

    
    

  - block: collection
    id: events
    content:
      title: Events
      subtitle: Notes from events, workshops and lectures I have attended
      text: Notes from events, workshops and lectures I have attended
      count: '3'
      filters:
       folders:
        - events   
      
    design:
      view: card
      columns: '3'
      

---
