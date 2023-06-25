#Simulating orbit of Earth around the Sun
sun = sphere(pos=vector(0,0,0), radius=0.1, color=color.orange, mass=1, velocity=vector(0,0,0), make_trail=True)

Earth = sphere(pos=vector(1,0,0), radius=0.05, color=color.cyan, velocity=vector(0,2*pi,0), make_trail=True)

dt = 0.001


def acceleration(p1,p2):

    G=4*pi**2

    r_vec = p1.pos - p2.pos

    r_mag = mag(r_vec)

    r_hat = r_vec/r_mag

    acceleration_magnitude = G/r_mag

    acceleration_vector = -acceleration_magnitude*r_hat

    return acceleration_vector



while(True):
	rate(500)

	Earth.acceleration = acceleration(Earth,sun)

	Earth.velocity = Earth.velocity + Earth.acceleration*dt

	Earth.pos = Earth.pos + Earth.velocity *dt  
