# my-dream-1stimport calendar
import tkinter as tk
from tkinter import ttk

def show_calendar():
    year = int(year_entry.get())
    cal_text.delete('1.0', tk.END)  # পুরাতন লেখা মুছে ফেলো
    cal_data = calendar.calendar(year)
    cal_text.insert(tk.END, cal_data)

# GUI window তৈরি করো
root = tk.Tk()
root.title("পাইথন ক্যালেন্ডার")
root.geometry("600x600")

# Label ও Entry
year_label = ttk.Label(root, text="যে বছর দেখতে চাও:", font=("Helvetica", 14))
year_label.pack(pady=10)

year_entry = ttk.Entry(root, font=("Helvetica", 14))
year_entry.pack(pady=5)

# Button
show_button = ttk.Button(root, text="ক্যালেন্ডার দেখাও", command=show_calendar)
show_button.pack(pady=10)

# Text area
cal_text = tk.Text(root, font=("Consolas", 10), wrap=tk.NONE)
cal_text.pack(expand=True, fill='both', padx=10, pady=10)

# চালু করো
root.mainloop()
