# Padhakutube Mock Test JSON Structure

Use this exact structure when extracting questions from PDF/HTML using ChatGPT. This ensures the app can read the data correctly.

### **JSON Format (Copy this for ChatGPT):**

```json
{
  "test_id": "unique_id_here",
  "title": "Test Title Here",
  "time_limit_minutes": 60,
  "questions": [
    {
      "id": 1,
      "section": "6", 
      "q_en": "Question in English",
      "q_hi": "सवालो का टेक्स्ट हिंदी में (Optional)",
      "options_en": ["Option A", "Option B", "Option C", "Option D"],
      "options_hi": ["विकल्प क", "विकल्प ख", "विकल्प ग", "विकल्प घ"],
      "correct_answer": "a", 
      "solution_en": "Solution explanation in English",
      "solution_hi": "समाधान हिंदी में"
    }
  ]
}
```

### **Section Mapping:**
- **6**: General Intelligence & Reasoning
- **18**: General Awareness (GK)
- **17**: Quantitative Aptitude (Maths)
- **7**: English Comprehension

---

### **ChatGPT Prompt to use:**
"I am providing a PDF/Text of a Mock Test. Please extract all questions into the provided JSON structure. 
1. Map sections as: Reasoning=6, GK=18, Maths=17, English=7.
2. Ensure `correct_answer` is a small letter 'a', 'b', 'c', or 'd'.
3. If Hindi text is missing, keep `q_hi` and `options_hi` empty strings.
4. Output only the final JSON array."
