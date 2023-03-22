# pythonProject33


import socket

socket = socket.socket()

socket.connect(("172.30.230.69", 1337))

txt = input("what you want to say?")

while txt != "exit":
    send = socket.send(txt.encode())
    rec = socket.recv(1024).decode()
    print(rec)
    print(send)
    txt = input("say somthing")

    #print(input("plese say somthing"))

socket.close()

