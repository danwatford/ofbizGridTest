Created by running the following command in the ofbiz sources directory:

./gradlew createPlugin -PgridTest

Areas to note:
- Ensure the allowedPaths init-param is set to allow the js and css directories in gridTest/webapp/gridTest/WEB-INF/web.xml
        <init-param>
            <param-name>allowedPaths</param-name>
            <param-value>/error:/control:/select:/index.html:/index.jsp:/default.html:/default.jsp:/images:/js:/css</param-value>
        </init-param>



To run, copy/clone to ofbiz/plugins/gridTest.

From ofbiz sources directory run:

./gradlew cleanAll
./gradlew "ofbiz --load-data readers=seed,seed-initial,demo" loadAdminUserLogin -PuserLoginId=admin
./gradlew ofbiz

Visit https://localhost:8443/gridTest (you may need to force your browser to access the site as it will be using
an recognised certificate.)

The GridTest plugin's main screen is displayed, using some demo data in a grid.
