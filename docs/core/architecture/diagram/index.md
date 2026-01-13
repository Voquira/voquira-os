```mermaid
flowchart TD
    A[Inputs<br/>Forms · CRM · APIs · Payments · Weather · Events]

    B[Core Operational Model<br/>Jobs · Visits · Schedules<br/>Crews / Technicians<br/>Customers · Invoices · State]

    C[Automation & AI Agents<br/>Dispatcher · Scheduler · AR · Comms · Compliance]

    D[Execution Systems<br/>Field Crews · Techs<br/>Scheduling Tools · Billing · Messaging]

    E[Outputs & Feedback<br/>Completion · Invoices · Payments · Metrics]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> A


### Why this is the best choice
- No asset paths
- No baseurl issues
- Renders natively on GitHub Pages
- Easy to modify as the system evolves
- Matches your written architecture **exactly**

After commit, refresh:


