flowchart LR
    A["<b>AC Mains</b><br/>220V<br/>AC"] -->|220VAC| B["<b>Transformer</b><br/>220V to 12V<br/>AC"]
    B -->|12VAC| C["<b>VDR</b><br/>12V to 0.707V<br/>AC"]
    C -->|0.707VAC| D["<b>Sound Card</b><br/>ADC"]
    D -->|010101| E["<b>Simulink</b>"]

    B ~~~ B1["Step<br/>Down"]
    D ~~~ D1["Sampling<br/>and<br/>Quantization"]
    E ~~~ E1["Further<br/>Processing"]

    classDef block fill:#fff,stroke:#000,stroke-width:1.5px,color:#000;
    classDef note fill:none,stroke:none,color:#000;
    class A,B,C,D,E block;
    class B1,D1,E1 note;
