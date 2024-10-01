# Отчет по лабораторной №1

1.OPTION

1.1.

@HostAddress_mail = https://mail.ru

OPTIONS  {{HostAddress_mail}} HTTP/1.1
```
Ответ:
HTTP/1.1 400  
Server: nginx/1.26.2
Date: Tue, 01 Oct 2024 17:23:06 GMT
Content-Type: text/html
Transfer-Encoding: chunked
Connection: keep-alive
X-XSS-Protection: 1; mode=block; report=https://cspreport.mail.ru/xxssprotection
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
X-Host: lf258.m.smailru.net
X-ETime: 0.001
Content-Security-Policy: base-uri 'self'; default-src 'none'; form-action

400 - HTTP-ответ с кодом состояния 400 (Bad Request) указывает на то, что сервер не может или не будет обрабатывать запрос из-за того, что он содержит неверный синтаксис.
```
1.2.
OPTIONS  https://ya.ru HTTP/1.1
```
Ответ:
HTTP/1.1 200 Ok
Accept-CH: Sec-CH-UA-Platform-Version, Sec-CH-UA-Mobile, Sec-CH-UA-Model, Sec-CH-UA, Sec-CH-UA-Full-Version-List, Sec-CH-UA-WoW64, Sec-CH-UA-Arch, Sec-CH-UA-Bitness, Sec-CH-UA-Platform, Sec-CH-UA-Full-Version, Viewport-Width, DPR, Device-Memory, RTT, Downlink, ECT, Width
Cache-Control: no-cache,no-store,max-age=0,must-revalidate
Content-Encoding: gzip
Content-Security-Policy: script-src 'unsafe-inline' 

200 - HTTP-ответ с кодом состояния 200 (OK) указывает на то, что запрос был успешно обработан сервером.

Но методы доступа не реализованы
```
1.3.
OPTIONS  https://vk.ru HTTP/1.1
```
Ответ:
HTTP/1.1 418 
Server: kittenx
Date: Tue, 01 Oct 2024 17:26:50 GMT
Content-Length: 0
Connection: keep-alive
X-Frontend: front661202
Access-Control-Expose-Headers: X-Frontend
X-Trace-Id: r1JqLIsEUg3gWFJ9lDz9Ui1zBqptVQ
Server-Timing: tid;desc="r1JqLIsEUg3gWFJ9lDz9Ui1zBqptVQ"

418 - HTTP-ответ с кодом состояния 418 (I'm a teapot) является шутливым кодом, который был определен в спецификации RFC 2324, известной как "April Fools' Day RFC". Сервер, представляющий собой чайник, отказывается заваривать чай, если к нему поступает запрос на это.
```
2.HEAD

2.1.
HEAD  https://vk.com HTTP/1.1
```
Ответ:
HTTP/1.1 418 
Server: kittenx
Date: Tue, 01 Oct 2024 17:30:59 GMT
Content-Length: 0
Connection: keep-alive
X-Frontend: front656600
Access-Control-Expose-Headers: X-Frontend
X-Trace-Id: a21R2BX_pN9GV7EGkMqiVHaIptoAwA
Server-Timing: tid;desc="a21R2BX_pN9GV7EGkMqiVHaIptoAwA",front;dur=0.134
```
2.2.
HEAD  https://apple.com HTTP/1.1
```
Ответ:
HTTP/1.1 200 OK
Server: Apple
Content-Type: text/html; charset=utf-8
Content-Length: 39748
X-Frame-Options: SAMEORIGIN
X-Xss-Protection: 1; mode=block
Accept-Ranges: bytes
Content-Encoding: gzip
X-Content-Type-Options: nosniff
Strict-Transport-Security: max-age=31536000; includeSubdomains; preload
Referrer-Policy: no-referrer-when-downgrade
Content-Security-Policy: default-src 'self' blob: data: *.akamaized.net *.apple.com *.apple-mapkit.com *.cdn-apple.com *.organicfruitapps.com; child-src blob: mailto: embed.music.apple.com embed.podcasts.apple.com https://recyclingprogram.apple.com swdlp.apple.com www.apple.com www.instagram.com platform.twitter.com www.youtube-nocookie.com; img-src 'unsafe-inline' blob: data: *.apple.com *.apple-mapkit.com *.cdn-apple.com *.mzstatic.com; script-src 'unsafe-inline' 'unsafe-eval' blob: *.apple.com *.apple-mapkit.com www.instagram.com platform.twitter.com; style-src 'unsafe-inline' *.apple.com
Cache-Control: max-age=368
Expires: Tue, 01 Oct 2024 17:38:31 GMT
Date: Tue, 01 Oct 2024 17:32:23 GMT
X-Cache: TCP_MEM_HIT from a104-94-100-167.deploy.akamaitechnologies.com (AkamaiGHost/11.6.4-e26983a004e229b4ffa935b6e3b2fe8f) (-)
Connection: keep-alive
Vary: Accept-Encoding
```
2.3.
HEAD  https://msn.com HTTP/1.1
```
Ответ:
HTTP/1.1 404 Not Found
Cache-Control: no-store, no-cache
Pragma: no-cache
Content-Length: 0
Set-Cookie: _C_ETH=1; domain=.msn.com; path=/; secure; httponly,_C_Auth=,_EDGE_S=F=1&SID=2ADF5D7265056AA0255C487964726BD7; domain=.msn.com; path=/; httponly
X-Ceto-Origin-ForwardOnError: https://staticview.msn.com
x-fabric-cluster: pmeprodneu
nel: {"report_to":"network-errors","max_age":604800,"success_fraction":0.001,"failure_fraction":0.5}
report-to: {"group":"network-errors","max_age":604800,"endpoints":[{"url":"https://deff.nelreports.net/api/report?cat=msn"}]},{"group":"csp-endpoint","max_age":86400,"endpoints":[{"url":"https://deff.nelreports.net/api/report"}]}
Strict-Transport-Security: max-age=1209600; includeSubDomains; preload
X-Ceto-ref: 66fc32668f3a47a590e8d81a2afd0193|AFD:12395C4E0EC449B29DDBE8EC31FD9427|2024-10-01T17:33:26.842Z
X-Cache: CONFIG_NOCACHE
Accept-CH: Sec-CH-UA-Arch, Sec-CH-UA-Bitness, Sec-CH-UA-Full-Version, Sec-CH-UA-Full-Version-List, Sec-CH-UA-Mobile, Sec-CH-UA-Model, Sec-CH-UA-Platform, Sec-CH-UA-Platform-Version
X-MSEdge-Ref: Ref A: 12395C4E0EC449B29DDBE8EC31FD9427 Ref B: FRAEDGE1313 Ref C: 2024-10-01T17:33:26Z
Date: Tue, 01 Oct 2024 17:33:26 GMT

404 - HTTP-ответ с кодом состояния 404 (Not Found) указывает на то, что сервер не может найти запрашиваемый ресурс. 
```
3.GET, POST

3.1.
GET  https://yandex.ru HTTP/1.1
```
Ответ:
HTTP/1.1 200 Ok
Access-Control-Allow-Origin: yastatic.net
Content-Length: 24107
Content-Type: text/html
Set-Cookie: _yasc=i4/VuiKnl1ytOWxQ/ipxtkUToXPQL6bU6ykT5eoJFkvwB5xbw02Ibcyt+6VR1E74nlrD; domain=.dzen.ru; path=/; expires=Fri, 29 Sep 2034 17:36:48 GMT; secure
X-Yandex-Captcha: captcha
X-Yandex-EU-Request: 0

<!doctype html>
```
3.2.
GET  https://google.com HTTP/1.1
```
Ответ:
HTTP/1.1 200 OK
Date: Tue, 01 Oct 2024 17:37:58 GMT
Expires: -1
Cache-Control: private, max-age=0
Content-Type: text/html; charset=ISO-8859-1
Content-Security-Policy-Report-Only: object-src 'none';base-uri 'self';script-src 'nonce-P2bvGaTBBthO81NAWObUhQ' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp
Accept-CH: Sec-CH-Prefers-Color-Scheme
P3P: CP="This is not a P3P policy! See g.co/p3phelp for more info."
Content-Encoding: gzip
Server: gws
X-XSS-Protection: 0
X-Frame-Options: SAMEORIGIN
Set-Cookie: AEC=AVYB7cqqqLAAFiGOCjGRhF1uMyDDYFhTNsepNE2PMFxaTjUe3LE1OAzjEw; expires=Sun, 30-Mar-2025 17:37:58 GMT; path=/; domain=.google.com; Secure; HttpOnly; SameSite=lax,NID=518=F9KwL1i5ZDzj4Z1Lv1HjyFmdXPsqbINZzj5b0SooQ3_radZp12BWd67z6Hjxs_Fs9Cqs0cdUCHQigeQez2S-t0BsvxKnjFj20U_y8EDU-MnTq3BEPntlylB9ALH0AQ4NE4by6YQ4Dfqkp8AY4iiENT-1rTeehguaS3LHMXPzkHc93Yzy_OkKZTfITW_zYqnAGSXM; expires=Wed, 02-Apr-2025 17:37:58 GMT; path=/; domain=.google.com; HttpOnly
Alt-Svc: h3=":443"; ma=2592000,h3-29=":443"; ma=2592000
Transfer-Encoding: chunked

<!doctype html>
```
3.3.
GET  https://apple.com HTTP/1.1
```
Ответ:
HTTP/1.1 200 OK
Server: Apple
Content-Type: text/html; charset=utf-8
X-Frame-Options: SAMEORIGIN
Vary: Accept-Encoding
Content-Security-Policy: default-src 'self' blob: data: *.akamaized.net *.apple.com *.apple-mapkit.com *.cdn-apple.com *.organicfruitapps.com; child-src blob: mailto: embed.music.apple.com embed.podcasts.apple.com https://recyclingprogram.apple.com swdlp.apple.com www.apple.com www.instagram.com platform.twitter.com www.youtube-nocookie.com; img-src 'unsafe-inline' blob: data: *.apple.com *.apple-mapkit.com *.cdn-apple.com *.mzstatic.com; script-src 'unsafe-inline' 'unsafe-eval' blob: *.apple.com *.apple-mapkit.com www.instagram.com platform.twitter.com; style-src 'unsafe-inline' *.apple.com
Referrer-Policy: no-referrer-when-downgrade
Strict-Transport-Security: max-age=31536000; includeSubdomains; preload
X-Content-Type-Options: nosniff
X-Xss-Protection: 1; mode=block
Content-Encoding: gzip
Cache-Control: max-age=212
Expires: Tue, 01 Oct 2024 17:42:00 GMT
Date: Tue, 01 Oct 2024 17:38:28 GMT
Content-Length: 39664
X-Cache: TCP_HIT from a104-94-100-159.deploy.akamaitechnologies.com (AkamaiGHost/11.6.4-e26983a004e229b4ffa935b6e3b2fe8f) (-)
Connection: keep-alive
```
3.4.
POST  https://yandex.ru HTTP/1.1

Content-Type: application/json

{
  "title": "foo",
  "body": "bar",
  "userId": 1
}
```
Ответ:
HTTP/1.1 302 Moved temporarily
Accept-CH: Sec-CH-UA-Platform-Version, Sec-CH-UA-Mobile, Sec-CH-UA-Model, Sec-CH-UA, Sec-CH-UA-Full-Version-List, Sec-CH-UA-WoW64, Sec-CH-UA-Arch, Sec-CH-UA-Bitness, Sec-CH-UA-Platform, Sec-CH-UA-Full-Version, Viewport-Width, DPR, Device-Memory, RTT, Downlink, ECT, Width
Location: https://yandex.ru/showcaptcha?mt=CA012A42AC1B294E0AC47928D713349E82304B2C0B65986B80D64A89C849FFD551239F8B9D82210947AAD473D762815A416E289ECD42B9DECDB91FB8B63716EFD5D1AE55AF477535B3798725810BC3FEE7E5CB36C5787341BA9F2F4A9604B41DAB378D20FE4A4161FBE0E18ED124F907950203FA8D8CA00AF2EDB226F57599C96914A470A8E75304F60DEAF84438C863468115A5AC10DC4534A23480A0CEC15C3C99546D0D6421B54ED86BDB3F5415215EB52D62CED1C6F99A1C0B20A44527C50C7EF138AA4F1D2CA09DA9FC7C489C29169B030E47C78DFEC058A60DF1C0&retpath=aHR0cHM6Ly95YW5kZXgucnUvPw%2C%2C_f026dab2c1cb57f806877b1e7f0ae972&t=2/1727804401/ba42f2d6d4871e05c4832b578f87560d&u=49999c7a-bd98db70-298d2b10-90229504&s=6b72888af87e7a525d2ef9eb7ac89fac
NEL: {"report_to": "network-errors", "max_age": 100, "success_fraction": 0.001, "failure_fraction": 0.1}
Report-To: { "group": "network-errors", "max_age": 100, "endpoints": [{"url": "https://dr.yandex.net/nel", "priority": 1}, {"url": "https://dr2.yandex.net/nel", "priority": 2}]}
Transfer-Encoding: chunked
X-Content-Type-Options: nosniff
X-Yandex-Captcha: captcha
X-Yandex-EU-Request: 0
X-Yandex-Req-Id: 1727804401492696-8814306035148675694-balancer-l7leveler-kubr-yp-sas-202-BAL

302 - HTTP-ответ с кодом состояния 302 (Found) указывает на временное перенаправление. Это означает, что запрашиваемый ресурс временно доступен по другому URL, и клиент должен выполнить новый запрос по указанному адресу.
```
3.5.
POST  https://google.com HTTP/1.1

Content-Type: application/json

{
  "title": "foo",
  "body": "bar",
  "userId": 1
}
```
Ответ:
HTTP/1.1 405 Method Not Allowed
Content-Type: text/html; charset=UTF-8
Referrer-Policy: no-referrer
Content-Length: 1589
Date: Tue, 01 Oct 2024 17:43:41 GMT
Alt-Svc: h3=":443"; ma=2592000,h3-29=":443"; ma=2592000
Connection: close

<!DOCTYPE html>
```
3.6.
POST  https://apple.com HTTP/1.1
Content-Type: application/json

{
  "title": "foo",
  "body": "bar",
  "userId": 1
}
```
Ответ:
HTTP/1.1 301 Redirect
Date: Tue, 01 Oct 2024 17:45:00 GMT
Connection: close
Via: http/1.1 sesto4-edge-bx-007.ts.apple.com (acdn/255.14450)
Cache-Control: no-store
Location: https://www.apple.com/
Content-Type: text/html
Content-Language: en
X-Cache: none
CDNUUID: 5e385463-b621-4b9b-8c7a-742002fe883a-14847189100
Content-Length: 304

<HTML>
```
4.GITHUB

https://docs.github.com/en/rest/search?apiVersion=2022-11-28#search-users

4.1.
GET https://api.github.com/search/users?q=EduardAleksandrov

Content-Type: application/json
```
Ответ:
HTTP/1.1 200 OK
Date: Tue, 01 Oct 2024 18:02:09 GMT
Content-Type: application/json; charset=utf-8
Cache-Control: no-cache
Vary: Accept,Accept-Encoding, Accept, X-Requested-With
X-GitHub-Media-Type: github.v3; format=json
x-github-api-version-selected: 2022-11-28
Access-Control-Expose-Headers: ETag, Link, Location, Retry-After, X-GitHub-OTP, X-RateLimit-Limit, X-RateLimit-Remaining, X-RateLimit-Used, X-RateLimit-Resource, X-RateLimit-Reset, X-OAuth-Scopes, X-Accepted-OAuth-Scopes, X-Poll-Interval, X-GitHub-Media-Type, X-GitHub-SSO, X-GitHub-Request-Id, Deprecation, Sunset
Access-Control-Allow-Origin: *
Strict-Transport-Security: max-age=31536000; includeSubdomains; preload
X-Frame-Options: deny
X-Content-Type-Options: nosniff
X-XSS-Protection: 0
Referrer-Policy: origin-when-cross-origin, strict-origin-when-cross-origin
Content-Security-Policy: default-src 'none'
Content-Encoding: gzip
Server: github.com
X-RateLimit-Limit: 10
X-RateLimit-Remaining: 9
X-RateLimit-Reset: 1727805789
X-RateLimit-Resource: search
X-RateLimit-Used: 1
Accept-Ranges: bytes
Content-Length: 375
X-GitHub-Request-Id: 7A2B:18BC28:6C2BB7A:6D7253B:66FC3921
{
  "total_count": 1,
  "incomplete_results": false,
  "items": [
    {
      "login": "EduardAleksandrov",
      "id": 76213460,
      "node_id": "MDQ6VXNlcjc2MjEzNDYw",
      "avatar_url": "https://avatars.githubusercontent.com/u/76213460?v=4",
      "gravatar_id": "",
      "url": "https://api.github.com/users/EduardAleksandrov",
      "html_url": "https://github.com/EduardAleksandrov",
      "followers_url": "https://api.github.com/users/EduardAleksandrov/followers",
      "following_url": "https://api.github.com/users/EduardAleksandrov/following{/other_user}",
      "gists_url": "https://api.github.com/users/EduardAleksandrov/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/EduardAleksandrov/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/EduardAleksandrov/subscriptions",
      "organizations_url": "https://api.github.com/users/EduardAleksandrov/orgs",
      "repos_url": "https://api.github.com/users/EduardAleksandrov/repos",
      "events_url": "https://api.github.com/users/EduardAleksandrov/events{/privacy}",
      "received_events_url": "https://api.github.com/users/EduardAleksandrov/received_events",
      "type": "User",
      "site_admin": false,
      "score": 1.0
    }
  ]
}
```
4.2.
GET https://api.github.com/search/users?q=in:login+repos:>=0&per_page=2&page=2&sort=repositories

Content-Type: application/json
```
Ответ:
HTTP/1.1 200 OK
Date: Tue, 01 Oct 2024 18:03:13 GMT
Content-Type: application/json; charset=utf-8
Cache-Control: no-cache
Vary: Accept,Accept-Encoding, Accept, X-Requested-With
X-GitHub-Media-Type: github.v3; format=json
Link: <https://api.github.com/search/users?q=in%3Alogin+repos%3A%3E%3D0&per_page=2&page=1&sort=repositories>; rel="prev", <https://api.github.com/search/users?q=in%3Alogin+repos%3A%3E%3D0&per_page=2&page=3&sort=repositories>; rel="next", <https://api.github.com/search/users?q=in%3Alogin+repos%3A%3E%3D0&per_page=2&page=500&sort=repositories>; rel="last", <https://api.github.com/search/users?q=in%3Alogin+repos%3A%3E%3D0&per_page=2&page=1&sort=repositories>; rel="first"
x-github-api-version-selected: 2022-11-28
Access-Control-Expose-Headers: ETag, Link, Location, Retry-After, X-GitHub-OTP, X-RateLimit-Limit, X-RateLimit-Remaining, X-RateLimit-Used, X-RateLimit-Resource, X-RateLimit-Reset, X-OAuth-Scopes, X-Accepted-OAuth-Scopes, X-Poll-Interval, X-GitHub-Media-Type, X-GitHub-SSO, X-GitHub-Request-Id, Deprecation, Sunset
Access-Control-Allow-Origin: *
Strict-Transport-Security: max-age=31536000; includeSubdomains; preload
X-Frame-Options: deny
X-Content-Type-Options: nosniff
X-XSS-Protection: 0
Referrer-Policy: origin-when-cross-origin, strict-origin-when-cross-origin
Content-Security-Policy: default-src 'none'
Content-Encoding: gzip
Server: github.com
X-RateLimit-Limit: 10
X-RateLimit-Remaining: 9
X-RateLimit-Reset: 1727805853
X-RateLimit-Resource: search
X-RateLimit-Used: 1
Accept-Ranges: bytes
Content-Length: 494
X-GitHub-Request-Id: 35D7:18BC28:6C39B76:6D807F3:66FC3961
{
  "total_count": 132844603,
  "incomplete_results": true,
  "items": [
    {
      "login": "experiment50",
      "id": 87437101,
      "node_id": "MDEyOk9yZ2FuaXphdGlvbjg3NDM3MTAx",
      "avatar_url": "https://avatars.githubusercontent.com/u/87437101?v=4",
      "gravatar_id": "",
      "url": "https://api.github.com/users/experiment50",
      "html_url": "https://github.com/experiment50",
      "followers_url": "https://api.github.com/users/experiment50/followers",
      "following_url": "https://api.github.com/users/experiment50/following{/other_user}",
      "gists_url": "https://api.github.com/users/experiment50/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/experiment50/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/experiment50/subscriptions",
      "organizations_url": "https://api.github.com/users/experiment50/orgs",
      "repos_url": "https://api.github.com/users/experiment50/repos",
      "events_url": "https://api.github.com/users/experiment50/events{/privacy}",
      "received_events_url": "https://api.github.com/users/experiment50/received_events",
      "type": "Organization",
      "site_admin": false,
      "score": 1.0
    },
    {
      "login": "wp-plugins",
      "id": 2996849,
      "node_id": "MDEyOk9yZ2FuaXphdGlvbjI5OTY4NDk=",
      "avatar_url": "https://avatars.githubusercontent.com/u/2996849?v=4",
      "gravatar_id": "",
      "url": "https://api.github.com/users/wp-plugins",
      "html_url": "https://github.com/wp-plugins",
      "followers_url": "https://api.github.com/users/wp-plugins/followers",
      "following_url": "https://api.github.com/users/wp-plugins/following{/other_user}",
      "gists_url": "https://api.github.com/users/wp-plugins/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/wp-plugins/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/wp-plugins/subscriptions",
      "organizations_url": "https://api.github.com/users/wp-plugins/orgs",
      "repos_url": "https://api.github.com/users/wp-plugins/repos",
      "events_url": "https://api.github.com/users/wp-plugins/events{/privacy}",
      "received_events_url": "https://api.github.com/users/wp-plugins/received_events",
      "type": "Organization",
      "site_admin": false,
      "score": 1.0
    }
  ]
}
```