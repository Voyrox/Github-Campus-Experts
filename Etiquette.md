# ✨ Code Etiquette: Writing Clean, Readable, and Maintainable Code

Code etiquette is about more than just making your code work — it’s about making your code **understandable**, **collaborative**, and **maintainable**. Whether you're working alone or in a team, good code etiquette ensures that your code can be reviewed, reused, and refined with ease.

---

## 🧠 Why Code Etiquette Matters

- 💬 **Improves readability**: Your code becomes easier for others (and future you) to understand.
- 🔄 **Simplifies collaboration**: Clean code is easier to review and merge in team environments.
- 🧹 **Reduces bugs**: Clear structure and naming prevent logic errors.
- 🏗️ **Encourages scalability**: Well-structured code can be built upon without rewrites.

---

## 📐 Key Principles of Code Etiquette

### ✅ Use Meaningful Names

Avoid vague names like `x`, `temp`, or `foo`. Instead, choose names that describe the variable or function’s purpose.

```java
// Bad
int x = 25;

// Good
int studentAge = 25;
```

---

### ✅ Keep Functions Short and Focused

Each function should do **one thing** and do it well.

```java
// Bad
public void processStudent() {
  // reads file
  // parses data
  // sends email
}

// Good
public void readStudentData() { ... }
public void parseStudentData() { ... }
public void sendEmailToStudent() { ... }
```

---

### ✅ Follow Consistent Formatting

Use indentation and spacing properly. Set up a linter or formatter to keep your style consistent.

```java
// Bad
if(x>10){System.out.println("High");}

// Good
if (x > 10) {
  System.out.println("High");
}
```

---

### ✅ Avoid Deep Nesting

Nested blocks make your code harder to read. Prefer **early returns** or logical separation.

```java
// Bad
if (user != null) {
  if (user.isActive()) {
    if (!user.isBanned()) {
      // do something
    }
  }
}

// Good
if (user == null || !user.isActive() || user.isBanned()) return;
// do something
```

---

### ✅ Use Comments Wisely

- ❌ Don't comment *what* the code does if it's obvious
- ✅ Do comment *why* something is done or document edge cases

```java
// Bad
i++; // increment i

// Good
i++; // Move to the next record in the list
```

---

### ✅ Remove Dead Code

Old code, commented-out logic, and unused variables should be removed before committing.

```java
// Bad
// int temp = 0; // left from debugging

// Good
// Clean, production-ready code with no leftovers
```

---

### ✅ Don’t Repeat Yourself (DRY)

If you see repeated code, extract it into a function or loop.

```java
// Bad
sendWelcomeEmail();
sendWelcomeSMS();
sendWelcomePush();

// Good
sendWelcomeMessage("email");
sendWelcomeMessage("sms");
sendWelcomeMessage("push");
```

---

### ✅ Respect File and Folder Structure

Organize your code by feature, not by type (when possible). Use consistent naming.

```bash
# Bad
src/
  - file1.java
  - file2.java

# Good
src/
  student/
    - Student.java
    - StudentService.java
  utils/
    - DateFormatter.java
```

---

## 🧪 Etiquette Exercise

Here’s a short code cleanup task:

```java
// Before
public class t {
  public static void M(String[] a) {
    int x=10;
    if(x>5){
      if(x<15){
        System.out.println("ok");
      }
    }
  }
}

// After (apply etiquette principles)
public class TemperatureChecker {
  public static void main(String[] args) {
    int temperature = 10;

    if (temperature > 5 && temperature < 15) {
      System.out.println("ok");
    }
  }
}
```

---

## 📋 Commit Message Etiquette

Follow this format for better history readability:

```
feat: add login button to header
fix: correct loop condition for attendance counter
docs: update README with setup instructions
refactor: clean up StudentParser class
```

Avoid vague messages like `fix bug`, `oops`, or `final version`.

---

## 📚 Resources
- [GitHub Commit Message Guidelines](https://www.conventionalcommits.org/)
