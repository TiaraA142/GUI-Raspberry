from tkinter import * 					# imports the Tkinter lib
root = Tk()								# create the root object
root.wm_title("AOITS")					# sets title of the window
root.configure(bg="#8080FF")			# change the background color 
root.attributes("-fullscreen", True) 	# set to fullscreen

#update the text in the label_1
def saldo():
	label_1 ["text"] = "Selamat Datang" 	
	label_2 ["text"] = "TIARA ASA" 			#+name.get() +"4 L"
	label_3 ["text"] = "Saldo"
	label_4 ["text"] = "Rp128.122,45"
	label_5 ["text"] = "Sisa Subsidi"
	label_6 ["text"] = "23 Liter"


# we can exit when we press the escape key
def end_fullscreen(event):
	root.attributes("-fullscreen", False)

name = StringVar() 						#store a string from the Entry widget input

label_1 = Label(root, text="Silahkan", font="Poppins 26",
			fg="#000",
			bg="#8080FF")
label_2 = Label(root, text="TAP KARTU", height=20,
			fg="#000",
			bg="#8080FF")
label_3 = Label(root, text=" ", height=20,
			fg="#000",
			bg="#8080FF")
label_4 = Label(root, text=" ", height=20,
			fg="#000",
			bg="#8080FF")
label_5 = Label(root, text=" ", height=20,
			fg="#000",
			bg="#8080FF")
label_6 = Label(root, text=" ", height=20,
			fg="#000",
			bg="#8080FF")
#entry_1 = Entry(root, textvariable = name)

Button = Button(root, text="Next", command = saldo) #Add a button inside the window


label_1.grid(row=2, column=2)
label_2.grid(row=3, column=2)
label_3.grid(row=5, column=2)
label_4.grid(row=6, column=2)
label_5.grid(row=7, column=2)
label_6.grid(row=8, column=2)

Button.grid(row=2, column=1)
#Button2.grid(row=2, column=3)

root.bind("<Escape>", end_fullscreen)
root.mainloop()				# starts the GUI loop
