## Lab 2: Password Aging Policies

### Objective
Enforce account security policies for `natasha`:
1. Max password age: 90 days.
2. Min password age: 2 days.
3. Warning period: 7 days.

### Implementation Commands
```bash
chage -M 90 -m 2 -W 7 natasha
```

### Verification
```bash
chage -l natasha
```


#### Verification Proof
![Chage verification output success](./user-management/lab-proofs/lab2-proof.png)
