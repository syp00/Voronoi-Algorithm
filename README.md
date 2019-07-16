# Voronoi Algorithm
 이 코드는 픽셀을 선택한 후 각자 색상코드를 넣고, 그 외의 픽셀을 가장 가까운 선택된 픽셀의 색상으로 바꿔 이미지를 출력 및 저장한다.
## 랜덤 요소를 넣었을 때
![N|Solid](https://upload.wikimedia.org/wikipedia/commons/thumb/5/54/Euclidean_Voronoi_diagram.svg/220px-Euclidean_Voronoi_diagram.svg.png)

랜덤으로 픽셀과 RGB 컬러를 넣으면 위의 사진과 같이 결과물이 나온다. 랜덤요소를 넣기 위해서는 업로드한 코드에서
```python
  nx = [20, 40, 40, 40, 40, 60, 60, 60, 60, 80, 80, 120, 120, 140, 140, 140, 140, 160, 160, 160, 160, 180]
  ny = [50, 20, 40, 60, 80, 20, 40, 60, 80, 40, 60, 40, 60, 20, 40, 60, 80, 20, 40, 60, 80, 50]
  nr = [0, 43, 100, 232, 0, 45, 73, 65, 233, 112, 213, 0, 43, 100, 232, 0, 45, 73, 65, 233, 112, 213]
  nb = [45, 33, 0, 0, 0, 241, 155, 214, 12, 156, 222, 45, 33, 0, 0, 0, 241, 155, 214, 12, 156, 222]
  ng = [90, 43, 100, 232, 0,  100, 232, 0, 45, 73, 65, 90, 43, 100, 232, 0,  100, 232, 0, 45, 73, 65]
  
  num_cells = len(nx)
  
  if __name__== "__main__":
  generate_voronoi_diagram(200, 100)
```
을
```python
nx = []
  ny = []
  nr = []
  ng = []
  nb = []
  for i in range(num_cells):
    nx.append(random.randrange(imgx))
    ny.append(random.randrange(imgy))
    nr.append(random.randrange(256))
    ng.append(random.randrange(256))
    nb.append(random.randrange(256))
    
    if __name__== "__main__":
  generate_voronoi_diagram(200, 100, 5)
```
으로 교체하도록 한다.
 
 ## 선택된 픽셀과 색깔을 바꾸고 싶을 때
 ```python
  nx = [20, 40, 40, 40, 40, 60, 60, 60, 60, 80, 80, 120, 120, 140, 140, 140, 140, 160, 160, 160, 160, 180]
  ny = [50, 20, 40, 60, 80, 20, 40, 60, 80, 40, 60, 40, 60, 20, 40, 60, 80, 20, 40, 60, 80, 50]
  nr = [0, 43, 100, 232, 0, 45, 73, 65, 233, 112, 213, 0, 43, 100, 232, 0, 45, 73, 65, 233, 112, 213]
  nb = [45, 33, 0, 0, 0, 241, 155, 214, 12, 156, 222, 45, 33, 0, 0, 0, 241, 155, 214, 12, 156, 222]
  ng = [90, 43, 100, 232, 0,  100, 232, 0, 45, 73, 65, 90, 43, 100, 232, 0,  100, 232, 0, 45, 73, 65]
```
 위 List의 값을 변경한다. 리스트 안의 원소의 개수는 항상 같아야 한다.
