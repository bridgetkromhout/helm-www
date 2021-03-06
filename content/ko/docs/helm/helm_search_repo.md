---
title: "Helm Search Repo"
---

## helm search repo

차트에서 키워드에 대한 저장소 검색

### 개요


검색은 시스템에 구성된 모든 저장소를 읽고 일치하는 
항목을 찾는다. 이러한 저장소 검색은 시스템에 
저장된 메타 데이터를 사용한다.

찾은 차트의 최신 안정 버전을 표시한다. 
--devel 플래그를 지정하면 출력에 시험판 버전이 포함된다. 
버전 제약을 사용하여 검색하려면 --version 을 사용하자.

예:

    # 키워드 "nginx" 와 일치하는 안정적인 릴리스 버전 검색
    $ helm search repo nginx

    # 시험판 버전을 포함하여 키워드 "nginx" 와 일치하는 리릴스 버전 검색
    $ helm search repo nginx --devel

    # 주 버전이 1인 nginx-ingress 의 최신 안정 릴리스 검색
    $ helm search repo nginx-ingress --version ^1.0.0

저장소는 'helm repo' 명령어로 관리된다.


```
helm search repo [keyword] [flags]
```

### Options

```
      --devel                개발 버전(알파, 베타 및 릴리스 후보 릴리스)으로 사용. 버전 '> 0.0.0-0' 에 해당하며 --version이 설정되어 있으면 무시.
  -h, --help                 helm search repo 명령어에 대한 도움말
      --max-col-width uint   출력 테이블의 최대 열 너비 (기본값 50)
  -o, --output format        지정된 형식으로 출력. 허용되는 값: table, json, yaml (기본값 table)
  -r, --regexp               추가한 저장소 검색에 정규식 사용
      --version string       추가한 레포지터리에 유의적 버전관리 제약을 사용하여 검색
  -l, --versions             추가한 저장소에 대해 각 차트의 각 버전과 함께 긴 목록을 한 줄에 표시
```

### 부모 명령어에서 상속된 옵션들

```
      --debug                       장황한(verbose) 출력 활성화
      --kube-apiserver string       쿠버네티스 API 서버의 주소 및 포트
      --kube-as-group stringArray   작업에 관해 제시할 그룹. 플래그를 여러 번 사용하여 여러 그룹 지정 가능
      --kube-as-user string         작업에 관해 제시할 사용자명
      --kube-context string         사용할 kubeconfig 컨텍스트 이름
      --kube-token string           인증에 사용될 베어러(bearer) 토큰
      --kubeconfig string           kubeconfig 파일 경로
  -n, --namespace string            이 요청에 대한 네임스페이스 스코프
      --registry-config string      레지스트리 구성 파일에 대한 경로 (기본값 "~/.config/helm/registry.json")
      --repository-cache string     캐시된 저장소 색인이 포함된 파일의 경로 (기본값 "~/.cache/helm/repository")
      --repository-config string    저장소 이름 및 URL 을 포함하는 파일 경로 (기본값 "~/.config/helm/repositories.yaml")
```

### 함께 보기

* [helm search](helm_search.md)	 - 차트에서 키워드 검색

###### Auto generated by spf13/cobra on 29-Oct-2020
