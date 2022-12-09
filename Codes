import customtkinter as ctk


class App():
    def __init__(self):
        self.root = ctk.CTk()
        self.root.geometry("300x180")
        self.root.title("Text Editor")
        self.mainframe = ctk.CTkFrame(master = self.root)
        self.mainframe.pack(pady=5 , padx= 5 ,fill="both" , expand="True")

        self.text = ctk.CTkLabel(master = self.mainframe , text = " Shervin" ,text_color="White" , font=("Calibri Light" , 18))
        self.text.grid(row=0 ,column=0)

        self.text_field = ctk.CTkEntry(master = self.mainframe)
        self.text_field.grid(row=1 , column=0 , pady= 5 ,padx=5, sticky="NWES")

        self.text_button = ctk.CTkButton(master = self.mainframe , text="Set Text" , command=self.set_text )
        self.text_button.grid(row=1 , pady=5 ,column=1 ,sticky="NWES")

        color_options = ["Blue" , "Red" , "Black" , "Purple" , "Pink" , "Teal"]
        self.set_color_field = ctk.CTkComboBox(self.mainframe , values=color_options)
        self.set_color_field.grid(row=2 , column=0 , sticky="NWES" , pady=10)
        self.set_color_button = ctk.CTkButton(self.mainframe , text="Set Color" , command=self.set_color)
        self.set_color_button.grid(row=2 , column=1 , pady=10)

        self.reverse_text = ctk.CTkButton(self.mainframe , text="Reverse Text" , command=self.reverse)
        self.reverse_text.grid(row=3 , column= 0 , sticky="NWES" , pady=10)

        self.root.mainloop()
        return


    def set_text(self):
        new_text = self.text_field.get()
        self.text.configure(text = new_text)


    def set_color(self):
        new_color = self.set_color_field.get()
        self.text.configure(text_color=new_color)


    def reverse(self):
        new_text= self.text.cget('text')
        reversed = new_text[::-1]
        self.text.configure(text=reversed)    


if __name__ == "__main__":
    App()
