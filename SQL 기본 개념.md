#### 데이터 조회 (SELECT)
- `SELECT` 문을 사용하여 테이블에서 데이터를 조회할 수 있습니다.
- 예시: `SELECT * FROM employees;` (employees 테이블의 모든 데이터 조회)

#### 데이터 필터링 (WHERE)
- `WHERE` 절을 사용하여 특정 조건을 만족하는 데이터만 조회할 수 있습니다.
- 예시: `SELECT * FROM employees WHERE age > 30;` (나이가 30세 이상인 직원 조회)

#### 데이터 정렬 (ORDER BY)
- `ORDER BY` 절을 사용하여 조회 결과를 특정 컬럼을 기준으로 정렬할 수 있습니다.
- 예시: `SELECT * FROM employees ORDER BY salary DESC;` (급여 기준 내림차순 정렬)

#### 데이터 삽입 (INSERT)
- `INSERT INTO` 문을 사용하여 테이블에 새로운 데이터를 삽입할 수 있습니다.
- 예시: `INSERT INTO employees (name, age, salary) VALUES ('John Doe', 28, 50000);` (새 직원 추가)

#### 데이터 업데이트 (UPDATE)
- `UPDATE` 문을 사용하여 테이블의 기존 데이터를 수정할 수 있습니다.
- 예시: `UPDATE employees SET salary = 60000 WHERE name = 'John Doe';` (John Doe의 급여 수정)

#### 데이터 삭제 (DELETE)
- `DELETE FROM` 문을 사용하여 테이블에서 데이터를 삭제할 수 있습니다.
- 예시: `DELETE FROM employees WHERE age < 25;` (25세 미만 직원 삭제)
