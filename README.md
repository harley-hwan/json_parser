# json_parser
RapidJSON 라이브러리를 사용한 C++ JSON 파서

<br/>

__'JsonParser'__ 클래스는 JSON 객체를 읽고, 쓰고, 파싱하고, 수정하고, 탐색하는 메서드를 제공합니다.

JsonParser 클래스의 주요 기능은 다음과 같습니다:

1. 생성자 및 소멸자:
- __'JsonParser(bool \_is_debug_print)'__: JsonParser 인스턴스를 생성하고 인수가 true인 경우 디버그 출력을 활성화합니다.
- __'~JsonParser(void)'__: JsonParser 클래스의 소멸자입니다.

2. 디버그 출력 기능:
- __'void print_debug_info(const char \*\_format, ...)'__: 디버그 출력이 활성화된 경우 디버그 정보를 출력합니다.
- __'void set_debug_print(void)'__: 디버그 출력을 활성화합니다.

3. 파일 입출력 기능:
- __'string read_file(string \_file_path)'__: 파일의 내용을 읽고 문자열로 반환합니다.
- __'bool write_file(string \_file_path, string \_json_string)'__: 문자열의 내용을 파일에 씁니다.
- __'bool write_json(string \_file_path)'__: JSON 문서를 예쁜 형식으로 파일에 씁니다.

4. JSON 파싱 및 변환 기능:
- __'bool parse(const string \_json_string)'__: JSON 문자열을 파싱하고 내부 문서 객체에 저장합니다.
- __'string to_string(void)'__: JSON 문서를 문자열 표현으로 변환합니다.
5. JSON 조작 기능:
- __'string select(string \_node_path)'__ : 노드 경로로 지정된 JSON 노드의 값을 반환합니다.
- __'bool update(string \_node_path, int/double/string \_value)'__: 노드 경로로 지정된 JSON 노드의 값을 업데이트합니다.
- __'bool add(string \_node_path, int/double/string \_value)'__: 지정된 값으로 새 JSON 노드를 추가합니다(존재하지 않는 경우).
- __'bool remove(string \_node_path)'__: 노드 경로로 지정된 JSON 노드를 제거합니다.
6. 유틸리티 기능:
- __'vector\<string> split(string \_string, string \_delimiter)'__ : 구분자를 사용하여 문자열을 분할하고 토큰의 벡터를 반환합니다.
- __'string replace_all(string &\_str, const string& \_from, const string& \_to)'__ : 문자열에서 부분 문자열의 모든 발생을 다른 부분 문자열로 바꿉니다.

<br/>

<br/>

1. 파일 읽기 및 쓰기: __'read_file()'__ 및 __'write_file()'__ 함수를 사용하여 JSON 파일을 읽고 쓸 수 있습니다.
2. JSON 객체 파싱: __'parse()'__ 함수를 사용하여 주어진 JSON 문자열을 파싱하고 내부 데이터 구조에 저장합니다.
3. JSON 객체를 문자열로 변환: __'to_string()'__ 함수를 사용하여 내부 JSON 객체를 JSON 문자열로 변환합니다.
4. 노드 선택: __'select()'__ 함수를 사용하여 JSON 객체에서 특정 노드를 선택하고 값을 가져옵니다.
5. 노드 업데이트: __'update()'__ 함수를 사용하여 JSON 객체에서 특정 노드의 값을 수정합니다.
6. 노드 추가: __'add()'__ 함수를 사용하여 JSON 객체에 새로운 노드를 추가합니다.
7. 노드 제거: __'remove()'__ 함수를 사용하여 JSON 객체에서 특정 노드를 삭제합니다.
8. JSON 파일 쓰기: __'write_json()'__ 함수를 사용하여 내부 JSON 객체를 파일로 저장합니다.
9. 문자열 분할: __'split()'__ 함수를 사용하여 주어진 문자열을 구분자를 기준으로 분할합니다.
10. 문자열 치환: __'replace_all()'__ 함수를 사용하여 문자열에서 특정 부분을 다른 문자열로 치환합니다.
11. 디버그 출력: __'print_debug_info()'__ 함수를 사용하여 디버그 정보를 출력할 수 있습니다. 이를 통해 파서 작업을 모니터링하고 문제를 해결하는 데 도움이 됩니다.
