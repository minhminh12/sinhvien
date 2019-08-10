lop = []
print("please choose\n"
      "1: enter student information\n"
      "2: enter more student\n"
      "3: edit student information\n"
      "4: detele student\n")
choose = input("nhap:")
choose = int(choose)
if choose==1:
    print("enter student information")
    numerical_order = input("enter numerical order")
    name= input("enter name:")
    age= input("enter age:")
    sex= input("enter sex:")
    phone_number= input("enter phone number:")
    address= input("enter address:")
    student = {numerical_order:{"name":name,
                                "age":age,
                                "sex":sex,
                                "phone number":phone_number,
                                "address":address},}
    print(student)
    lop.append(student)
elif choose==2:
    print("enter student information")
    numerical_order= input("enter numerical order")
    numerical_order= int(numerical_order)
    numerical_order= numerical_order - 1
    name= input("enter name:")
    age= input("enter age:")
    sex= input("enter sex:")
    phone_number= input("enter phone number:")
    address= input("enter address:")
    student[numerical_order] =[{"name":name,
                                "age":age,
                                "sex":sex,
                                "phone number":phone_number,
                                "address":address}]
    print(student[numerical_order])
    lop.append(student)
elif choose==3:
    print("edit student information:")
    numerical_order = input("enter numerical order")
    numerical_order = int(numerical_order)
    numerical_order = numerical_order - 1
    print(student[mumerical_order])
    print("please choose"
          "1: fix name\n"
          "2: fix age\n"
          "3: fix sex\n"
          "4: fix phone number\n"
          "5: fix address\n")
    choose1 = input("please choose")
    choose1 = int(choose1)
    if choose1==1:
        name = input("please enter name")
        student[numerical_order][name] = name
    elif choose1==2:
        age = input("please enter age")
        student[numerical_order][age] = age
    elif choose1==3:
        sex = input("please enter sex")
        student[numerical_order][sex] = sex
    elif choose1==4:
        phone_number = input("please enter phone number")
        student[numerical_order][phone_number] = phone_number
    elif choose1==5:
        address = input("please enter address")
        student[numerical_order][address] = address
    else :
        print("erro")
elif choose==4:
    print("detele student")
    numerical_order = input("please enter student detele")
    del student[numerical_order]
else :
    print("erro")
