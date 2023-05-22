# perfectcircle.py
Perfect circle 99.5%
Нарисовать идеальный круг на платформе [neal.fun](https://neal.fun) с точностью на 99.5%

### Перед тем как начать, нужно: 📚
- Скачать последнюю версию Python ([https://python.org](https://python.org))
 - Загрузить Pyautogui (Для того чтобы загрузить Pyautogui, введите `pip install pyautogui` или `pip3 install pyautogui`)
 
- ### Шаги 📜
- Откройте командную строку в Python 
- Введите данный код:
import pyautogui
import math
import time
SPEED = 3
RADIUS = 494
X_OFFSET = 0
Y_OFFSET = 0

def getX(t, rad):
    return ((pyautogui.size()[0] / 2) + math.cos(t) * rad) + Y_OFFSET

def getY(t, rad):
    return ((pyautogui.size()[1] / 2) + math.sin(t) * rad) + X_OFFSET

print('\n--> Place your cursor on the website while on fullscreen.\n\n(Ctrl+C to stop)\n')
try:
    time.sleep(3)
    for i in range(5):
        print(str(5 - i) + ' seconds left.')
        time.sleep(1)
except KeyboardInterrupt:
    print('Aborted.')
    exit()

pyautogui.moveTo(getX(0, RADIUS), getY(0, RADIUS))
pyautogui.mouseDown(button="left")
for i in range(SPEED + 2):
    t = i * math.pi / (SPEED / 2)
    pyautogui.moveTo(getX(t, RADIUS), getY(t, RADIUS), duration=0)
pyautogui.mouseUp(button='left')

- Затем откройте [https://neal.fun/perfect-circle/](https://neal.fun/perfect-circle/) в новой вкладке на большом экране
- Запустите команду и вернитесь на экран браузера (neal fun)!Не забудьте открыть его на полный экран!
- Подождите 5 секунд.
