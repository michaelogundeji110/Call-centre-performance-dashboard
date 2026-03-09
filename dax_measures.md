# DAX Measures Used

## Total Calls
```
Total Calls = COUNT('Call Center'[Call ID])
```

## Answered Calls
```
Answered Calls =
CALCULATE(
    COUNT('Call Center'[Call ID]),
    'Call Center'[Answered] = "Y"
)
```

## Answer Rate %
```
Answer Rate % =
DIVIDE([Answered Calls], [Total Calls])
```

## Resolved Calls
```
Resolved Calls =
CALCULATE(
    COUNT('Call Center'[Call ID]),
    'Call Center'[Resolved] = "Y"
)
```

## Resolution Rate %
```
Resolution Rate % =
DIVIDE([Resolved Calls], [Total Calls])
```

## Average Speed of Answer
```
Avg Speed of Answer =
AVERAGE('Call Center'[Speed of Answer (s)])
```

## Average Satisfaction
```
Avg Satisfaction =
AVERAGE('Call Center'[Satisfaction])
```
