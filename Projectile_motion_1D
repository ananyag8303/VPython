#Part 1
newSphere = sphere(pos=vector(0,10,0), radius=0.1, color = color.red,make_trail=True, trail_type="points",
              interval=0.5, retain=100, trail_color = color.white)
box(pos=vector(0,-0.4,0), size=vector(1,.05,.05), color=color.white)
scene.center = vector(0,5,0)
scene.width = 400
time = 0
g = 9.8
dt = 0.01
#Having a small dt ensures the truncation error doesnt happen
vy = 0
y = 10
t = 0
while y > 0:
        rate(30)
        ay = -g
        y += vy * dt    # use old vy to calculate new y
        vy += ay * dt   # use old ay to calculate new vy
        newSphere.pos = vector(0, y, 0)
        time += dt
        
print("Ball lands at t =", time, "seconds, with velocity", vy, "m/s")


v = -sqrt(20*g)
t = v/(-g)
print("Accordring to calculations, the final velocity should be", v,"m/s") 
print("Accordring to calculations, the final time should be", t,"s")
