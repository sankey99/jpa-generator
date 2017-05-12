# jpa-generator
generate jpa entities through gradle

run following command to generate POJO
./gradlew hbm2java //unix/linux
gradlew hbm2java //windows

there is a bug in plugin being used resulting in database url not appending database to  connection url

workarouund -> clean -> ./gradlew clean
./gradlew hbm2java //this will fail
update  hibernate.connection.url in the desired format as expected by your database driver e.g jdbc:postgresql://host:port/database
hi$jpa-generator/build/generated/resources/hibernate.cfg.xml 

run ./gradlew hbm2java // this time it will work
