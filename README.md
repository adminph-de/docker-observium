<!--
*** To avoid retyping too much info. Do a search and replace for the following:
*** Obersium (Community Edition),adminph-de, docker-observium, N00ky2010, patrick.hayo@flsmidth.com
-->

# Obersium (Community Edition)

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<br />
<p align="left">
  <a href="https://github.com/adminph-de/docker-observium">
    <img src="images/logo.png" alt="Code Snipes" width="35%" height="35%">
  </a>
  <p align="left">
    Obersium (Community Edition) Network monitoring with intuition.
    <br />
    <a href="https://github.com/adminph-de/docker-observium/issues">Bug Report</a>
    ·
    <a href="https://github.com/adminph-de/docker-observium/issues">Request Feature</a>
  </p>
</p>


## Content

- Obersium (Community Edition)
  - [Content](#content)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Contributing](#contributing)
  - [License](#license)
  - [Contact](#contact)
  - [Acknowledgements](#acknowledgements)

## Installation

Create the container image out of the ``Dockerfile`` in this Repository

Clone the Repository:
```bash
git clone -b master https://github.com/adminph-de/docker-observium.git 
```
Run the build of the container:
```bash
docker build -t observium:latest .
```

If you don't need or like to change settings in the ``Dockerfile``
you can simply pull the Docker image from my [DockerHub Repository](https://hub.docker.com/r/codesnipes/observium) 
to install Obersium (Community Edition).
```bash
docker pull codesnipes/observium:latest
```
Check the [DockerHub Repository](https://hub.docker.com/r/codesnipes/observium) to see the different tags.

## Usage

After a sucessfull creation or pulling of the image, you can run the container

### Volumes:
You might like to keep the configuration in a docker volume to persist your settings:

- /opt/config/obsobservium
- /opt/config/apache2
- /var/lib/mysql

### Example:
```bash
docker container run --name observium \
    -p 8443:443 \
    -v obs_config:/opt/config/obsobservium \
    -v obs_apache:/opt/config/apache2 \
    -v obs_mysql:/var/lib/mysql \
    observium:latest
```

If the container is running, you can access the Observium Webinterface by:

```html
https://localhost:8443
````

- **User:** Demo
- **Password:** Demo

Find all details at [codesnipes/observium](https://hub.docker.com/r/codesnipes/observium) (DockerHub)


## Contributing
Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. [Fork](https://docs.github.com/en/enterprise/2.13/user/articles/fork-a-repo) the Project
2. Create your Feature Branch `git checkout -b feature/AmazingFeature`
3. Commit your Changes `git commit -m 'Add some AmazingFeature'`
4. Push to the Branch `git push origin feature/AmazingFeature`
5. Open a Pull Request

## License

Distributed under the [MIT](https://choosealicense.com/licenses/mit/) License. See `LICENSE` for more information.


## Contact

Project Link: [https://github.com/adminph-de/docker-observium](https://github.com/adminph-de/docker-observium)

[Patrick Hayo](patrick.hayo@flsmidth.com)

[![N00ky2010](https://img.shields.io/twitter/follow/N00ky2010)](https://www.twitter.com/N00ky2010)



## Acknowledgements

* [Janaina Laguardia Areal Hyldvang, Ph.D.](https://www.linkedin.com/in/janainahyldvang/)
* [Jakob Daugaard](https://www.linkedin.com/in/jakobdaugaard/?locale=en_US)
* [Senthil Kumar Bose](https://www.linkedin.com/in/senthil-kumar-bose-6900582/)
* [Javed Khan](https://www.linkedin.com/in/javed-khan-674863164/)


<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/adminph-de/docker-observium.svg?style=flat-square
[contributors-url]: https://github.com/adminph-de/docker-observium/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/adminph-de/docker-observium.svg?style=flat-square
[forks-url]: https://github.com/adminph-de/docker-observium/network/members
[stars-shield]: https://img.shields.io/github/stars/adminph-de/docker-observium.svg?style=flat-square
[stars-url]: https://github.com/adminph-de/docker-observium/stargazers
[issues-shield]: https://img.shields.io/github/issues/adminph-de/docker-observium.svg?style=flat-square
[issues-url]: https://github.com/adminph-de/docker-observium/issues
[license-shield]: https://img.shields.io/github/license/adminph-de/docker-observium.svg?style=flat-square
[license-url]: https://github.com/adminph-de/docker-observium/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/patrickhayo/?locale=en_US
[gravatar-url]: https://secure.gravatar.com/avatar/7ff4a974bdce7e98ec072b9cb354f64c
[product-screenshot-run]: images/screenshot_run.png
