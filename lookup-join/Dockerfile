###############################################################################
#  Licensed to the Apache Software Foundation (ASF) under one
#  or more contributor license agreements.  See the NOTICE file
#  distributed with this work for additional information
#  regarding copyright ownership.  The ASF licenses this file
#  to you under the Apache License, Version 2.0 (the
#  "License"); you may not use this file except in compliance
#  with the License.  You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
#  Unless required by applicable law or agreed to in writing, software
#  distributed under the License is distributed on an "AS IS" BASIS,
#  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#  See the License for the specific language governing permissions and
# limitations under the License.
###############################################################################

FROM mysql:latest
WORKDIR /tpch/dbgen/
# use arm64 based tpch-mysql image
COPY --from=myasuka/tpch-mysql:latest /tpch/dbgen/ /tpch/dbgen/
COPY ./mysql/ /tpch/dbgen/

ARG sf=1

ENV SF=${sf}
ENV MYSQL_DATABASE=tpch_s${SF}

RUN chown -R mysql:mysql /tpch/dbgen/ /docker-entrypoint-initdb.d/ \
    && mv mysql.cnf /etc/mysql/conf.d/ \
    && chmod +x /tpch/dbgen/*.sh \
    && mv a_init_db.sh gen_data.sh load_data.sh /docker-entrypoint-initdb.d/ \
    && chmod +x /docker-entrypoint-initdb.d/*.sh \
    && ln -s dbgen /usr/local/bin/dbgen