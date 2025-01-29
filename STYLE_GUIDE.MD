# Glossary Style Guide  

This guide ensures all glossary entries are clear, consistent, and easy to navigate.  

## Entry Structure  
1. **Term Title**: Use sentence case (e.g., "API", not "Api").  
2. **Definition**:  
   - 1–2 sentences. Avoid jargon unless defined elsewhere.  
   - Example:  
     ✅ "A set of protocols for software communication."  
     ❌ "APIs let apps talk to each other."  

3. **Real World Usage**:  
   - **Examples**: Code snippets, quotes, or use cases.  
     ```python
     # Good example
     response = requests.get("https://api.example.com/data")
     ```  
   - **Best Practices**: Bullet points with ✅ **Do** and ❌ **Avoid**.  

4. **Changelog**:  
   - Track major updates in a table. Minor fixes (e.g., typos) need not be logged.  

## Formatting  
- **Bold terms**: `**API**` on first mention.  
- **Links**: Use relative paths (e.g., `[SDK](../software/sdk.md)`).  
- **Code**: Wrap inline code in backticks (`` `GET /users` ``).  



---

## File Naming Rules
1. **Lowercase Letters**:  
   - ✅ `api.md`  
   - ❌ `API.md`  

2. **Hyphens for Spaces**:  
   - ✅ `version-control.md`  
   - ❌ `version control.md` or `versionControl.md`  

3. **Special Characters**:  
   - Replace `/` with hyphens: `ci-cd.md` (not `ci/cd.md`).  
   - Simplify phrases: `two-factor-auth.md` instead of `two-factor-authentication.md`.  

---

## Examples
| Term Name                   | Filename                     | Category Folder      |
|-----------------------------|------------------------------|----------------------|
| **API**                     | `api.md`                     | `software`           |
| **CI/CD**                   | `ci-cd.md`                   | `devops`             |
| **Version Control**         | `version-control.md`         | `software`           |
| **Two-Factor Authentication** | `two-factor-auth.md`      | `cybersecurity`      |
| **Kubernetes**              | `kubernetes.md`              | `devops`             |

---



## Tone & Voice  
- **Active voice**: "The API processes requests" (not "Requests are processed by the API").  
- **Audience**: Assume readers are technical writers or developers new to the term.  

## Metadata  
- **Categories**: Tag terms accurately (e.g., `devops`, `software`).  
- **Related terms**: Link to 2–3 relevant terms.  

## Need Help?  
Open an issue or ping a maintainer in your PR!  