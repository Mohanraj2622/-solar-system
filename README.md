class CelestialBody:
    def __init__(self, name, mass, radius):
        self.name = name
        self.mass = mass  # in kilograms
        self.radius = radius  # in meters

class SolarSystem:
    def __init__(self):
        self.bodies = []

    def add_body(self, body):
        self.bodies.append(body)

    def get_body(self, name):
        for body in self.bodies:
            if body.name == name:
                return body
        return None

# Define some celestial bodies
sun = CelestialBody("Sun", 1.989e30, 6.957e8)
earth = CelestialBody("Earth", 5.972e24, 6.371e6)
moon = CelestialBody("Moon", 7.34767309e22, 1.737e6)

# Create a solar system and add the bodies
solar_system = SolarSystem()
solar_system.add_body(sun)
solar_system.add_body(earth)
solar_system.add_body(moon)

# Example usage
print("Solar System Bodies:")
for body in solar_system.bodies:
    print(f"Name: {body.name}, Mass: {body.mass} kg, Radius: {body.radius} m")
