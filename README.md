# Tistory 문제 변환기

이 HTML + JavaScript 웹 툴은 Notion, Markdown 등에서 복사한 텍스트를 **Tistory 블로그용 HTML 형식**으로 자동 변환해줍니다. 문제, 코드, 정답/풀이 블럭, 마크다운 테이블까지 지원합니다.

---

## ✅ 기능 설명

### 1. **문제/정답/풀이 블럭 자동 인식**
- `**1. 문제 내용` → `<h4>` 태그
- `- 정답` 또는 `- 풀이` → `더보기 토글 블럭`으로 감싸짐
- 각 내용은 `<p data-ke-size="size16">...</p>`로 감싸짐

### 2. **코드 블럭 처리**
- 마크다운 코드 블럭 (```로 감싼 영역)을 자동 인식해
  ```html
  <pre class="arduino"><code>...</code></pre>
  ```
  형식으로 변환

### 3. **마크다운 테이블 자동 변환**
- 아래처럼 생긴 테이블은:
  ```markdown
  | A | B | C |
  | -- | -- | -- |
  | a1 | b1 | c1 |
  ```
- 다음 HTML로 변환됩니다:
  ```html
  <table style="border-collapse: collapse; width: 100%;" border="1" data-ke-align="alignLeft">
    <tbody>
      <tr><td>A</td><td>B</td><td>C</td></tr>
      <tr><td>a1</td><td>b1</td><td>c1</td></tr>
    </tbody>
  </table>
  ```

### 4. **리스트 지원**
- `- 항목1`, `- 항목2` 형태의 리스트도 HTML 리스트로 변환됨

### 5. **복사하기 버튼**
- 변환된 결과 아래에 있는 `결과 복사하기` 버튼 클릭 시 자동 복사

---

## 🛠 사용법

1. 문제/정답/풀이/코드/표 형식의 마크다운 텍스트를 복사
2. 텍스트 상자에 붙여넣기
3. **[변환하기]** 버튼 클릭
4. 아래 출력된 HTML 복사 → Tistory 에디터에 붙여넣기
5. 필요시 **[결과 복사하기]** 버튼으로 자동 복사 가능

---

## 💡 예시 입력 템플릿
```md
**1. 다음 Java 코드를 보고 결과를 쓰시오**

```java
System.out.print("Hello Tistory");
```

- 정답
    Hello Tistory

- 풀이
    ```java
    System.out.print(...)
    ```
    → 단순 출력
```

---

## 📁 파일로 저장 원할 시
이 HTML 파일을 `.html`로 저장 후 브라우저에서 실행하세요.

---

문의 및 피드백은 언제든지 환영입니다 🙌
