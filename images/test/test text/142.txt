from virtual_plotting import Triangle

class StepperMotor:
    def __init__(self):
        self.mode = 'virtual mode'
        self.triangle = Triangle()

    def setAngle(self, angle):
        # print('inner angle on inner motor is set to: ' + str(angle))
        pass

    def plot(self, inner_angle, pen):
        x , y= pen.get_current_position()
        self.triangle.set_alfa(inner_angle)
        self.triangle.find_coordinates( pen, (x,y))
        self.triangle.plot()
