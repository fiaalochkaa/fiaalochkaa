<div id="badges" align ="center">
  <a href= " https://vk.com/fualochka "> 
    <img src = "https://img.shields.io/badge/VK-blue?style=for-the-badge&logo=VK&logoColor=white" alt="VK Badge"/>
  </a>

  <a href= " https://www.google.com/support/accounts/bin/answer.py?answer=181692 ">
    <img src = "https://img.shields.io/badge/EMAIL-red?style=for-the-badge&logo=Gmail&logoColor=white" alt="VK Badge"/>
  </a>
</div>

<div id="viewprof" align="center" >
  <img src="https://komarev.com/ghpvc/?username=fiaalochkaa&style=flat-square&color=blue" alt=""/>
</div>

<div id="heythere" align="center">
<h1> Профиль на GITNUB </h1>
</div>

### :woman_technologist: Обо мне :

- :nerd_face: Учеба

- :woman_cook: Кухня

- :woman_astronaut: Космос

### :hammer_and_wrench: Языки и инструменты :

<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/github/github-original-wordmark.svg" width="40" height="40"/>
  <img src="https://github.com/devicons/devicon/blob/master/icons/ionic/ionic-original-wordmark.svg" width="40" height="40"/>
  <img src="https://github.com/devicons/devicon/blob/master/icons/twitter/twitter-original.svg" width="40" height="40"/>
  <img src="https://github.com/devicons/devicon/blob/master/icons/atom/atom-original-wordmark.svg" width="40" height="40"/>
  <img src="https://github.com/devicons/devicon/blob/master/icons/cucumber/cucumber-plain-wordmark.svg" width="40" height="40"/>
  <img src="https://github.com/devicons/devicon/blob/master/icons/crystal/crystal-line-wordmark.svg" width="40" height="40"/>
</div>

### :trophy: Достижения :

<div>
  <img src="https://github-profile-trophy.versel.app/?username=fiaalochkaa" alt=""/>
  src/Types
</div>

import { ServiceError } from "../Types/index.ts";
import {
  GitHubUserActivity,
  GitHubUserIssue,
  GitHubUserPullRequest,
  GitHubUserRepository,
  UserInfo,
} from "../user_info.ts";

export abstract class GithubRepository {
  abstract requestUserInfo(username: string): Promise<UserInfo | ServiceError>;
  abstract requestUserActivity(
    username: string,
  ): Promise<GitHubUserActivity | ServiceError>;
  abstract requestUserIssue(
    username: string,
  ): Promise<GitHubUserIssue | ServiceError>;
  abstract requestUserPullRequest(
    username: string,
  ): Promise<GitHubUserPullRequest | ServiceError>;
  abstract requestUserRepository(
    username: string,
  ): Promise<GitHubUserRepository | ServiceError>;
}

export class GithubRepositoryService {
  constructor(public repository: GithubRepository) {}
}
