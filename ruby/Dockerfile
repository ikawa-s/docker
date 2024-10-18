# FROM amazonlinux:2

# # 言語・時刻設定・パッケージインストール
# RUN yum install -y glibc-langpack-ja && \
#   ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
#   yum install -y cmake gcc-c++ git make readline-devel mysql-devel tar bzip2 which openssl-devel \
#   wget unzip procps mariadb-libs openssl libffi-devel libyaml-devel 1>/dev/null

# # RUBYインストール
# ARG RUBY_VERSION="3.2.2"
# RUN git clone https://github.com/sstephenson/ruby-build.git && \
#   ruby-build/bin/ruby-build ${RUBY_VERSION} /usr/local/ruby/
# ENV PATH /usr/local/ruby/bin:$PATH

FROM ruby:3.2.2

COPY ./sample.rb /sample.rb

CMD ["ruby", "/sample.rb"]
