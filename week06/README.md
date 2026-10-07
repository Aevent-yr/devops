- ghcr.io/aevent-yr/guestbook:v2
- Dockerfile 설명
FROM guestbook:v1 // guestbook:v1을 기반 이미지로
ENV APP_TITLE="커스텀" \ // 환경변수 APP TITLE을 "커스텀"으로
THEME_COLOR="#1f1e33" // 환경변수 THEME COLOR를 #1f1e33으로 설정한다
- => CACHED [1/1] FROM docker.io/library/guestbook:v1@sha256:e1e427db10a423a348c70444eff02c2b157cf84b1961adbd834ea754a2fa9b3d
- 설정은 코드 -> ENV -> -e 순서로 덮어씌워지므로, 우선순위를 비교하면 -e > ENV > 코드이다.
