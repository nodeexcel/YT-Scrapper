# YT-Scraping

# Creating a Puppeteer-driven REST API for YouTube scraping with a focus on Test-Driven Development

Scrapes YouTube video data with ID, and returns `title`, `description`, `channel`, `views` and `gameName` (if it's a game video)

## Getting Started

Follow these steps to set up and run a local copy of the project for development and testing.

### Prerequisites

- Installed local [Node.js](https://nodejs.org/) environment
- Package manager to install packages. [Yarn](https://yarnpkg.com/) or [npm](https://www.npmjs.com/)

Clone the repo in your environment

```bash
git clone https://github.com/nodeexcel/YT-Scrapper.git
```

### Installing

```bash
# move into project folder
cd YT-Scrapper

# install the dependencies
yarn install

# rename the .env.sample
mv .env.sample .env

# add your variables
nano .env
```

#### Running the server

```bash
yarn start
```

## Example

```bash
# GET - /{videoId}
curl localhost:3000/h8OX0FNWANM
```

##### Response

```json
{
  "status": true,
  "title": "Recognizing Ignaz Semmelweis and Handwashing",
  "description": "Today’s Doodle follows the official guidelines ...",
  "channel": "GoogleDoodles",
  "views": "56188961"
}
```

## Running the tests

```bash
yarn test
```

## Built With

* [Express](https://github.com/expressjs/express/) - The web framework used
* [Puppeteer](https://github.com/puppeteer/puppeteer) - For web scraping
* [Jest](https://github.com/facebook/jest) - For testing
* [SuperTest](https://github.com/visionmedia/supertest) - For testing HTTP API
