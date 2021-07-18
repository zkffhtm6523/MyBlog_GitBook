# Blog

### 1. 원하는 테마 찾기

먼저 처음에 제가 원했던 테마는 포스트를 보기 쉽도록 카테고리가 있어야 했습니다.

그 조건으로 여러가지 찾아보다가 [**jekyll-theme-chirpy**](https://github.com/cotes2020/jekyll-theme-chirpy) 테마를 알게 되었고 써보기로 했습니다. 제가 생각한 이 테마의 장점은 다음과 같습니다.

* 카테고리의 존재
* 지속적인 업데이트
* 꽤나 이쁜 디자인!

### 2. 블로그 생성

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/1.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/1.png?raw=true) |
| :--- |
| $$\color{\#228B22}{\textit{Download ZIP}}$$ |

블로그를 생성하기 위해서, 먼저 소스를 다운로드\(Clone\) 받았습니다.

Fork를 하는 방법도 있지만 여러 커스터마이징을 하기 위해서 이런 방법으로 했습니다.

다만 이런 방식으로 할 때는 꼭 **라이선스\(!!\)** 를 참고하여 진행하도록 합니다. 이 테마는 MIT 라이선스를 가지고 있고 저는 이에 맞춰서 블로그와 저장소의 [**README.md**](https://github.com/estrogenic/estrogenic.github.io/blob/master/README.md) 에 제작자 명시를 하는 방식으로 진행했습니다.

### 3. 세부 설정 변경

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/2-1.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/2-1.png?raw=true) | [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/2-2.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/2-2.png?raw=true) |
| :--- | :--- |
| $$\color{\#228B22}{\textit{\_config.yml}}$$ | $$\color{\#228B22}{\textit{deploy.sh}}$$ |

꼭 넣어야 하는 부분만 진행하겠습니다.

1. 먼저 위와 같이 `_config.yml` 의 `url` 부분에 내 깃허브 페이지 주소를 넣어주세요.
2. `deploy.sh` 의 `PAGES_BRANCH` 를 원하는 이름으로 수정해주세요. 추후 deploy가 진행될 때 이곳에 작성된 이름으로 브랜치가 만들어지고, 그곳에 빌드된 Jekyll 파일들이 저장됩니다.

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/2-3.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/2-3.png?raw=true) | [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/2-4.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/2-4.png?raw=true) |
| :--- | :--- |
| $$\color{\#228B22}{\textit{pages-deploy.yml.hook}}$$ | $$\color{\#228B22}{\textit{pages-deploy.yml.hook &gt; pages-deploy.yml}}$$ |

1. `pages-deploy.yml.hook` 파일의 `branches` 를 소스가 위치할 브랜치 이름으로 수정해주세요. 소스를 읽는데 필요합니다.
2. `pages-deploy.yml.hook` 파일의 확장자 `hook` 을 제거해주세요! 이에 대한 설명은 제작자의 저장소 README.md 를 참고해주세요.

### 4. 로컬에서 돌려보기

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/3-1.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/3-1.png?raw=true) | [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/3-2.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/3-2.png?raw=true) |
| :--- | :--- |
| $$\color{\#228B22}{\textit{run project on localhost - 1}}$$ | $$\color{\#228B22}{\textit{run project on localhost - 2}}$$ |

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/3-3.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/3-3.png?raw=true) | [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/3-4.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/3-4.png?raw=true) |
| :--- | :--- |
| $$\color{\#228B22}{\textit{run project on localhost - 3}}$$ | $$\color{\#228B22}{\textit{local server}}$$ |

로컬에서 프로젝트를 돌려봅니다.나중에 블로그 글을 작성하기 위해서는 로컬에서 먼저 실행을 해보고, GitHub에 업로드 하는 방식으로 진행해야할 것 같습니다.

먼저 로컬로 실행을 하기 위해선 **ruby**를 설치해야 하는데 이에 대한 부분은 건너뜁니다!. 저는 **HomeBrew**를 사용해서 설치하였기에 경로를 직접 지정해서 실행했습니다.

아래 명령어를 순서대로 실행해줍니다. 간혹 webrick 설치가 안되있다고 오류가 떠서 의존성 설정을 추가해줬습니다. =\_=

* /usr/local/Cellar/ruby/3.0.0\_1/bin/bundle add webrick
* /usr/local/Cellar/ruby/3.0.0\_1/bin/bundle install
* /usr/local/Cellar/ruby/3.0.0\_1/bin/bundle exec jekyll serve

### 5. GitHub 에 업로드

#### 5-1. \(선택\) 쓰레기 제거

깃에 올리기에 앞서 잡다한 파일들을 제거해줍니다. `.gitignore` 에 추가해 주셔도 무관합니다.

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/4-1.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/4-1.png?raw=true) | [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/4-2.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/4-2.png?raw=true) |
| :--- | :--- |
| $$\color{\#228B22}{\textit{remove useless files - 1}}$$ | $$\color{\#228B22}{\textit{remove useless files - 2}}$$ |

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/4-3.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/4-3.png?raw=true) |
| :--- |
| $$\color{\#228B22}{\textit{remove useless files - 3}}$$ |

#### 5-2. 업로드

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/5-1.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/5-1.png?raw=true) | [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/5-2.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/5-2.png?raw=true) |
| :--- | :--- |
| $$\color{\#228B22}{\textit{upload to github - 1}}$$ | $$\color{\#228B22}{\textit{upload to github - 2}}$$ |

처음에는 업로드할 파일들이 많아서 IntelliJ 기능으로 업로드 하면 프로그램이 멈추더라고요;; -\_- 그래서 커맨드 명령어로 업로드 해줬습니다. 편하신 대로 업로드 해주시면 됩니다.

#### 5-3 빌드 진행

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/6-1.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/6-1.png?raw=true) | [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/6-2.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/6-2.png?raw=true) |
| :--- | :--- |
| $$\color{\#228B22}{\textit{proceeding build}}$$ | $$\color{\#228B22}{\textit{completed jekyll build}}$$ |

GitHub Page는 선택한 Branch에 Push가 되면 자동으로 빌드가 진행됩니다. 두 번째 사진에서 마스터 브런치에 사이트가 빌드된 것을 볼 수 있는데, 3번 세부설정에서 바꿔준 `PAGES_BRANCH` 를 master 로 해서 그렇습니다.이제 더 많은 커스터마이징을 시도해보세요!😆😆

### 번외. 도메인 설정

| [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/7-1.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/7-1.png?raw=true) | [![](https://github.com/zkffhtm6523/zkffhtm6523.github.io/raw/main/blog-assets/article-1/7-2.png?raw=true)](https://github.com/zkffhtm6523/zkffhtm6523.github.io/blob/main/blog-assets/article-1/7-2.png?raw=true) |
| :--- | :--- |
| $$\color{\#228B22}{\textit{setting in GitHub}}$$ | $$\color{\#228B22}{\textit{setting in domain management page}}$$ |

도메인 설정은 위 사진과 같이 간단하게 GitHub Pages의 Repo Setting 에서 적어준 뒤에, 도메인 관리 사이트에서 연결해주면 됩니다. 적용까지는 시간이 좀 걸리니 기다렸다가 들어가면 연결됩니다.😉

