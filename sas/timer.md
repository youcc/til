#### Set up SAS timer

- At the very beginning of your SAS program, place the following line of code that effectively starts the timer and remembers the start time:

```
/* Start timer */
%let _timer_start = %sysfunc(datetime());
```

- At the end of your SAS program place the following code snippet that captures the end time, calculates duration and outputs it to the SAS log:

```
/* Stop timer */
data _null_;
    dur = datetime() - &_timer_start;
    put 30*'-' / ' TOTAL DURATION:' dur time13.2 / 30*'-';
run;
```

Reference: https://blogs.sas.com/content/sgf/2015/01/21/sas-timer-the-key-to-writing-efficient-sas-code/