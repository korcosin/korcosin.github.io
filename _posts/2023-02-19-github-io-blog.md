---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_github_io_blog
title: github.io를 이용한 블로그 개설

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
#author: Mr. Green's Workshop
# multiple category is not supported
category: dev
# multiple tag entries are possible
tags: [dev, tip]
# thumbnail image for post
img: ":mock1.jpg"
# disable comments on this page
#comments_disable: true

# publish date
date: 2023-02-19 23:00:00 +0900

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-03-03 12:32:10 +0900
# check the meta_common_description in _data/owner/[language].yml
#meta_description: ""

# optional
# please use the "image_viewer_on" below to enable image viewer for individual pages or posts (_posts/ or [language]/_posts folders).
# image viewer can be enabled or disabled for all posts using the "image_viewer_posts: true" setting in _data/conf/main.yml.
#image_viewer_on: true
# please use the "image_lazy_loader_on" below to enable image lazy loader for individual pages or posts (_posts/ or [language]/_posts folders).
# image lazy loader can be enabled or disabled for all posts using the "image_lazy_loader_posts: true" setting in _data/conf/main.yml.
#image_lazy_loader_on: true
# exclude from on site search
#on_site_search_exclude: true
# exclude from search engines
#search_engine_exclude: true
# to disable this page, simply set published: false or delete this file
#published: false
---

### 서론  
평소에 노션(Notion)을 통해 기록을 하는데,  
기술 블로그를 통해 더 체계적으로 기록하고 공유하고 싶다는 바람이 불어서 개설하게 되었다.  
  
아주 오래전에 티스토리를 이용했다가 거의 10개정도 글 작성하고 포기해버린 사례가 있어서..  
사실 블로그 개설은 매우 고민이 되었었고 이번 github.io에서 작성하는 블로그도 성공하리라는 보장은 없다.  
하지만 나태해지지 않기 위한 나만의 채찍질의 의미로 한번 잘 해나가보려고 한다.  
  
### 사전 준비사항
**1. ruby 설치**  
**2. [github](https://github.com/){:target="_blank"} 계정**  
**3. git에 대한 기본적인 지식**  
  
### github.io 블로그 만들기  
**1. Github > New Repository**  
- korcosin.github.io 와 같이 `본인계정.github.io` 포맷으로 레파지토리를 만든다.
- ReadMe.md 파일만 있는데, 여기에 index.html 페이지를 만든다.
- 브라우저를 통해 해당 URL을 입력하여 접속하면 인덱스 페이지로 접근이 된다.(뭔가 좀 썰렁하지만..)
  
**2. 깃 클론 하여 로컬에 프로젝트 세팅한다**  
- 로컬 터미널에서 본인의 github remote repository를 클론하여 로컬에 세팅한다.
```bash
git clone //github remote repository//
```  
- jekyll 설치한다.
```bash
gem install jekyll bundler
```
- 본인의 로컬환경에 jekyll index.html을 생성한다. (force 옵션을 줘야 overwrite 가능)
```bash
jekyll new ./ --force
```
- 위의 명령에 의해 생성 된 GemFile은 서버를 띄우기 위한 일종의 라이브러리 모음이다. 해당 gemfile을 인스톨하는 명령어를 실행 한다.
```bash
bundle install
```
- 완료가 되면 로컬에서 서버를 실행해본다.
```bash
bundle exec jekyll serve
```
- 터미널에 `Server address: http://127.0.0.1:4000/` 와 같은 메시지가 출력되면 서버실행이 성공한 것이다. 브라우저에서 로컬 어드레스를 실행해보면 jekyll default 테마로 화면이 뜨는 것을 확인 할 수 있을 것이다.  
  

**3.테마만들기**
- 테마 다운로드 URL
  - **[jamstackthemes.dev](https://jamstackthemes.dev/ssg/jekyll/){:target="_blank"}**
  - **[jekyllthemes.org](http://jekyllthemes.org/){:target="_blank"}**
  - **[jekyllthemes.io](https://jekyllthemes.io/){:target="_blank"}**
  - **[jekyll-themes.com](https://jekyll-themes.com/){:target="_blank"}**
- 맘에 드는 테마 github 접근해서 download zip
  - 지금 현재 사용하고 있는 블로그 테마는 **"[MrGreen](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme){:target="_blank"}"** 테마이다.
  - 압축 해제 후, 해당 폴더에 있는 파일들 모두 본인 프로젝트 폴더에 대치한다.
  - 각 테마마다 사용되는 라이브러리가 다르다. 아마 폴더를 대치하면 GemFile또한 많이 바뀌어 있을 것이다 `bundle install` 명령어를 통해 새로 라이브러리를 동기화 한다.
  - `bundle exec jekyll serve` 명령어를 실행 항 후 로컬에서 화면을 확인 했을 때, 데모화면과 동일하게 보여진다면 성공
- 블로그 커스터마이징은 테마를 관리하는 github에서 잘 설명이 되어 있다. 시간이 좀 여유롭다면 각각의 config yml 파일을 까보면서 이것 저것 수정해보는 것도 좋다. (주석으로 설명이 잘 되어 있음)

### 결론
이렇게 해서 블로그를 만들게 되었다.  
잘 운영해봤으면 좋겠는데.. 그리고 지금은 뭔가 체계적으로 관리가 바로 되지는 않겠지만 점점 하면 할 수록 정리정돈의 능력이 많이 올라갔으면 좋겠다.  
