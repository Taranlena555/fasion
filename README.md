# fasion
class Appointment:
    def __init__(self, date, time, service, customer_name):
        self.date = date
        self.time = time
        self.service = service
        self.customer_name = customer_name

class BeautySalon:
    def __init__(self):
        self.appointments = []

    def book_appointment(self, date, time, service, customer_name):
        appointment = Appointment(date, time, service, customer_name)
        self.appointments.append(appointment)
        print(f"Appointment booked for {customer_name} on {date} at {time} for {service}.")

    def display_appointments(self):
        if self.appointments:
            print("Scheduled Appointments:")
            for appointment in self.appointments:
                print(f"Date: {appointment.date}, Time: {appointment.time}, Service: {appointment.service}, Customer: {appointment.customer_name}")
        else:
            print("No appointments scheduled.")

# Example usage:
salon = BeautySalon()

salon.book_appointment("2024-04-01", "10:00 AM", "Haircut", "Alice")
salon.book_appointment("2024-04-02", "11:30 AM", "Manicure", "Bob")

salon.display_appointments()
