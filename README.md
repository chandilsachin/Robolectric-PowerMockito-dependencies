# Robolectric-PowerMockito-dependencies
Dependencies for Robolectric and PowerMockito 
``` gradle
dependencies {

    // ...

    ext.power_mockito_version = "1.6.4"
    testCompile 'junit:junit:4.12'
    testCompile 'org.hamcrest:hamcrest-integration:1.3'
    testCompile 'org.easymock:easymock:3.3.1'
    testCompile "org.powermock:powermock-core:$power_mockito_version"
    testCompile "org.powermock:powermock-module-junit4:$power_mockito_version"
    testCompile 'org.powermock:powermock-api-easymock:1.6.2'

    testCompile "org.powermock:powermock-module-junit4:$power_mockito_version"
    testCompile "org.powermock:powermock-module-junit4-rule:$power_mockito_version"
    testCompile "org.powermock:powermock-api-mockito:$power_mockito_version"
    testCompile "org.powermock:powermock-classloading-xstream:$power_mockito_version"

    testCompile "org.robolectric:shadows-multidex:3.0"
    testCompile('org.robolectric:robolectric:3.0') {
        exclude group: 'commons-logging', module: 'commons-logging'
        exclude group: 'org.apache.httpcomponents', module: 'httpclient'
    }

    testCompile 'org.apache.maven:maven-ant-tasks:2.1.3' // fixes mac crash
    testCompile('org.robolectric:shadows-support-v4:3.0') {
        exclude group: 'commons-logging', module: 'commons-logging'
        exclude group: 'org.apache.httpcomponents', module: 'httpclient'
    }
}
```