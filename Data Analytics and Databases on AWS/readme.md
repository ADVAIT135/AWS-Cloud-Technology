
# Data Analytics and Databases on AWS

This repository contains course materials, lab exercises, notes, and cheat sheets for learning **Data Analytics and Databases on AWS**. It covers ETL/ELT processes, SQL fundamentals, AWS services, and practical labs with real-world scenarios.

---

## 📘 Course Roadmap

### Module 01: Foundations of Data Analysis
- Business use case assessment  
- ETL and ELT data-processing  
- Differences between structured, unstructured, and semistructured data  
- Importance of metadata  

### Module 02: ETL Pipeline and Database Foundations
- The ETL pipeline  
- SQL vs NoSQL databases  
- Common SQL queries  

### Module 03: AWS Services for ETL
- Amazon API Gateway  
- Amazon QuickSight  
- Amazon Relational Database Service (Amazon RDS)  
- Identifying the right service for the job  

---

## 📝 Important Notes

### Data Analytics in Everyday Life
Data analytics is everywhere—from customer preferences to competitive advantage. With the rise of big data, traditional tools fall short, and cloud services like **AWS** provide scalable solutions for real-time and batch processing.

### ETL vs ELT
- **ETL (Extract, Transform, Load):** Transform data before loading into the target system. Best for structured data and legacy systems.  
- **ELT (Extract, Load, Transform):** Load raw data first, then transform inside the target system. Best for modern analytics, big data, and unstructured datasets.  

| Category | ETL | ELT |
|----------|-----|-----|
| Process | Transform before load | Load first, transform later |
| Speed | Slower | Faster |
| Data Compatibility | Structured | Structured, unstructured, semi-structured |
| Cost | Higher setup | More cost-efficient |
| Security | Custom apps | Built-in database features |

### Data Visualization
Visualization is key to analytics. AWS provides:
- **Amazon QuickSight**: Interactive dashboards, ML-powered insights.  
- **Amazon Managed Grafana**: Open-source visualization for metrics and logs.  

Common chart types: KPI charts, scatter plots, bubble charts, bar/line charts, histograms, pie charts, stacked charts, treemaps.

---

## 💻 Labs

### Lab 1
Hands-on exercises with AWS services for ETL and analytics.

### Lab 2: AWS Lambda FAQ
- **What is AWS Lambda?** Run code without provisioning servers. Pay only for compute time.  
- **Triggers:** DynamoDB updates, S3 object changes, CloudWatch logs, SNS notifications, Kinesis streams, scheduled events.  
- **Languages Supported:** Node.js, Python, Java, Go, Ruby, Bash.  
- **Stateless Functions:** Each Lambda runs in isolation; persistent state stored in S3/DynamoDB.  

### Lab 3: RDS Connection
```bash
mysql --user student --password --host my-rds.cpqpozbusork.us-west-2.rds.amazonaws.com
```
### Lab 4: Player Analytics
Using **Amazon QuickSight** to analyze crossing averages by name and age.  
Example: Bottom 20 in age and top 20 in name.  
Players include: P. Socha, M. Benmoussa, C. Ibarra, R. Richards, G. Gilliespie, A. Karabec, D. Udogie, J. Brand, K. De Bruyne, Vinícius Júnior, Pedri, Ansu Fati, K. Mbappé, Ferran Torres, Cristiano Ronaldo, and many more.

---

## 📊 SQL Cheatsheet

### Glossary
- **SQL**: Language for relational databases.  
- **Schema**: Defines structure.  
- **Primary Key**: Unique identifier.  
- **Foreign Key**: Links tables.  

### Common Statements
```sql
-- Create database and table
CREATE DATABASE web_store;
CREATE TABLE orders (
  orderID INT PRIMARY KEY,
  itemID INT NOT NULL,
  department VARCHAR(50),
  customerName VARCHAR(50),
  QTY INT NOT NULL,
  price VARCHAR(10),
  orderDate DATE
);

-- Insert data
INSERT INTO orders (orderID, itemID, department, customerName, QTY, price, orderDate)
VALUES (13293, 1234, 'electronics', 'Nikki Wolf', 1, '19.99', '2023/09/12');

-- Update data
UPDATE orders SET QTY = 1, price = '2.99' WHERE orderID = 64345;

-- Select data
SELECT * FROM orders;
SELECT department FROM orders;
SELECT QTY, orderDate FROM orders WHERE orderDate BETWEEN '2023/09/01' AND '2023/09/30';

-- Aggregate functions
SELECT SUM(price) FROM orders;
SELECT AVG(QTY) FROM orders;

-- Delete data
DELETE FROM orders WHERE customerName = 'Martha Rivera';

-- Drop table
DROP TABLE orders;
```

---

## ⚽ Player Analytics Dashboards

### Top 30 Players
| Name | Attacking | Crossing | Dribbling |
|------|-----------|----------|-----------|
| Cristiano Ronaldo | 437 | 84 | 88 |
| C. Sinclair | 432 | 82 | 85 |
| A. Griezmann | 425 | 83 | 87 |
| C. Hansen | 418 | 88 | 92 |
| D. Marozsán | 411 | 89 | 90 |

### Top Dribblers
- L. Messi  
- Neymar  
- Cristiano Ronaldo  
- M. Rapinoe  
- T. Heath  

### Top Free-Attackers
- Cristiano Ronaldo  
- L. Messi  
- R. Lewandowski  
- V. Miedema  
- H. Kane  

### Value and Power
Players sorted by **power vs value (in millions €)**:
- Cristiano Ronaldo  
- A. Popp  
- Casemiro  
- T. Partey  
- M. Behringer  

---

## 🚀 Key Takeaways
- **ETL vs ELT**: Choose based on data type and workload.  
- **SQL**: Core language for relational databases.  
- **AWS Services**: Lambda, RDS, QuickSight, Glue, Kinesis, DynamoDB.  
- **Visualization**: Essential for insights; QuickSight and Grafana are powerful tools.  
- **Player Analytics**: Demonstrates real-world use of AWS QuickSight for sports data.  

---


