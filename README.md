<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/inikolaou/pc-setup">
    <img src="images/logo.png" alt="Logo" width="180" height="180">
  </a>

<h3 align="center">Unix PC Setup</h3>

  <p align="center">
    An ansible playbook that creates a reproducable unix environment!
    <br />
    <br />
    <a href="https://github.com/inikolaou/pc-setup/issues">Report Bug</a>
    ·
    <a href="https://github.com/inikolaou/pc-setup/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
This project is about creating a reproducable environment with the help of an ansible playbook and the nix package manager for all unix based operating systems.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* [![Ansible][Ansible.com]][Ansible-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To get started you need to have a pc with a unix operating system. Some tasks in the playbook are specific to ubuntu operating systems. If you are using another operating system you can submit a pull request with the same task modified so it works on your operating system.

### Prerequisites

 All of the commands below were executed on ubuntu 22.04. Execute them based on your specific operating system and using your preffered package manager.
* First update and upgrade your package manager
  ```sh
  sudo apt update && apt upgrade
  ```
* Make sure you have installed git and curl 
  ```sh
  sudo apt install git curl -y
  ```
* Install the [nix package manager](https://nixos.org/download) (multi-user install recommended)
  ```sh
  sh <(curl -L https://nixos.org/nix/install) --daemon
  ```
* Make sure you have installed [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/)
  ```sh
  sudo apt install software-properties-common
  sudo add-apt-repository --yes --update ppa:ansible/ansible
  sudo apt install ansible
  ```

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/inikolaou/pc-setup.git
   ```
2. Install ZSH first
   ```sh
   ansible-playbook pc-setup/run.yml -K --tags "zsh"
   ```
3. Log out of the system and log back in
4. Execute the remaining tasks based on your preferences by using specific [tags](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_tags.html#selecting-or-skipping-tags-when-you-run-a-playbook)
    ```sh
   ansible-playbook pc-setup/run.yml -K --tags "dev-env"
   ```
5. Reboot your system

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the GNU GPL-3.0 License. See `LICENSE` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Project Link: [https://github.com/inikolaou/pc-setup](https://github.com/inikolaou/pc-setup)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Getting Started With Ansible](https://www.youtube.com/watch?v=Z7p9-m4cimg&t=376s&pp=ygULYW5zaWJsZSBwdDE%3D)
* [Nix Package Manager](https://www.youtube.com/watch?v=BwEIXIjLTNs&pp=ygUTbml4IHBhY2thZ2UgbWFuYWdlcg%3D%3D)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/inikolaou/pc-setup.svg?style=for-the-badge
[contributors-url]: https://github.com/inikolaou/pc-setup/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/inikolaou/pc-setup.svg?style=for-the-badge
[forks-url]: https://github.com/inikolaou/pc-setup/network/members
[stars-shield]: https://img.shields.io/github/stars/inikolaou/pc-setup.svg?style=for-the-badge
[stars-url]: https://github.com/inikolaou/pc-setup/stargazers
[issues-shield]: https://img.shields.io/github/issues/inikolaou/pc-setup.svg?style=for-the-badge
[issues-url]: https://github.com/inikolaou/pc-setup/issues
[license-shield]: https://img.shields.io/github/license/inikolaou/pc-setup.svg?style=for-the-badge
[license-url]: https://github.com/inikolaou/pc-setup/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/nikolaou-ioannis
[Ansible.com]: https://img.shields.io/badge/Ansible-123?style=for-the-badge&logo=ansible&logoColor=white
[Ansible-url]: https://www.ansible.com/