# LinkPage [![Zerodha Tech](https://zerodha.tech/static/images/github-badge.svg)](https://zerodha.tech)

LinkPage is a FOSS self-hosted alternative to link listing websites such as LinkTree and Campsite.bio

## Features

- Self hostable and open source
- Responsive and customizable design
- Admin panel with custom link ordering
- Fetch details (thumbnail, description) directly from the link using OpenGraph tags
- Minimal JavaScript with cached Go templating for the homepage
- Anonymized link click tracking
- Simple sqlite3 setup for getting started instantly
- Basic Auth for admin endpoints

## Demo

### Home

<img src="static/demo.png" height="400" >

### Admin

<img src="static/demo_admin.png" height="400" >

## Get Started

1. Download the latest release
2. Decompress the archive
3. Run the app using `./linkpage --init`, this will generate an empty sqlite database and config file in your local directory.
4. Now you can run the app using `./linkpage`, goto the `/admin` page to add new entries.

## Developer Setup

0. `git clone https://github.com/rhnvrm/linkpage.git`

1. Initialize SQL schema from `schema.sql` by copying the schema using sqlite:

```
sqlite3 app.db

sqlite> (paste and run schema)
```

2. Edit `config.toml`

3. Run the app

`go run main.go`

4. Insert new entries under `/admin` page.
