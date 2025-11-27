# Udemy Search Scraper
> This tool collects detailed course information directly from Udemy’s course pages, giving you structured and reliable data for research, cataloging, or content strategy. It focuses on accuracy, clean formatting, and handling large batches of URLs with ease.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/za2122/footer-section/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>udemy-search-scraper</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
The Udemy Search Scraper takes one or many Udemy course URLs and turns them into structured JSON. It solves the usual headache of digging through course pages manually and helps anyone needing consistent course metadata. Researchers, developers, analysts, and content teams can all use it without friction.

### Why This Scraper Matters
- Grabs high-value course details in a consistent structure.
- Handles multiple URLs efficiently in a single run.
- Maintains stable scraping even with dynamic pages.
- Outputs clean JSON ready for downstream tools or dashboards.
- Reduces manual collection time dramatically.

## Features
| Feature | Description |
|----------|-------------|
| Comprehensive Course Data | Captures title, instructors, ratings, outcomes, duration, images, and more. |
| Multi-URL Processing | Accepts and processes multiple course pages at once. |
| Structured JSON Output | Delivers clean, predictable fields suitable for databases or analytics. |
| Optional Proxy Support | Allows proxy configuration for smoother scraping. |
| Error Handling | Manages failures, retries, and timeouts gracefully. |

---
## What Data This Scraper Extracts
| Field Name | Field Description |
|-------------|------------------|
| id | Unique course identifier. |
| title | Full course title as displayed on Udemy. |
| headline | Short course description or tagline. |
| instructors | List of instructor names. |
| rating | Average course rating value. |
| rating_count | Number of ratings provided by students. |
| is_free | Indicates if the course is free or paid. |
| level | Difficulty or level category of the course. |
| duration_in_seconds | Total video length in seconds. |
| lectures_count | Number of lectures in the course. |
| learning_outcomes | Array of what the learner will gain from the course. |
| updated_on | Last update date for the course. |
| locale | Language/locale of the course. |
| images | Collection of available course image URLs. |
| url_course_landing | Direct link to the course landing page. |
| url_auto_enroll | Auto-enroll URL for the course. |
| search_query | Query term used during discovery. |

---
## Example Output
Example:
    [
        {
            "id": "1529012",
            "title": "Social Media Content Creation: Canva Beginner to Advanced",
            "headline": "Using Canva you'll learn to design incredible graphics, videos, and more for use in your social media marketing in 2025!",
            "instructors": ["Maggie Stara"],
            "rating": 4.654065132141113,
            "rating_count": 5838,
            "is_free": false,
            "level": "ALL_LEVELS",
            "duration_in_seconds": 47811,
            "lectures_count": 96,
            "learning_outcomes": [
                "Create eye-catching designs for Instagram, Facebook, Pinterest, YouTube and LinkedIn that will help you get noticed online",
                "Save time and money by designing your own (mobile-friendly) graphics using Canva and other online tools",
                "Learn advanced skills like creating moving GIFs, videos and professional eBooks",
                "Create beautiful Canva templates that you can share with your audience or sell online",
                "Design captivating videos for organic posts or paid video ads"
            ],
            "updated_on": "2025-06-09",
            "locale": "en-US",
            "images": {
                "height125": "https://img-c.udemycdn.com/course/125_H/1529012_6f0f_16.jpg",
                "px100x100": "https://img-c.udemycdn.com/course/100x100/1529012_6f0f_16.jpg",
                "px240x135": "https://img-c.udemycdn.com/course/240x135/1529012_6f0f_16.jpg",
                "px304x171": "https://img-c.udemycdn.com/course/304x171/1529012_6f0f_16.jpg",
                "px480x270": "https://img-c.udemycdn.com/course/480x270/1529012_6f0f_16.jpg",
                "px50x50": "https://img-c.udemycdn.com/course/50x50/1529012_6f0f_16.jpg"
            },
            "url_course_landing": "https://www.udemy.com/course/design-school-create-social-media-graphics",
            "url_auto_enroll": "https://www.udemy.com/course/design-school-create-social-media-graphics/enroll",
            "search_query": "content marketing"
        }
    ]

---
## Directory Structure Tree
    udemy-search-scraper-scraper/
    ├── src/
    │   ├── main.py
    │   ├── parser/
    │   │   ├── udemy_parser.py
    │   │   └── helpers.py
    │   ├── network/
    │   │   ├── requester.py
    │   │   └── proxy_manager.py
    │   ├── output/
    │   │   └── writer.py
    │   └── config/
    │       └── input.example.json
    ├── data/
    │   ├── sample_output.json
    │   └── urls.txt
    ├── docs/
    │   └── README.md
    ├── tests/
    │   └── test_parser.py
    ├── requirements.txt
    ├── LICENSE
    └── README.md

---
## Use Cases
- **Researchers** gather structured course data to study educational trends and learner behavior.
- **Platform builders** collect course metadata to populate catalogs and search systems automatically.
- **Marketing teams** analyze ratings, outcomes, and instructors to shape content strategies.
- **Developers** integrate real course data into dashboards, automation flows, or analytics pipelines.

---
## FAQs
**How many URLs can I process at once?**
You can supply a single URL or a long list. The scraper processes each independently and merges the output into one JSON array.

**Does the scraper require proxies?**
Proxies are optional but helpful when running large batches, as they keep requests stable and reduce the chance of throttling.

**What format is the output saved in?**
All results are delivered as structured JSON, ensuring easy import into databases or Python workflows.

**What happens if a page fails to load?**
The scraper retries the request and gracefully handles unexpected responses so the run can continue without interruption.

---
## Performance Benchmarks and Results
- **Primary Metric:** Capable of processing dozens of course pages per minute with consistent response parsing.
- **Reliability Metric:** Maintains a high success rate across large URL batches thanks to resilient request handling.
- **Efficiency Metric:** Lightweight execution minimizes resource usage while keeping throughput stable.
- **Quality Metric:** Produces near-complete field coverage for each course, ensuring dependable data for analysis.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtube.com/shorts/6AwB5omXrIM" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review3.gif" alt="Review 3" width="35%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Exceptional results, clear communication, and flawless delivery. Bitbash nailed it.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
