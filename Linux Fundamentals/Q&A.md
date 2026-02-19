### 1. What happens Servers Disk becomes 100% full or Why might the application crash?
Disk full is not a "storage problem" | It is 

- Logging failure problem (access/errors logs) (transactions logs) log writes fails
- Database failure - (It stores data and maintain transaction logs) if fails data can be corrupt
- Monitoring failure
- Services startup problem
- Potential data loss 

### 2. An application suddenly starts logging 10GB per hour. Why might that happen?
