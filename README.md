# XỬ LÝ SỐ LIỆU THÔNG KÊKÊ

## 1. **Mục tiêu của project:**

## **2. Cài Đặt LaTeX Workshop Trên VSCode**

Ta sẽ cần phải cài đặt các phần sau:
1. VsCode
2. WSL
3. Remote window

### 🔧 Bước 1: Cài đặt công cụ biên dịch LaTeX
- **Windows:** Cài [MiKTeX](https://miktex.org/download)
- **macOS:** Cài [MacTeX](https://tug.org/mactex/)

- **Linux (Ubuntu/Debian/WSL):**

```bash
sudo apt update
sudo apt install texlive-bibtex-extra chktex latexmk texlive-lang-other texlive-science texlive-xetex texlive-luatex texlive-fonts-recommended 
```

### 🧩 Bước 2: Cài đặt tiện ích mở rộng **LaTeX Workshop**

1. Mở VSCode → nhấn `Ctrl + Shift + X` để mở tab Extensions
2. Gõ **LaTeX Workshop**
3. Nhấn **Install**

 Inside Vscode, hold ctrl shift P -> Open user settings (Json), then modify your settings.json files into this:

```bash
{
    "git.autofetch": true,
    "git.enableSmartCommit": true,
    "git.confirmSync": false,

    "latex-workshop.latex.tools": [
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "%DOC%"
            ]
        },
        {
            "name": "xelatexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-xelatex",
                "%DOC%"
            ]
        },
        {
            "name": "lualatexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-lualatex",
                "%DOC%"
            ]
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": ["%DOCFILE%"]
        }
    ],

    "latex-workshop.latex.recipes": [
        {
            "name": "latexmk (xelatex)",
            "tools": ["xelatexmk"]
        },
        {
            "name": "xelatexmk -> bibtex -> xelatexmk * 2",
            "tools": [
                "xelatexmk",
                "bibtex",
                "xelatexmk",
                "xelatexmk"
            ]
        }
    ],

    "latex-workshop.latex.recipe.default": "latexmk (xelatex)",
    "latex-workshop.latex.clean.fileTypes": [
        "*.aux", "*.bbl", "*.blg", "*.idx", "*.ind", "*.lof",
        "*.lot", "*.out", "*.toc", "*.acn", "*.acr", "*.alg",
        "*.glg", "*.glo", "*.gls", "*.fls", "*.log", "*.fdb_latexmk"
    ],
    "latex-workshop.latex.autoBuild.run": "onSave",
    "explorer.confirmDelete": false
}

```


### 📂 Bước 3: clone repo này về thư mục làm việc

1. Tạo một thư mục để làm việc, sau đó dùng git clone để clone về
2. Trong đó, tạo file `main.tex`
3. Dán đoạn mã mẫu sau để kiểm tra:

   ```latex
   \documentclass{article}
   \begin{document}
   Hello LaTeX!  
   \LaTeX\ is working perfectly.
   \end{document}
   ```

4. Nhấn **Ctrl + Alt + B** (hoặc nhấn biểu tượng “Build LaTeX project” ở thanh công cụ) để biên dịch thành file PDF.






