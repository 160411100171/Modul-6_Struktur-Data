# Modul-6_Struktur-Data
Searching

Searching - proses yang fundamental dalam pengolahan data yang menemukan data tertentu didalam sekumpulan data yang bertipe sama.
Searching algorithm adalah algoritma yang menerima sebuah argumen kunci dan dengan langkah-langkah tertentu akan mencari value dengan keys tersebut.

------------------------------------------------------------------------------------------------------------------
a=[12,5,9,8,1,10,26]
11 in a
Running: False
	12 in a
Running: True
	15 in a
Running: False

Sequential Search

teknik pencarian data dengan cara membandingkan data yang dicari dengan seluruh data yang terdapat pada kumpulan data secara satu persatu, dari data awal sampai data akhir.

Unordered List Sequential Search
Data berada pada keadaan acak, tidak terurut, sehingga pencarian harus dilakukan mulai dari indeks awal sampai indeks akhir data, atau pencarian berhenti ketika data sudah ditemukan.
def seqSearch(listData, data):
    ind = 0
    found = False
    while ind < len(listData) and not found:
        if listData[ind] == data:
            found = True
        else:
            ind = ind+1
    return found

a=[12,5,9,8,1,10,26]
print(seqSearch(a,1))


Ordered List Sequential Search

Data sudah dalam keadaan terurut, hal ini tentunya dapat mengurangi waktu komputasi pencarian.

def orderedSeqSearch(listData, data):
    ind = 0
    found = False
    stop = False
    position=[]
    while ind < len(listData) and not found and not stop:
        if listData[ind] == data:
            found = True
            position.append(ind)
        else:
            if listData[ind] > data:
                stop = True
            else:
                ind = ind+1
    
    if found:
        return ind
    else:
        return ('Data tidak ada')

a=[1,1,5,5,5,8,9,10,12,26]
ind=orderedSeqSearch(a,5)
print(ind)


------------------------------------------------------------------------------------------------------------------------------------------
