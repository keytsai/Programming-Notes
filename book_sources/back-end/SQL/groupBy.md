# GROUP BY

>群組化表格資料，可以用來搭配聚合函數

## 聚合函數

>可以執行所選取的欄位值的筆數、平均、統計等，以便資料分析

| 聚合函數 | 作用               |
| -------- | ------------------ |
| Count    | 取得欄位資料筆數   |
| Sum      | 取得欄位資料總和   |
| Max      | 取得欄位資料最大值 |
| Min      | 取得欄位資料最小值 |
| Avg      | 取得欄位資料平均值 |

### EX1

```SQL
-- SELECT列出來的欄位，除了聚集函數的欄位外，其餘都要列在GROUP BY條件中，否則會不符合閱讀邏輯
-- 如把 Author 從GROUP BY拿掉就會出錯
SELECT PUBLISHER_ID, AUTHOR, COUNT(BOOK_NAME) AS BOOK_COUNT
FROM BOOK
GROUP BY PUBLISHER_ID, AUTHOR
ORDER BY BOOK_COUNT DESC;
```

### EX2

```SQL
--查部門最高薪、最低薪
SELECT DNAME 部門名, MAX(SAL) 最高薪水, MIN(SAL) 最低薪水 FROM EMP2 E JOIN DEPT2 D ON E.DEPTNO = D.DEPTNO
GROUP BY DNAME;

--查部門平均薪資
SELECT DNAME, ROUND(AVG(SAL)) 平均薪資 FROM EMP2 E JOIN DEPT2 D ON E.DEPTNO = D.DEPTNO
GROUP BY DNAME;

--查部門人數
SELECT DNAME, COUNT(ENAME) 部門人數 FROM EMP2 E JOIN DEPT2 D ON E.DEPTNO = D.DEPTNO
GROUP BY DNAME;
```

## References

[SQL Group By](https://www.1keydata.com/tw/sql/sqlgroupby.html)
