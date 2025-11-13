import serial
import time

# Настройка последовательного порта
ser = serial.Serial('/dev/ttyACM0', 9600, timeout=1)  # Укажите порт Arduino
ser.flush()

def send_message(message):
    ser.write(f"{message}\n".encode())  # Отправляем сообщение
    print(f"Sent: {message}")

try:
    while True:
        send_message(1)  # Отправляем 1
        time.sleep(2)    # Ждем 2 секунды
        send_message(2)  # Отправляем 2
        time.sleep(2)    # Ждем 2 секунды
except KeyboardInterrupt:
    print("Программа остановлена")
finally:
    ser.close()  # Закрываем порт
