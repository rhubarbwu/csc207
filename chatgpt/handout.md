---
title: "**AI-Assisted Software Design Exercise**"
subtitle: "CSC207H1Y: Software Design (Summer 2023)"
author: "Prepared by [Robert Wu](https://www.cs.toronto.edu/~rupert) ([`rupert@cs.toronto.edu`](mailto:rupert@cs.toronto.edu))"
geometry: margin=.6in
header-includes:
  - \usepackage{fancyhdr}
  - \pagestyle{fancy}
  # - \setlength{\headheight}{30pt}
  # - \fancyhfoffset{2cm}
  - \lhead{AI-Assisted Software Design Exercise}
  - \rhead{CSC207H1Y -- Software Design (Summer 2023)}
linkcolor: purple
---

**Grade Weight**: 5% of overall course grade.

**Due Time:** August 6th, 2023 at 11:59PM (Eastern).

**Submission:** MarkUs ([`markus.teach.cs.toronto.edu/2023-05`](https://markus.teach.cs.toronto.edu/2023-05)).

**Collaboration:** Assignment is **individual** except for approved/appropriate Piazza threads.

---

There's no doubt that artificial intelligence (AI) has revolutionized the human experience, and software development is no exception. As we navigate the impact of ever-improving AI systems, it is important for us to be aware of their capabilities, limitations, and ethics. In this exercise, you will guide a large language model (LLM) chatbot, [OpenAI's ChatGPT](https://chat.openai.com), to assist in the design and implementation of a simple program. This will be an opportunity to apply your programming skills and learnings of software design in a modern and experiential way.

**PDF Version:** [`www.cs.toronto.edu/~rupert/207/chatgpt.pdf`](https://www.cs.toronto.edu/~rupert/207/chatgpt.pdf)

## Software and Language Model

In order to complete this assignment, you will need to use ChatGPT ([`chat.openai.com`](https://chat.openai.com)). If you do not already have an account, create one anyhow you like; you are encouraged to experiment with it before attempting this assignment. We will use the "Free Research Preview": (one of) the default model(s) based on GPT-3.5. **This means you should not be using any premium/reserved features such as GPT-4 or browsing**.

Additionally, you will need some way to export your conversation with ChatGPT. OpenAI does not currently provide a mechanism for this, and printing to HTML from your browser is unlikely to work. Here are suggestions:

- [**Save ChatGPT**](https://chrome.google.com/webstore/detail/save-chatgpt/iccmddoieihalmghkeocgmlpilhgnnfn) (Chromium-based such as Microsoft Edge, Brave, Opera, or Google Chrome)
- [**Superpower ChatGPT**](https://addons.mozilla.org/en-CA/firefox/addon/superpower-chatgpt/) (Mozilla Firefox).
- Alternatively (but not advised), you can copy-paste into text-to-PDF tools like [`pandoc`](https://pandoc.org/) or word-processing software such as Microsoft Word or Google Docs. Formatting will be up to you.

# Instructions

1. Start by identifying a program title. See the [**appendix**](#appendix-program-titles) for examples for inspiration; you can pick one from this list or propose your own. Your final program should be simple but satisfy the [**program requirements**](#program-requirements).
2. In a new conversation with ChatGPT, ask for a simple implementation. For example,

   ```txt
   Write a simple Java implementation of a determinant calculator.
   ```

3. Enter at least 20 [**additional prompts**](#additional-prompts) towards improving, documenting and helping you understand design choices in the code. Make note of the [**program requirements**](#program-requirements) below. Example: [**Determinant Calculator**](https://drive.google.com/file/d/1unVs3r0RF8tM5ug2PkQcwJ0FJnUOSfub/view?usp=sharing).
4. Concurrently with the previous step, maintain a codebase that compiles and runs the way you expect.
   - ChatGPT can output code snippets, but it is your responsibility to put it all together.
5. Once you are satisfied, document, compile, test, and submit!

Documentation and additional testing can be added anytime (even if only at the end), manually or with ChatGPT.

## Additional Prompts

You should ask ChatGPT to explain or refactor the code towards the [**program requirements**](#program-requirements). Throughout your conversation, your 20 or (likely) more prompts should include at least the following:

- Two prompts about use cases and/or user stories.
- Two prompts about program correctness and testing; consider some corner cases!
- One prompt about efficiency; keep in mind both memory and compute!
- Two prompts about modularity and extensibility; some/all of SOLID/CA will be relevant!
- Two additional prompts about SOLID.
- One additional prompt about CA.
- Two prompts about code smells.
- Two prompts about design patterns.
- One prompt about accessibility.
- One additional prompt about ethics.
- Two prompts to add new features/functionality.

You are free to make any additional prompts to meet the [**program requirements**](#program-requirements). These need not be in order; the sequence of questions should be very different for each student. There is no maximum but note [**context-length**](#context-length-and-long-range-dependencies).

## Program Requirements

Your final code should:

- Consist of (ideally) one or multiple source code (`*.java`) files.
- Ideally be less than $500$ lines of code (over all files, including documentation).
  - There is no strict minumum and it is not necessary to approach $500$ to receive full marks.
  - Submissions exceeding $1000$ (1K) lines (across all files) will be penalized.
- Exhibit at least two **design patterns**. $\dagger$
  - Any patterns discussed in lecture and the original _Design Patterns_ book (Gamma, Helm, Johnson, and Vlissides, 1995) can be used without citation.
  - More modern patterns that are _reasonably recognized_ can be used with citation; consult with the instructor or TAs if you are not sure.
- Adhere to **SOLID** and **Clean Architecture (CA)** principles and avoid **code smells**. $\dagger$
- Include a suite of reasonable unit tests, covering some corner cases.
- Be well documented with light **Java Docs** and a small but adequate amount of internal documentation.

If you have concerns about any of the above (especially $\dagger$), consult the instructor or a TA.

### Advice on Complexity

- **Start simple!** You can always extend your code later. For example, most of the programs in the [**appendix**](#appendix-program-titles) can be augmented with reading from/writing to files.
- Avoid explicitly supporting a graphical interface. Instead, limit your program to the command-line while being partially extensible to a future GUI. This is just advice, so you will not be penalized if you incorporate a GUI.
- If you are not sure that your program title is appropriate, ask on Piazza or in office hours.

### Note on Academic Integrity

This assignment is individual. Submissions with similar programs will be subject to more scrutiny, so try your best to pick/develop programs that are distinct from your peers'. With that said, you are free to discuss your ChatGPT conversations with classmates provided what you ultimately submit cites your sources and is otherwise your own work.

# More About ChatGPT

If anything ChatGPT writes doesn't make sense to you, you can use conventional resources (such as StackOverflow) to help you understand. Sometimes, you can/should instead question ChatGPT to provide explanations (based on the expertise of the vast number of developers on the internet over many years).

## Correctness and Limitations

LLMs aren't perfect, and have limitations stemming from their architecture/capacity and the data they were trained on. You should expect ChatGPT to sometimes provide incorrect information or nonsensical explanations/logic. The upside is you can demonstrate your knowledge and design skills by checking ChatGPT's work. If its responses do not make sense to you or otherwise seem suspicious, you are encouraged to question/correct it.

But do not overcorrect! By the same token, ChatGPT might believe anything false or nonsensical you prompt it with. Therefore, you should check your understanding with the course materials and in office hours. You might find some internet resources helpful here, but be skeptical all the same and cite your sources.

\vspace{-0.2cm}

### Timeliness and Training

ChatGPT (static GPT-3.5) was pre-trained on data available on the internet at some point in 2021. This means you should not rely on ChatGPT to have more recent knowledge. Additionally, the coherence of ChatGPT's responses with all real-world information depends on how visible/accurate said information was in the first place.

\vspace{-0.2cm}

### Context Length and Long-Range Dependencies

Furthermore, LLMs currently have trouble scaling to long sequence lengths (this is a deep learning thing; do not worry about it!). Most widely available models can only handle sequences up to a few thousand tokens/words before accuracy or coherence deteriorate. Therefore, if you find that ChatGPT starts struggling with long-term memory, it might be an indication that your program is too complex or the conversation has become too long/messy. It is okay to (re)start with a clean slate and/or new program for your "final draft".

## Concerns about ChatGPT

If you have concerns about or objections to using ChatGPT, please [**contact the course team**](mailto:csc207-2023-05@cs.toronto.edu). You can also ask questions in office hours or on [**Piazza**](https://piazza.com/class/lhezn6infr55th). We can try arranging alternatives, but note that ChatGPT was in the approved syllabus.

# Deliverables and Submission

Upload the following to MarkUs: [`markus.teach.cs.toronto.edu/2023-05`](https://markus.teach.cs.toronto.edu/2023-05).

1. Documented and tested Java code that compiles without errors.
2. Any other code that is required to compile or run your program.
3. PDF export of your conversation with ChatGPT using some [**software tool**](#software-and-language-model).
4. README **briefly** summarizing the program, with use cases, user story, and design patterns.

   - Include which version of Java and what testing framework you used.
   - Briefly explain remaining code smells and violations of SOLID or CA; if there are none, state so.
   - Keep this brief as the conversation log will tell most of the story.

## Grading Rubric

Code that does not compile or run will receive a grade of $0$.

| Criteria                                | Points |
| --------------------------------------- | ------ |
| length (<1K lines)                      | 1      |
| documentation $*$                       | 1      |
| testing $*$                             | 1      |
| design patterns (2)                     | 2      |
| SOLID compliance $\dagger$              | 1      |
| Clean Architecture compliance $\dagger$ | 1      |
| avoid code smells $\dagger$             | 1      |
| additional prompts (see above)          | 20     |
| **total**                               | 28     |

\vspace{-0.2cm}

$*$ coverage doesn't have to be full; just add a little bit.

$\dagger$ compliance should be best-effort and remaining violations briefly explained.

---

# Appendix: Program Titles

Here are some example programs that aim to both inspire and give you an idea of the expected complexity. You can combine multiple ideas if that makes sense (for example, solvers for generators or games). Feel free to suggest more to your classmates or propose your own as follow-ups on [**Piazza**](https://piazza.com/class/lhezn6infr55th/post/109).

1. Calculator: domain-specific, general-purpose, scientific, statistical, area/volume, dates.
2. Games: Hangman, number guessing, Tic-Tac-Toe, rock-paper-scissors, chess/checkers, Snake, Sudoku, puzzles.
3. Converter: number systems (binary, octal, decimal, hexadecimal), measurement (temperature, mass, weight, length, energy), currency, morse code.
4. Generator: passwords, hashing, fibonnaci series/spiral, permutations/combinations/power sets, ASCII art, QR codes, fractals, Mandelbrot set, mazes.
5. Validator: prime numbers, palindromic strings, hashing.
6. Solvers: quadratic/polynomial equations, mazes, Tower of Hanoi, Sudoku, puzzle games or riddles.
7. Accounting: bank accounts, academic records.
8. Search: linear, binary.
9. Sorting: bubble, insertion, merge, quick, selection.
10. Data Structures: binary (search/heap) trees, hash tables.
11. Manager: files, passwords, accounts/profiles.
12. Simulators: dice, Enigma machine, elevators.
13. Files: search, manager, text editor, word/line counter, image viewer.

Your final submission should be very unique so it helps if your idea is distinct from your peers. If you're concerned about [**academic integrity**](#note-on-academic-integrity), roll some dice to pick something random or come up an original idea.
