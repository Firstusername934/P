flowchart TD
  A((Start))
  B[/Input list L of size n/]
  C[Initialize: min = L[1], max = L[1], sum = 0, i = 1]
  D{Is i ≤ n?}
  E{Is L[i] < min?}
  E1[Set min = L[i]]
  F{Is L[i] > max?}
  F1[Set max = L[i]]
  G[sum = sum + L[i]]
  H[i = i + 1]
  I[average = sum / n]
  J[/Output min, max, average/]
  K((End))

  A --> B --> C --> D
  D -- Yes --> E
  E -- Yes --> E1 --> F
  E -- No  --> F
  F -- Yes --> F1 --> G
  F -- No  --> G
  G --> H --> D
  D -- No  --> I --> J --> K
