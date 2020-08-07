# LM2576
## Application Information
### Inductor Selection (KR)
모든 switching regulator 들은 continuous 와 discontinuous 의 두 가지 기본 동작 모드가 있습니다.
두 동작 모드의 차이는 인덕터에 흐르는 전류에 있는데,
전류가 지속적으로 흐르는지에 따라,
또는 일반적인 switching 사이클에 0 까지 떨어지에 따라 달라집니다.
각 모드는 특별하게 다른 동작 특성을 가지고 있어 regulator 의 성능과 요구사항에 영향을 줍니다.

LM2576 (또는 SIMPLE SWITCHER® family 의 어느 regulator 들도) 는 continuous 모드와 discontinuous 모드 둘다로 동작이 가능합니다.

Figure 27 에서 Figure 31 까지 이어지는 inductor 값 선택표는 cuntinuous buck regulator 를 설계하기 위한 인덕터값을 설정할수 있게 해줍니다.
inductor 선택표의 inductor 를 사용할때,
인덕터 ripple 전류의 최대-최소값은 DC 전류 최대치의 약 20 ~ 30 % 로 동작합니다.
상대적으로 높은 전류를 공급해야 할때,
회로는 continuous 모드(인덕터의 전류가 항상 흐르는)로 동작하지만,
반대로 낮은 전류를 공급할때는 회로는 (인덕터의 전류가 주기적으로 0 가 되는) discontinuous 모드로 동작합니다.
discontinuous 모드는 완벽하게 동작합니다.
약 300 mA 이하의 낮은 전류를 공급할때 regulators 는 discontinuous 모드로 동작하는데,
낮은 inductor 값이 필요합니다.

inductor 선택표는 continuous mode 동작에 적합한 inductor 값을 추천합니다.
하지만 inductor 값을 매우 크게 선택한다면 discontinuous 동작 가능성이 있다는 점을 알아야 합니다.

인덕터들은 pot core 에 따라서 달라질수 있습니다.
E-frame, bobbin core, 등등이 철 또는 powdered iron 같은 코어 물질에 따라 다르게 정의됩니다.
bobbin core 는 가장 싼 형태로 ferrite rod core 를 와이어로 감싼 형태입니다.
하지만 magnetic flux 가 완전인 core 안에 담기지 않기 때문에 EMI 를 더 많이 발생시킵니다.
EMI 는 민감한 회로에 문제를 발생시키거나 유도 전압으로 인해 오실로스코프의 프로브에 잘못된 값이 읽히게 합니다.

인덕터 선택표에 있는 인덕터에는 AIE, powdered iron toroid, ferrite bobbin core 등이 사용되었습니다.

인덕터는 반드시 최대 전류 이상으로 동작되서는 안됩니다. saturation 을 발생시키기 때문입니다.
인덕터가 statation 되면,
인덕턴스가 빠르게 감소하고,
인덕터는 저항처럼 동작하여 switching 전류가 매우 빠르게 증가하게 됩니다.
인덕터 타입에 따라 saturation 특성이 다르기 때문에 인덕터를 선택할때 반드시 고려되어야 합니다.
인덕터 제조사들은 데이터 시트에 saturation 을 피하기 위한 전류와 전력에 대한 한계를 명시하고 있습니다.

### Inductor Selection
All switching regulators have two basic modes of operation: continuous and discontinuous. The difference
between the two types relates to the inductor current, whether it is flowing continuously, or if it drops to zero for a
period of time in the normal switching cycle. Each mode has distinctively different operating characteristics,
which can affect the regulator performance and requirements.

The LM2576 (or any of the SIMPLE SWITCHER® family can be used for both continuous and discontinuous
modes of operation.

The inductor value selection guides in Figure 27 through Figure 31 are designed for buck regulator designs of
the continuous inductor current type. When using inductor values shown in the inductor selection guide, the
peak-to-peak inductor ripple current is approximately 20% to 30% of the maximum DC current. With relatively
heavy load currents, the circuit operates in the continuous mode (inductor current always flowing), but under light
load conditions, the circuit is forced to the discontinuous mode (inductor current falls to zero for a period of time).
This discontinuous mode of operation is perfectly acceptable. For light loads (less than approximately 300 mA), it
may be desirable to operate the regulator in the discontinuous mode, primarily because of the lower inductor
values required for the discontinuous mode.

The selection guide chooses inductor values suitable for continuous mode operation, but if the inductor value
chosen is prohibitively high, the designer should investigate the possibility of discontinuous operation.

Inductors are available in different styles such as pot core, toriod, E-frame, bobbin core, and so on, as well as
different core materials, such as ferrites and powdered iron. The bobbin core is the least expensive type, and
consists of wire wrapped on a ferrite rod core. This type of construction makes for an inexpensive inductor;
however, because the magnetic flux is not completely contained within the core, the bobbin core generates more
electromagnetic interference (EMI). This EMI can cause problems in sensitive circuits, or can give incorrect
scope readings because of induced voltages in the scope probe.

The inductors listed in the selection chart include ferrite pot core construction for AIE, powdered iron toroid for
Pulse Engineering, and ferrite bobbin core for Renco.

An inductor must not operate beyond its maximum-rated current because it may saturate. When an inductor
begins to saturate, the inductance decreases rapidly, and the inductor begins to look mainly resistive (the DC
resistance of the winding), causing the switch current to rise very rapidly. Different inductor types have different
saturation characteristics, and this must be considered when selecting an inductor.
The inductor manufacturer's data sheets include current and energy limits to avoid inductor saturation.

### Inductor Ripple Current (KR)
레귤레이터가 continous mode 로 동작하면,
인덕터 전류는 삼각 톱날 모양의 전류 파형으로 나타나게 됩니다.
정해진 입력 / 출력 전압이 있을때 인덕터 전류 파형의 최대 / 최소 크기는 고정적입니다.
출력 전류가 증가하고 줄어드는것에 따라 톱날 파형 전류의 전체 크기도 증가하고 줄어듭니다.
인덕터 파형의 DC 평균값은 출력 전류의 DC 평균값과 동일합니다.

만약 출력 전류가 충분히 낮아지게 되면 톱날 파형의 전류도 0 까지 도달하게 됩니다.
그리고 레귤레이터는 discontinuous 모드로 동작하게 됩니다.
이것은 완전히 적합한 동작입니다.
모든 buck switching 레귤레이터들은 출력 전류가 충분히 낮아지면 discontinuous 모드로 동작하도록 되어 있습니다.

### Inductor Ripple Current
When the switcher is operating in the continuous mode, the inductor current waveform ranges from a triangular
to a sawtooth type of waveform (depending on the input voltage). For a given input voltage and output voltage,
the peak-to-peak amplitude of this inductor current waveform remains constant. As the load current rises or falls,
the entire sawtooth current waveform also rises or falls. The average DC value of this waveform is equal to the
DC load current (in the buck regulator configuration).

If the load current drops to a low enough level, the bottom of the sawtooth current waveform reaches zero, and
the switcher changes to a discontinuous mode of operation. This is a perfectly acceptable mode of operation.
Any buck switching regulator (no matter how large the inductor value is) is forced to run discontinuous if the load
current is light enough.

# Buck Regulator Inductor selection
* https://www.ti.com/lit/an/snva038b/snva038b.pdf?ts=1596762346529&ref_url=https%253A%252F%252Fwww.google.com%252F
* https://passive-components.eu/how-to-choose-the-right-inductor-for-dc-dc-buck-applications/
