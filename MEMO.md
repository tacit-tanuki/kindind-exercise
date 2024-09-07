
```
❯ docker compose build
WARN[0000] /home/vagrant/ghq/github.com/tacit-tanuki/kindind-exercise/docker-compose.yaml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion
[+] Building 45.6s (9/9) FINISHED                                                                 docker:default
 => [kind internal] load build definition from Dockerfile                                                   0.1s
 => => transferring dockerfile: 668B                                                                        0.0s
 => [kind internal] load metadata for docker.io/library/docker:stable-dind                                  2.8s
 => [kind internal] load .dockerignore                                                                      0.1s
 => => transferring context: 2B                                                                             0.0s
 => [kind 1/4] FROM docker.io/library/docker:stable-dind@sha256:4972457c6a8a4309f9796fc3c8fd288923045ba0e  19.1s
 => => resolve docker.io/library/docker:stable-dind@sha256:4972457c6a8a4309f9796fc3c8fd288923045ba0e214c10  0.0s
 => => sha256:4972457c6a8a4309f9796fc3c8fd288923045ba0e214c102d92b70be99e249d1 1.00kB / 1.00kB              0.0s
 => => sha256:6f19136cf89d49aee8fa560eaab20e034c6ee17bbce55a9d33e1fbe5baa35b03 6.36kB / 6.36kB              0.0s
 => => sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457 2.04MB / 2.04MB              1.0s
 => => sha256:2a7e15ecad4d18a6bb71b1b828dc7bb1b1a6c890e7420a89726a0649e94e8fb1 2.61kB / 2.61kB              0.0s
 => => sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964 2.80MB / 2.80MB              0.7s
 => => sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658 153B / 153B                  0.8s
 => => extracting sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964                   0.6s
 => => sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef 62.89MB / 62.89MB           11.1s
 => => sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6 549B / 549B                  1.1s
 => => sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946 1.02kB / 1.02kB              1.3s
 => => sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e 116B / 116B                  1.5s
 => => sha256:9ec33e9a5dc986ed79c57562e16a160920e60a9045ad42b230c8b3c3c2500937 5.96MB / 5.96MB              3.6s
 => => sha256:7f95e189f660a26dc7fef2e6cb0cb97e5fd58a2cc3d94401ec05ec021b5d88ec 1.28kB / 1.28kB              2.0s
 => => extracting sha256:0c7c675703d60dc4d757acb40557350159f600ca3d49e2e8d4c2039dd6b69457                   0.6s
 => => sha256:48132e2f3ac7e59ba71722801162920cf61f245698f60bf839dc424199bbfceb 932B / 932B                  2.9s
 => => extracting sha256:cc8c12a437cbe4e104dcea425e0ce277a2442603e14551d22a948e11026ae658                   0.0s
 => => sha256:97b4df673d204888097abe33a208c939806155dbd1b8e08ea0f23b7dee721183 2.51kB / 2.51kB              3.4s
 => => extracting sha256:f092543453df2d4fbc4652f5584b56dd62987a33816ffd2a8d7ad9fad249b1ef                   5.8s
 => => extracting sha256:65b6bc45957d739e38db2da98d43e419af5fc45c46b8149f61b743dc613383e6                   0.0s
 => => extracting sha256:4de832df471bbad41016f9621737b66aa5d8e575d7676661d111ea80b87e3946                   0.0s
 => => extracting sha256:79aa7fa92271a7c1a46782d83623d7b9a111a2236c077aa11fe4bb289865955e                   0.0s
 => => extracting sha256:9ec33e9a5dc986ed79c57562e16a160920e60a9045ad42b230c8b3c3c2500937                   0.9s
 => => extracting sha256:7f95e189f660a26dc7fef2e6cb0cb97e5fd58a2cc3d94401ec05ec021b5d88ec                   0.0s
 => => extracting sha256:48132e2f3ac7e59ba71722801162920cf61f245698f60bf839dc424199bbfceb                   0.0s
 => => extracting sha256:97b4df673d204888097abe33a208c939806155dbd1b8e08ea0f23b7dee721183                   0.0s
 => [kind 2/4] RUN apk update && apk add curl &&   curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.17.0/kin  4.8s
 => [kind 3/4] RUN curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://  10.6s
 => [kind 4/4] RUN curl https://raw.githubusercontent.com/helm/helm/HEAD/scripts/get-helm-3 | ash           7.3s
 => [kind] exporting to image                                                                               0.5s
 => => exporting layers                                                                                     0.4s
 => => writing image sha256:081fced232dab3ea8d74dd935609bdce2b7ca54307b486aa0f82412801c7b47f                0.0s
 => => naming to docker.io/library/kindind-exercise-kind                                                    0.0s
 => [kind] resolving provenance for metadata file 

❯ docker images kindind-exercise-kind
REPOSITORY              TAG       IMAGE ID       CREATED              SIZE
kindind-exercise-kind   latest    081fced232da   About a minute ago   353MB
```

```
❯ docker compose up -d
WARN[0000] /home/vagrant/ghq/github.com/tacit-tanuki/kindind-exercise/docker-compose.yaml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion
[+] Running 2/2
 ✔ Network kindind-exercise_default  Created                                                                0.8s
 ✔ Container kind                    Started                                                                0.7s 
```
```