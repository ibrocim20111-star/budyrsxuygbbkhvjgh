def foydalanuvchini_qoshish():
    ism = input("Ismingizni kiriting: ")
    yosh = input("Yoshingizni kiriting: ")
    qiziqish = input("Qiziqishingiz: ")
    
    profil = {
        "ism": ism.capitalize(),
        "yosh": yosh,
        "qiziqish": qiziqish.lower()
    }
    
    return profil

def profilni_chiqarish(user):
    print("\n--- Foydalanuvchi Profili ---")
    print(f"Ism: {user['ism']}")
    print(f"Yosh: {user['yosh']} yoshda")
    print(f"Qiziqishi: {user['qiziqish']}")
    
    if int(user['yosh']) < 18:
        print("Status: Yosh o'quvchi")
    else:
        print("Status: Tajribali foydalanuvchi")

if __name__ == "__main__":
    yangi_user = foydalanuvchini_qoshish()
    profilni_chiqarish(yangi_user)
