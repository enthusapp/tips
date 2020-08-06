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
When the switcher is operating in the continuous mode, the inductor current waveform ranges from a triangular
to a sawtooth type of waveform (depending on the input voltage). For a given input voltage and output voltage,
the peak-to-peak amplitude of this inductor current waveform remains constant. As the load current rises or falls,
the entire sawtooth current waveform also rises or falls. The average DC value of this waveform is equal to the
DC load current (in the buck regulator configuration).

If the load current drops to a low enough level, the bottom of the sawtooth current waveform reaches zero, and
the switcher changes to a discontinuous mode of operation. This is a perfectly acceptable mode of operation.
Any buck switching regulator (no matter how large the inductor value is) is forced to run discontinuous if the load
current is light enough.

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
