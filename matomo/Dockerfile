FROM matomo:4.1.0
LABEL maintainer="noname.spyware@gmail.com"
LABEL version="4.1.0"

ENV MATOMO_MYSQL_HOST="172.16.2.200" \
    MATOMO_MYSQL_USER="matomo" \
    MATOMO_MYSQL_PASSWORD="matomo" \
    MATOMO_MYSQL_DBNAME="matomo" \
    MATOMO_MYSQL_PORT=3306 \
    MATOMO_MYSQL_TBL_PREFIX="matomo_"

COPY --chown=1000:1000 configs/global.ini.php /usr/src/matomo/config/

RUN chmod 755 /usr/src/matomo/config/global.ini.php

COPY --chown=1000:1000 plugins/ /usr/src/matomo/plugins/
RUN chmod -R 755 /usr/src/matomo/plugins

# RUN chmod 755 /usr/src/matomo/plugins/Bandwidth
# RUN chmod 755 /usr/src/matomo/plugins/LanguageToogle
# RUN chmod 755 /usr/src/matomo/plugins/PerformanceAudit
# RUN chmod 755 /usr/src/matomo/plugins/ProfileAvatar
# RUN chmod 755 /usr/src/matomo/plugins/EnvironmentVariables
