**Title: Collision Detection System**

**Introduction**

With the advancement of technology and automobile manufacturing, the frequency of road accidents has risen significantly. Unfortunately, due to a lack of proper emergency facilities, the survival rate following accidents remains alarmingly low. Our proposed concept aims to address this issue by developing a system that can detect accidents and determine their location. This information would then be swiftly communicated to rescue teams and the emergency contacts of the vehicle's occupants.

**Components Utilized**

In this project, we focus on collision detection in vehicles. To achieve this, we employ an **impact sensor** mounted on the car's bumper. The sensor is responsible for detecting collisions during accidents. Additionally, we use **ADXL335** to determine the vehicle's orientation. ADXL335 provides comprehensive 3-axis acceleration measurements, with its output signals being analog voltages proportional to the accelerations. The data from ADXL335 is processed by **Arduino**, an open-source microcontroller board equipped with digital and analog input-output pins. By processing this data, the system can detect the accident's location using a **GPS module**. Alert messages are then sent to the vehicle occupants' emergency contacts or nearby emergency services using a **GSM module**. The system operates on a 5V power supply for the GSM module and impact sensor, while the GPS and ADXL335 function on 3.3V.
![COmponents Used](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/660981c5-4baa-4b3e-ae74-e11435a25d8e)

**Design Overview**

![Circuitry](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/8eedf11f-74ca-4a3c-843d-e36e423d3def)

The **impact sensor**, designed to detect collisions, functions as a collision signal sensor. In the simulation software Proteus, we emulate the impact sensor's behavior using the TouchPad tool, considering a collision when tapped. When a collision or flip occurs, a **buzzer** alerts the passengers that an emergency message has been sent. As the ADXL sensor is unavailable in the simulation tool, we used three potentiometers in parallel as an equivalent model. The **GSM module (GSM1)** is programmed to send messages, while **Arduino** processes sensor readings, identifies the current location, and sends this information to the GSM code, which then includes the sensor details in the emergency message.

![Logic flow](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/ff1b8822-37c9-4f9c-bae2-50d82e009ee6)

**Implementation**

The system's implementation involves considering four collision scenarios, each leading to different outcomes:

**Case 1: No impact and no flip**
In this scenario, the vehicle functions normally, requiring no emergency messages to be sent. GPS readings are not necessary, and the GSM module remains inactive.

**Case 2: Impact occurred and no flip**
When a collision happens without the vehicle flipping, the system utilizes GPS to determine the current location and GSM to send emergency messages to relevant services.

**Case 3: No impact and flip occurred**
If the vehicle flips without a collision, the system uses GPS to identify the current location and GSM to send emergency messages to the appropriate contacts.

**Case 4: Impact and flip occurred**
In this case, when a collision happens, and the vehicle flips, the system utilizes GPS to find the current location and GSM to send detailed emergency messages to the necessary services.

**Testing Images**

![Testing Image 2](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/61563777-a2c9-4dfc-bf40-3fd58c1a7aff)

![Testing Image](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/6b35a985-3150-4a79-98c5-c501b88cd901)

![In-case of collision](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/9c59bb3d-e5e0-46ca-bc53-9be43394ac05)

![Phone message](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/d353a00d-2179-416c-b485-ecc596f0bd56)

**Conclusion**

By combining impact sensors, orientation detection, GPS technology, and GSM modules, our collision detection system offers a comprehensive solution to enhance emergency response mechanisms, potentially saving lives in critical situations.
