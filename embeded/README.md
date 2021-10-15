# embeded
## STM32
### NUCLEO-F031K6
* https://github.com/stm32duino/Arduino_Core_STM32
* https://docs.platformio.org/en/latest/boards/ststm32/nucleo_f031k6.html
* https://www.st.com/en/evaluation-tools/nucleo-f031k6.html
* https://docs.platformio.org/en/latest/platforms/ststm32.html

#### Arduino framework
* https://github.com/platformio/platform-ststm32/tree/master/examples

##### SystemClock_Config 버그
Arduino framework 에 내장된 `SystemClock_Config` 함수를 사용하면 에러가 발생한다.
NUCLEO-F031K6 에 맞지 않는 Clock 설정을 하는 것으로 추정된다.

Arduino framework 에 내장된 `SystemClock_Config` 는 `WEAK` 로 설정되어 있기 때문에,
`void SystemClock_Config(void) { }` 를 소스에 추가하는 것만으로 문제가 해결된다.

##### Unit Test
* https://docs.platformio.org/en/latest/tutorials/core/unit_testing_blink.html

#### STM32Cube HAL framework
* https://docs.platformio.org/en/latest/tutorials/ststm32/stm32cube_debugging_unit_testing.html
