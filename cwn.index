import tkinter as tk
import datetime

def get_current_week_number():
    current_date = datetime.date.today()
    week_number = current_date.strftime("%V")
    return int(week_number)

class WeekNumberWidget(tk.Tk):
    def __init__(self):
        super().__init__()

        self.title("Week Number Widget")
        self.geometry("300x100")

        self.label = tk.Label(self, text="Current Week Number:")
        self.label.pack(pady=10)

        self.week_number_var = tk.StringVar()
        self.week_number_label = tk.Label(self, textvariable=self.week_number_var, font=("Helvetica", 18))
        self.week_number_label.pack()

        self.update_week_number()

    def update_week_number(self):
        current_week_number = get_current_week_number()
        self.week_number_var.set(str(current_week_number))
        self.after(1000, self.update_week_number)

if __name__ == "__main__":
    app = WeekNumberWidget()
    app.mainloop()
