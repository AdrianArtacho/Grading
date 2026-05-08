# Grading

A lightweight browser-based grading calculator for [GitHub Pages](https://adrianartacho.github.io/Grading/).

This tool converts numeric exam scores into grades using a configurable grading scale.

The grading system is controlled entirely through URL parameters, making it easy to reuse for different courses, exams, or grading systems without editing the code.

---

## Features

* Browser-based (no backend required)
* Works on GitHub Pages
* URL-configurable grading system
* Decimal grades supported (e.g. `2.5`)
* Real-time calculation
* Suitable for:

  * university grading
  * ear training exams
  * music theory exams
  * quizzes and assignments
  * custom grading systems

---

## Parameters

The tool accepts the following URL parameters:

| Parameter | Description                    |
| --------- | ------------------------------ |
| `min`     | Minimum possible score         |
| `max`     | Maximum possible score         |
| `pass`    | Minimum passing score          |
| `grades`  | Number of grades in the system |

---

## Example

```txt
?min=0&max=60&pass=30&grades=5
```

This means:

* Minimum score: `0`
* Maximum score: `60`
* Passing score: `30`
* Grade system: `1–5`

  * `1` = best
  * `5` = fail

---

## Example URL

```txt
https://yourusername.github.io/grading/?min=0&max=60&pass=30&grades=5
```

---

## Example Conversion

| Score | Grade |
| ----- | ----- |
| 28    | 5     |
| 30    | 4     |
| 37    | 3.5   |
| 43.5  | 2.5   |
| 52    | 1.5   |
| 60    | 1     |

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/grading.git
```

---

### 2. Rename the main file

Ensure the main page is called:

```txt
index.html
```

GitHub Pages expects this filename by default.

---

### 3. Enable GitHub Pages

Go to:

```txt
Settings → Pages
```

Then set:

* Source → `Deploy from a branch`
* Branch → `main`
* Folder → `/ (root)`

Save.

After a short deployment delay, the page will become available at:

```txt
https://yourusername.github.io/grading/
```

---

## Grade Calculation

The calculator:

1. Checks whether the score passes.
2. Maps the passing-to-maximum range linearly.
3. Converts the normalized value into grades.
4. Rounds to the nearest `0.5`.

---

## Customization

You can easily modify:

* grading direction
* rounding precision
* color themes
* integer-only grades
* percentage display
* keyboard shortcuts
* Austrian/German grading labels
* CSV export
* dark mode

---

## License

MIT License.
