a = [
    [1,1,1,1,1,1,1,1,1,1],
    [1,0,1,0,1,1,1,1,1,1],
    [1,0,1,0,1,0,0,0,0,1],
    [1,0,1,0,1,1,1,1,0,1],
    [1,0,1,0,0,0,1,1,0,1],
    [1,0,1,0,0,0,1,1,0,1],
    [1,0,0,0,0,0,1,1,0,1],
    [1,0,1,0,0,0,1,1,0,1],
    [1,0,1,0,0,0,0,0,0,1],
    [1,1,1,1,1,1,1,1,1,1],
]

start = 1, 1
end = 2, 5

m = []
for i in range (len(a)):
    #print(a[i])
    m.append([])
    for j in range(len(a[i])):
        m[-1].append(0)
i,j = start
m[i][j] = 1

def make_step(k):
  for i in range(len(m)):
    for j in range(len(m[i])):
      if m[i][j] == k:
        if i>0 and m[i-1][j] == 0 and a[i-1][j] == 0:
          m[i-1][j] = k + 1
        if j>0 and m[i][j-1] == 0 and a[i][j-1] == 0:
          m[i][j-1] = k + 1
        if i<len(m)-1 and m[i+1][j] == 0 and a[i+1][j] == 0:
          m[i+1][j] = k + 1
        if j<len(m[i])-1 and m[i][j+1] == 0 and a[i][j+1] == 0:
           m[i][j+1] = k + 1

# make_step(1)
# make_step(2)
# make_step(3)
# make_step(4)
# make_step(5)
# make_step(6)
# make_step(7)
# make_step(8)
#
# for i in range (len(m)):
#     print(m[i])

k = 0
while m[end[0]][end[1]] == 0:
    k += 1
    make_step(k)

for i in range (len(m)):
     print(m[i])

i, j = end
k = m[i][j]
the_path = [(i,j)]
while k > 1:
  if i > 0 and m[i - 1][j] == k-1:
    i, j = i-1, j
    the_path.append((i, j))
    k-=1
  elif j > 0 and m[i][j - 1] == k-1:
    i, j = i, j-1
    the_path.append((i, j))
    k-=1
  elif i < len(m) - 1 and m[i + 1][j] == k-1:
    i, j = i+1, j
    the_path.append((i, j))
    k-=1
  elif j < len(m[i]) - 1 and m[i][j + 1] == k-1:
    i, j = i, j+1
    the_path.append((i, j))
    k -= 1

print(the_path)
