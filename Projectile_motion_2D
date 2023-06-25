#Vertical projectile motion in 2D

def launch():
    print("Launching the projectile!")
    
newSphere = sphere(pos=vector(0,0.1,0), radius=0.05, color = color.red, make_trail=True, trail_type="points", interval=2, retain=10000, trail_color = color.white)
box(pos=vector(0,0,0), size=vector(1,0.01,.05), color=color.white)

v0 = 10
g = vector(0,-9.8,0)
t = 0
dt = 0.001
theta = 70*pi/180
newSphere.m = 0.2
r0=newSphere.pos

vx = [v0*cos(theta)]
vy = [v0*sin(theta)]
v = vector(vx,vy,0)
print(v)

newSphere.p=newSphere.m*v0*vector(cos(theta),sin(theta),0)
print(newSphere.p)
while newSphere.pos.y >= 0:
        rate(1000)
        Fnet=newSphere.m*g
        newSphere.p=newSphere.p+Fnet*dt
        newSphere.pos=newSphere.pos+newSphere.p*dt/newSphere.m
        t=t+dt

print("dr final = ",newSphere.pos-r0," m")
print("t final = ",t," s")


gd=graph(xtitle="Time [s]", ytitle="Vertical Position [m]")
f1=series()

m=.1 #kg
g=9.8 #N/kg

v0=4 #m/s

theta=90*pi/180

vy=v0*sin(theta) #m/s

y=0.8 #m
x=0 #m

t=0 #s
dt=0.01 #s

while t<5:
  #calculate the force
  Fnety=-m*g
  Fnetx=0
  #calculate the acceleration
  ay=Fnety/m
  ax=Fnetx/m
  
  #update velocity
  vy=vy+ay*dt
  
  #update position
  y=y+vy*dt
  
  #update time
  t=t+dt
