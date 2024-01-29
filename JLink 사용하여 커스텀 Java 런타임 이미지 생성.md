# JLink 사용하여 커스텀 Java 런타임 이미지 생성
jlink --module-path $JAVA_HOME/jmods:path/to/your/app/modules \
      --add-modules java.base,java.sql,your.app.module \
      --output path/to/output/runtime-image \
      --compress 2 --no-header-files --no-man-pages

# JPackage 사용하여 Windows 실행 파일 생성
jpackage --type exe \
         --input path/to/app \
         --main-jar your-app.jar \
         --main-class com.example.YourApp \
         --runtime-image path/to/output/runtime-image \
         --dest path/to/output \
         --name "YourApp"
