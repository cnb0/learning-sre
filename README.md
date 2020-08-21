# learning-sre
 
- SREs write code to fix those bugs
- SREs write software to run other software
- SREs write Kubernetes Operators
- Add metrics awareness and tuning to your Operator


- Level 1 
      -  Installation/Deployment
          - Can you set operand configuration in the CR?
          - Do CR changes cause non-disruptive updates to the Operand?
          - Does CR status show what has and hasn’t been applied?
- Level 2 
      - Upgrades
         - Can the Operator upgrade its Operand?
         - Without disruption?
         - Does CR status show what has and hasn’t been upgraded?
- Level 3
      - Full Lifecycle Management
          - Can your Operator back up its Operand?
          - Can your Operator restore from a previous Operand backup?
          - Ready/Live probes? Active monitoring of basic execution state?
          - CPU and other requests and limits set for Operand?

- Level 4
      - Deep insights
         - Does the Operator expose metrics about its own health?
         - Metrics and alerts for the Operand?
         - Does CR status show what has and hasn’t been applied?

- Level 5
      - Auto Pilot
          - Auto scaling, healing, tuning
                - Detect condition from metrics, scale horizontally (Replicas) or 
                  vertically (Requests/Limits)
          - Think especially about scaling back down; resource savings
          - Detecting deterioration in Operand(s) (based on Level 4’s metrics) and take
            action to redeploy or reconfigure
      - CR Status, custom Events: Clear status and especially error conditions

- RED
        - Rate (aka Traffic) - Errors - Duration (aka Latency
        - The RED Method defines three key metrics for every service
          - Rate (the number of requests per second)
          - Errors (the number of those requests that are failing)
          - Duration (the amount of time those requests take)
