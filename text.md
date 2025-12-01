git init

// 파일 추가

git add .

git commit -m "<메세지>"

git push

// 파일 추가 .gitignore
// 파일 추가 README.md
// 파일 추가 LICENSE
// 파일 추가 page/index.html

git add .
t commit -m "<메세지>"
git push

<!-- 회원 가입, 로그인 추가 예정-->

git switch -c development

<!-- A 직원-->

git switch development
git swtich -c feat/register

// 파일 추가 register.js, regist.html, register.css

git add .
git commit -m ""
git push <!-- feat/register 브랜치 -->

<!-- B 직원-->

git switch development
git swtich -c feat/login

// 파일 추가 login.js, login.html, login.css

git add .
git commit -m ""
git push <!-- feat/login 브랜치 -->

git switch development
git merge --no-ff feat/register
git merge --no-ff feat/login

git switch -c release
git merge --no-ff development

git switch main
git merge -no-ff release

git tag 1.0.0