# 🔗 Link Cleaner Tool  

A lightweight Python script to clean and extract URLs from raw logs or messy text. Removes failed entries, extracts valid links, and outputs a clean list.  

---

## 🚀 Features  
- **Removes junk text**: Filters out `"Failed creating"` entries.  
- **Extracts URLs**: Cleans lines with `"Successfully created and pinged"`.  
- **Trims metadata**: Cuts off anything after `" : "` in remaining lines.  
- **Preserves direct links**: Leaves well-formed URLs unchanged.  
- **Simple GUI**: Built with IPython widgets for ease of use.  

---

## 🛠️ Usage  

### **Method 1: Jupyter Notebook**  
1. Paste raw links/logs into the input box.  
2. Click **"Process Links"**.  
3. Copy the cleaned URLs from the output.  

### **Method 2: Standalone Script**  
Replace the `input_area` value in the script with your text and run:  
```python
# Example hardcoded input (alternative to GUI)
input_text = """
https://good.link : Successfully created
https://bad.link : Failed creating
"""

# Clone the repository (if hosted on GitHub)
git clone https://github.com/yourusername/link-cleaner-tool.git
cd link-cleaner-tool

# Install dependencies (only ipywidgets needed)
pip install ipywidgets

# Launch Jupyter Notebook
jupyter notebook
```
## 🔄 Example

### Input:
https://example.com : Successfully created and pinged  
https://broken.link : Failed creating  
http://direct-url.com  
https://needs-cleaning.com : Extra metadata here  

### Output:
https://example.com  
http://direct-url.com  
https://needs-cleaning.com  

## 🤔 Why Use This?

🕒 Saves time: Automatically cleans hundreds of links in seconds.

🔧 No manual work: Removes the need for regex or text editing.

📦 Lightweight: Single script with zero bloat.

🔄 Reusable: Works with logs, APIs, scraped data, and more.
