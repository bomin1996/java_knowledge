### SQL 고급 개념

#### 조인 (JOIN)
- 다른 테이블의 데이터를 결합할 때 사용합니다.
- 예시: `SELECT employees.name, departments.name FROM employees JOIN departments ON employees.department_id = departments.id;`

#### 서브쿼리 (Subquery)
- 쿼리 내부에 또 다른 쿼리를 포함합니다.
- 예시: `SELECT name FROM employees WHERE salary > (SELECT AVG(salary) FROM employees);`

#### 그룹화 및 집계 함수 (GROUP BY, HAVING)
- 데이터를 그룹화하고, 그룹별로 데이터를 집계합니다.
- 예시: `SELECT department_id, AVG(salary) FROM employees GROUP BY department_id HAVING AVG(salary) > 50000;`

#### 윈도우 함수 (Window Functions)
- 데이터의 서브셋에 대한 계산을 수행합니다.
- 예시: `SELECT name, salary, RANK() OVER (ORDER BY salary DESC) FROM employees;`

#### 인덱스 생성 및 관리 (Indexing)
- 데이터 검색 성능을 향상시키기 위해 인덱스를 생성하고 관리합니다.
- 예시: `CREATE INDEX idx_salary ON employees(salary);`

#### 트랜잭션 관리 (Transactions)
- 데이터의 일관성과 무결성을 보장하기 위해 트랜잭션을 사용합니다.
- 예시: 
  ```sql
  START TRANSACTION;
  INSERT INTO accounts (user_id, amount) VALUES (1, 100);
  UPDATE accounts SET amount = amount - 100 WHERE user_id = 2;
  COMMIT;
