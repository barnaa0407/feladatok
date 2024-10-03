#1

while True:
    try:
        diakok = []
        hanydiak = int(input("Hány diákot szeretnél hozzáadni? "))
        if type(hanydiak) == int:
            break
    except:
        print("Rossz input.")
        
    
for i in range(hanydiak):
    nev = input(f"Add meg az {i + 1}. diák nevét: ")
    jegy = int(input(f"Add meg {nev} jegyét: "))
    diakok.append((nev, jegy))

#2
    
if input("Szeretnéd látni az összes diákot? (igen/nem): ").strip().lower() == "igen":
    print("\nDiákok:")
    print("Név       | Jegy")
    print("----------------")
    for nev, jegy in diakok:
        print(f"{nev:<10} | {jegy}")

#3
if input("Szeretnéd tudni az átlagos jegyet? (igen/nem): ").strip().lower() == "igen":
    atlag = sum(jegy for _, jegy in diakok) / len(diakok)
    print(f"Az átlagos jegy: {atlag:.1f}")

#4
if input("Szeretnéd tudni a legmagasabb és legalacsonyabb jegyet? (igen/nem): ").strip().lower() == "igen":
    legmagasabb = max(jegy for _, jegy in diakok)
    legalacsonyabb = min(jegy for _, jegy in diakok)
    print(f"Legmagasabb jegy: {legmagasabb}")
    print(f"Legalacsonyabb jegy: {legalacsonyabb}")

#5
if input("Szeretnél eltávolítani egy diákot? (igen/nem): ").strip().lower() == "igen":
    eltavolitando = input("Add meg a diák nevét, akit el szeretnél távolítani: ")
    diakok = [diak for diak in diakok if diak[0] != eltavolitando]
    print(f"{eltavolitando} eltávolítva.")

#diakok kiirasa
if input("Szeretnéd látni az összes diákot? (igen/nem): ").strip().lower() == "igen":
    print("\nDiákok:")
    print("Név       | Jegy")
    print("----------------")
    for nev, jegy in diakok:
        print(f"{nev:<10} | {jegy}")
                
