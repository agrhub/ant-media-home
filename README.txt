How to build the installation file
1. Go to ant-media-server-parent directory

2. Run cmd 'mvn clean install "-Dgpg.skip=true" "-Dmaven.javadoc.skip=true" "-Dmaven.test.skip=true"' to build java projects with maven

3. Go to ManagementConsole_AngularApp to build web panel
$ wget https://nodejs.org/download/release/v14.8.0/node-v14.8.0-linux-x64.tar.gz
$ tar -zxf node-v14.8.0-linux-x64.tar.gz
$ export PATH=$PATH:`pwd`/node-v14.8.0-linux-x64/bin
$ npm install -g @angular/cli@10.0.5 
$ npm install
$ ng build --prod
$ cp -a ./dist/. ../Ant-Media-Server/src/main/server/webapps/root/

4. Go to home directory

5. Run cmd 'mvn clean install "-Dgpg.skip=true" "-Dmaven.javadoc.skip=true" "-Dmaven.test.skip=true"' to build java projects with maven

6. Go to Ant-Media-Server directory

7. Run cmd "./repackage_enterprise.sh" to build installation file
or 'mvn clean package "-P assemble_enterprise" "-Dmaven.javadoc.skip=true" "-Dmaven.test.skip=true"'

More detailed: https://github.com/ant-media/Ant-Media-Server/wiki/Build-From-Source