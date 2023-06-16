.jsp
.jsp로 페이지를 사용하고 싶다면 src/main/resources/templates 디렉토리에 jsp파일을 추가하여 사용할 수 있다.
build.gradle -
아래 내용 추가

dependencies {
  compileOnly 'org.apache.tomcat.embed:tomcat-embed-jasper'
  implementation 'javax.servlet:jstl:1.2'
}
페이지 예시

<a href="/study/openjsp">JSP Page 오픈</a>
@RestController
public class JSPController {

  @GetMapping("/openjsp")
  public Object openjsp() {
  // test.jsp 파일을 열고 싶을 때
    return "test";
  }
}
