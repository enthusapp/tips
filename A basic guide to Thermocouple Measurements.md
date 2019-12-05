http://www.ti.com/lit/an/sbaa274/sbaa274.pdf

# Thermocouple Overview
열전대(Thermocouple) 은 온도변화에 따라 전압 발생시키는 온도 측정 센서입니다.
열전대는 다른 금속으로 구성된 두개의 전선 가닥으로 구성됩니다.
두 전선 가닥은 용접되어 하나의 접점을 만듭니다.
온도 변화에 따라 접점에서 전압이 발생합니다.

다른 금속의 조합은 다양한 전압 응답을 만들어냅니다.
측정 온도 범위와 정확도에 맞게 금속 조합에 결정됩니다.
또한 지속성, 사용 환경 그리고 수명을 고려하여 결정됩니다.

## Seebeck Voltage
1820 년, Thomas Hohann Seebeck 은 긴 금속이 데워질때 양단에 전압이 발생하는 것을 발견했습니다.
전압은 온도와 어떤 금속을 사용하는지에 따라 달라졌습니다.
다른 금속의 결합은 다른 Seebeck 전압, 즉 열전대 전압 Vtc 을 발생시킵니다.

열전대를 발생시키는 온도를 Ttc 로 두 금속 접점의 온도입니다.
두 금속의 Vtc 가 측정되는 위치의 온도를 Tcj 로 기준 온도라고 부릅니다.
측정 위치는 등온선 영역(isothtermal block) 이라고 부릅니다.

열전대와 등온선 영역의 연결은 온도 측정에 중요한 요소입니다.
정확한 열전대 측정을 위해서는 열전대에서 돌아오는 지점의 온도는 반드시 같아야 하기 때문입니다.

어떤 형태의 다른 금속의 연결도 열전대를 발생시키기 때문에,
열전대에서 ADC 까지의 연결은 반드시 단순해야 하고 대칭성을 유지해야 합니다.
다른 어떠한 추가적인 접점도 측정오류를 발생시킵니다.

열전대 신호가 ADC 까지 연결되기까지의 각 과정에서 어쩔수 없이 더해지는 열전대 접점들이 있다는 점을 반드시 고려해야 합니다.
즉 연결 커넥터, solder, copper, IC pin, bond wire, chip contact 등은 모두 추가되는 접점입니다.
하지만 차등 신호를 이용할때 다른 접점들의 온도가 동일하다면, 추가된 접점에서 발생하는 열전대는 제거되고 측정에 영향을 주지 않습니다.
정확한 측정을 요구하는 사용 환경에서는 사용자는 반드시 이러한 요소들을 파악하고 있어야 합니다.

## Thermocouple Types
### Thermocouple Construction
노출형, Ground 접지형, 비 Ground 접지형의 구조가 있습니다.
노출형이 가장 반응이 빠르고, Ground 및 다른 회로에서 발생하는 노이즈에 가장 유리합니다.

### Tolerance Standards
측정 오류 범위는 K-type 의 경우 +- 1.1, 1.5, 2.2, 2.5 도의 차이가 있을수 있습니다.
측정 규격에 따라 허용되는 오차의 범위가 달라집니다.

## Thermocouple Measurement and Cold-Junction Compensation (CJC)

## Design Notes
### Indentify the Range of Thermocouple Operation
### Biasing the Thermocouple
