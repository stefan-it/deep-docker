from nvidia/cuda:9.0-devel

RUN apt update && DEBIAN_FRONTEND=noninteractive apt install -y locales \
    graphviz python3-pip git-core make build-essential libssl-dev \
    zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl \
    llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev

RUN sed -i -e 's/# de_DE.UTF-8 UTF-8/de_DE.UTF-8 UTF-8/' /etc/locale.gen && \
    dpkg-reconfigure --frontend=noninteractive locales && \
    update-locale LANG=de_DE.UTF-8


RUN git clone git://github.com/yyuu/pyenv.git .pyenv

ENV LANG de_DE.UTF-8
ENV PYENV_ROOT /.pyenv
ENV PATH $PYENV_ROOT/shims:$PYENV_ROOT/bin:$PATH

RUN pip3 install pipenv
