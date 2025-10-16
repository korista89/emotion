# Test Plan

## Automated UI Flow (Playwright)
- Launch a local HTTP server with `python -m http.server 8000` and open `index.html`.
- Log in as class A using the default credentials (`A123`).
- Register a sample student ("테스트학생", grade "초3").
- Switch back to the 데이터 입력 tab and select the registered student.
- Record a session with date `2024-01-15`, 증가 4, 감소 1, memo "테스트 메모".
- Verify that the record appears in the table and that the 입력 탭 remains interactive.
- Capture a screenshot of the resulting state for regression evidence (`artifacts/test-flow.png`).

## Notes
- During tests, the remote Google Apps Script endpoint was unreachable in the container, but all local storage workflows continued to function as expected.
