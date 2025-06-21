```mermaid
flowchart TD
  %% Start
  A((Start))
  
  %% Input
  B[/ Input list L of size n /]
  
  %% Initialization
  C[Initialize:\nmin ← L[1]\nmax ← L[1]\nsum ← 0\ni ← 1]
  
  %% Loop condition
  D{ i ≤ n ? }
  
  %% Check minimum
  E{ L[i] < min ? }
  E1[min ← L[i]]
  
  %% Check maximum
  F{ L[i] > max ? }
  F1[max ← L[i]]
  
  %% Sum and advance
  G[ sum ← sum + L[i] ]
  H[ i ← i + 1 ]
  
  %% After loop
  I[ average ← sum ÷ n ]
  J[/ Output min, max, average /]
  K((End))
  
  %% Flow arrows
  A --> B --> C --> D
  D -- Yes --> E
  E -- Yes --> E1 --> F
  E -- No  --> F
  F -- Yes --> F1 --> G
  F -- No  --> G
  G --> H --> D
  D -- No  --> I --> J --> K
