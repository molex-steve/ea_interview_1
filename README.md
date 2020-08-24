# Embedded Automation Interview Question 1

<a name="top"></a>

* [Background](#background)
* [Question](#question)
    * [Part A](#question-a)
    * [Part B](#question-b)
    * [Part C](#question-c)
    * [Part D](#question-d)
    * [Part E](#question-e)

<a name="background"></a>

## Background

---

This project is developed to be used as an interview question for Embedded Automation.<br/><br/>
We use web relays to toggle power on devices during automated tests. The relays have an IP address and 8 indexes to toggle (1 - 8). The IP address and index(s) are stored on the internal database and returned as a JSON object from the server.

Here is an example of a return:

```json
{
    "addresses": 
        [
            "192.168.1.101", 
            "192.168.1.102"
        ],
    "indices": 
        [
            1, 
            2
        ]
}
```

<sub><sup>[top](#top)</sup></sub>

<a name="question"></a>

## Question 

---

Given the following series of inputs, please use Python to print the address(s) with it's corresponding index(s).

Here is an example input:

```json
{
    "addresses": 
        [
            "192.168.1.101", 
            "192.168.1.102"
        ],
    "indices": 
        [
            1, 
            1
        ]
}
```

Here is the expected print from Python:

```text
Relays at 192.168.1.101 are 1.
Relays at 192.168.1.102 are 1.
```

<sub><sup>[top](#top)</sup></sub>

<a name="question-a"></a>

### Question Part A

---

Here is the Python input for part A, copy and paste this into your script.

```python
q_a = {"addresses": ["192.168.1.101", "192.168.1.102"], "indices": [1, 1]}
```

<sub><sup>[top](#top)</sup></sub>

<a name="question-b"></a>

### Question Part B

---

Here is the Python input for part B, copy and paste this into your script.

```python
q_b = {"addresses": ["192.168.1.101", "192.168.1.101", "192.168.1.102"], "indices": [1, 2, 1]}
```

<sub><sup>[top](#top)</sup></sub>

<a name="question-c"></a>

### Question Part C

---

Here is the Python input for part C, copy and paste this into your script.

```python
q_c = {"addresses": ["192.168.1.101"], "indices": [1]}
```

<sub><sup>[top](#top)</sup></sub>

<a name="question-d"></a>

### Question Part D

---

Here is the Python input for part D, copy and paste this into your script.

```python
q_d = {"addresses": ["192.168.1.101", "192.168.1.101", "192.168.1.102", "192.168.1.103", "192.168.1.102", "192.168.1.103"], "indices": [1, 2, 1, 1, 2, 2]}
```

<sub><sup>[top](#top)</sup></sub>

<a name="question-e"></a>

### Question Part E

---

Here is the Python input for part E, copy and paste this into your script. These should all print to indicate that there is an error, all previous inputs should work still.

```python
q_e_1 = {"addresses": ["192.168.1.101", "192.168.1.101", "192.168.1.102", "192.168.1.103", "192.168.1.102", "192.168.1.103"], "indices": []}

q_e_2 = {"addresses": ["192.168.1.101", "192.168.1.101", "192.168.1.102", "192.168.1.103", "192.168.1.102", "192.168.1.103"], "indices": [1, 2, 1, 1, 2]}

q_e_3 = {"addresses": ["192.168.1.101", "192.168.1.102"]}
```

<sub><sup>[top](#top)</sup></sub>
