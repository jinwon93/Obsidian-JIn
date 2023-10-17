애플리케이션에서 인스턴스를 하나만 만들어 사용하기 위한 패턴



₩₩₩
public class Singleton {
    // private static 변수로 유일한 인스턴스를 저장
    private static Singleton instance;

    // private 생성자로 외부에서의 인스턴스화 방지
    private Singleton() {
        // 초기화 코드
    }

    // 인스턴스에 접근할 수 있는 메서드
    public static Singleton getInstance() {
        // 인스턴스가 없을 경우에만 인스턴스 생성
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }

    // 다른 메서드들
    public void someMethod() {
        // 동작 정의
    }
}
₩₩₩
