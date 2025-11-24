# ATFA
A High-Speed Electronic Alternative to Pitot Tubes

# ✈️ Acoustic Time-of-Flight Anemometer (ATFA): A High-Speed Electronic Alternative to Pitot Tubes

**Project Concept:**  
This project presents a novel **electronic fluid velocity measurement system** designed as a potential alternative to conventional Pitot tube systems in aerodynamics. The sensor measures airflow velocity by tracking the propagation time of a controlled acoustic burst through a short pipe and calculating the resulting **time-of-flight difference (Δτ)** between two microphones.

---

## 🧠 How It Works: Acoustic Time-of-Flight Principle

1. **Single Acoustic Burst Generation:**  
   A miniature speaker located at the center of a short pipe emits a single-tone burst (e.g., 20 kHz, 1 ms duration). The pipe is aligned with the airflow to be measured.

2. **Time Difference (Δτ) Measurement:**  
   Two microphones positioned at the ends of the pipe detect the arrival of the burst. The airflow accelerates the wave toward one microphone (c+v) and slows it toward the other (c−v). The system measures the difference in arrival times **Δτ**.

3. **Velocity Calculation:**  
   The fluid velocity \(v\) is calculated using the speed of sound \(c\) and the distance between microphones \(2L\):

   

$$v \approx \frac{\Delta \tau \cdot c^2}{2L}$$



4. **Burst Control Optimization:**  
   Each new burst is emitted only after the previous one has fully reached both microphones. This design removes repetition-rate limitations and allows measurement of **high-speed and even supersonic flows**, depending on sensor response time.

5. **Noise Filtering:**  
   Each microphone channel is filtered using a band-pass filter centered at the burst frequency (e.g., 20 kHz) to reject ambient noise. Optional envelope detection or comparators can provide clean digital signals for microcontroller capture.

---

## ⭐ Key Advantages

- **Electronic, high-speed alternative** to traditional Pitot tubes.  
- **Scalable**: from slow laboratory airflow experiments to high-speed aerodynamics.  
- **Reliable burst control** prevents timing conflicts between signals.  
- **Simple microcontroller implementation** (Arduino, ESP32, Deneyap Mini).  
- **Adjustable resolution** via burst averaging or advanced signal processing.  

---

## ⚙️ Typical Parameters (Prototype Example)

| Parameter | Example Value | Notes |
|-----------|---------------|-------|
| Pipe length (center → microphone) | 0.343 m | Matches speed of sound for timing clarity |
| Burst frequency | 20 kHz | Ultrasonic, inaudible to humans |
| Burst duration | 1 ms | Critical for detection accuracy |
| Burst repetition | Triggered after previous burst detected | Enables high-speed flow measurement |
| Target resolution | ~0.1–1 km/h (with averaging) | Adjustable |

---

## 🎯 Applications

- Replacement for Pitot tubes in small aircraft or drones  
- Precision airflow measurements in wind tunnels and labs  
- Educational demonstrations of time-of-flight velocity sensing  
- Any project requiring **non-intrusive, high-speed fluid velocity measurement**  

---

## 🗺️ Next Steps

1. Prototype the analog front-end with a central speaker, two microphones, and band-pass filtering.  
2. Implement timestamp capture on a microcontroller (Arduino, ESP32, Deneyap Mini).  
3. Calculate velocity using Δτ measurements and unit conversions.  
4. Test accuracy and repeatability; optimize burst duration and averaging.  

---

## 🌍 Philosophy & Open-Source Vision

This project is not only a technical innovation but also an **educational tool**. By making advanced aerodynamics measurement accessible, it empowers students, researchers, and makers worldwide. Contributions are welcome — from new algorithms to hardware designs — to build a shared legacy of open-source aerodynamics.
