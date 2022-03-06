
-- Mar 2, 2022
Currently these projects require local builds to get the versions referenced 
in the cxf.
 
  https://github.com/apache/activemq-artemis.git  version: 2.21.0-SNAPSHOT
  https://github.com/apache/cxf-build-utils.git   version: 3.4.5-SNAPSHOT
  https://github.com/apache/cxf-xjc-utils.git     version: 4.0.0-SNAPSHOT

  https://github.com/spring-projects/spring-ldap.git  version: 2.4.0-M2 
  https://github.com/spring-projects/spring-boot.git  version: 3.0.0-M1
  https://github.com/spring-projects/spring-framework.git version: 6.0.0-M2
  https://github.com/spring-projects/spring-security.git  version: 6.0.0-M1

  https://github.com/eclipse-ee4j/jaxb-fi.git
      - checkout tagged branch 2.1.0-M1
      - build with this cmd
          mvn install -Poss-release -Dgpg.skip=true -Dcopyright.ignoreyear=true

-- needed for
(my changes) https://github.com/rsearls/ws-wss4j/tree/jakarta-namespace-upgrade-ver-3.0.0-SNAPSHOT
(my changes) https://github.com/rsearls/jaxb-ri/tree/jakarta-updates-4.0.0-M3-RI
(my changes) https://github.com/rsearls/cxf-xjc-utils/tree/jakarta-gen-fix
        - build it without running test.  There is a jdk-17 (reflection) issue
          that can't be easily solved currently.
            mvn clean install -DskipTests














