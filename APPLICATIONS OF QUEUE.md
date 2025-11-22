# Exp.No:40  
## APPLICATIONS OF QUEUE

---

### AIM  
To write a Python program to implement CPU Process Scheduling using a queue.

---

### ALGORITHM  

1. Start the program.  
2. Define the function `CalculateWaitingTime(at, bt, N)`.  
3. Initialize a list `wt` of size `N` with all values set to 0.  
4. Set `wt[0] = 0` for the first process.  
5. Print the table header: "P.No.", "Arrival Time", "Burst Time", "Waiting Time".  
6. Print the values for the first process.  
7. For each process from index `1` to `N-1`:  
   - Calculate `wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]`.  
   - Print the process number, arrival time, burst time, and waiting time.  
8. Initialize `total_waiting_time = 0`.  
9. Add up all waiting times.  
10. Calculate average waiting time as `average = total_waiting_time / N`.  
11. Print the average waiting time.  
12. Get burst times as input from the user for 5 processes.  
13. Call `CalculateWaitingTime()` with `at`, `bt`, and `N`.  
14. End the program.

---

### PROGRAM  

```
# REGNO:-212222060229
# NReg.No: 212223060305
Name: Vishnu Priya E

def CalculateWaitingTime(at, bt, N):
	wt = [0]*N;

	wt[0] = 0;

	print("P.No.\tArrival Time\t" , "Burst Time\tWaiting Time");
	print("1" , "\t\t" , at[0] , "\t\t" , bt[0] , "\t\t" , wt[0]);

	for i in range(1,5):
		wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i];

		print(i + 1 , "\t\t" , at[i] , "\t\t" , bt[i] , "\t\t" , wt[i]);

	average = 0.0;
	sum = 0;

	for i in range(5):
		sum = sum + wt[i];

	average = sum / 5;

	print("Average waiting time = " , average);
N = 5;
at = [ 0, 1, 2, 3, 4 ];

bt=[]
for i in range(0, 5):
    ele = int(input())
    bt.append(ele)
CalculateWaitingTime(at, bt, N);ame:-Penumalli GowriNandini

```

### OUTPUT
<img width="1070" height="480" alt="image" src="https://github.com/user-attachments/assets/b00ebf67-ad7f-45b8-bd5f-c30ec898a247" />


### RESULT
Thus the Python program to implement CPU Process Scheduling using a queue implemented and executed successfully.
