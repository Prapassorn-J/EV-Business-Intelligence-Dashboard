⚡ EV Business Intelligence Dashboard – Thailand Market Insight

**จากอดีต → ปัจจุบัน → โอกาสลงทุนในอนาคต**

โปรเจกต์นี้เป็นการวิเคราะห์ข้อมูลเชิงลึกของอุตสาหกรรมยานยนต์ไฟฟ้า (EV) ในประเทศไทย ตั้งแต่ภาพรวมตลาดโลกจนถึงโครงสร้างดีมานด์–ซัพพลายในระดับจังหวัด เพื่อสนับสนุนการตัดสินใจด้านกลยุทธ์และการลงทุนของธุรกิจที่เกี่ยวข้องกับ EV Ecosystem

## การออกแบบข้อมูล (Data Architecture)

โปรเจกต์ใช้แหล่งข้อมูลหลัก 3 ชุด

1. **EV Sale (Global)** – ข้อมูลยอดขาย EV ทั่วโลก (region/country, powertrain, parameter, year)
2. **Vehicle Registration (Thailand)** – ข้อมูลจดทะเบียนรถยนต์จากกรมขนส่งทางบก
3. **EV Charging Station (Thailand)** – จำนวนและตำแหน่งสถานีชาร์จในไทย

ข้อมูลทั้งหมดถูก **Clean → Transform → Load (ETL)** ผ่าน *Staging Area* ก่อนโหลดเข้าสู่ **BigQuery**
แดชบอร์ดพัฒนาใน **Looker Studio** เพื่อการวิเคราะห์แบบ Interactive

##  อินไซต์สำคัญจาก 4 Dashboard

### 1️. Thailand EV Market Overview

* ไทยยังเป็น **ตลาดขนาดเล็ก** แต่เป็นหนึ่งในประเทศที่ **โตเร็วที่สุดของโลก**
* Sales share เพิ่มจาก **0.6% → 7.1% ภายใน 3 ปี**
* ดีมานด์เติบโตเร็วกว่างานพัฒนาโครงสร้างพื้นฐาน → เริ่มเกิด “คอขวด” ทั่วประเทศ

### 2️. Market Structure & Brand Landscape

* กลุ่มเติบโตสูงสุดคือ **รถนั่ง ≤ 7 ที่นั่ง (Type 1)** และ **มอเตอร์ไซค์ไฟฟ้า**
* **BYD ครองตลาดแบบผู้นำชัดเจน** 
* ตลาดกำลังเข้าสู่ Mass Adoption ทำให้การแข่งขันเริ่มเข้มข้น

### 3️. Geographic Demand vs Infrastructure Gap

* จังหวัดส่วนใหญ่มีรถ EV หลักพัน–หลักหมื่น แต่มีสถานีเพียง 1–10 จุด
* อุดรธานี กรุงเทพมหานคร สงขลา นครศรีธรรมราช นครราชสีมา มี “ดีมานด์สูงแต่โครงสร้างไม่พอ”
* สะท้อนความจำเป็นในการวางโครงสร้างพื้นฐานแบบ *pinpoint location*

### 4️. Cluster Model + Opportunity Index

ใช้ **K-Means (k=3)** วิเคราะห์จังหวัดไทยตามตัวแปร EV/DC และอัตราการเติบโต
ผลลัพธ์ 3 กลุ่มหลัก:

* **Cluster 2 – Mature Hub**: กรุงเทพฯ (โครงสร้างพร้อมสุด → Benchmark)
* **Cluster 1 – Balanced & Infra-Ready**: เหมาะสำหรับบริการ Value-Added
* **Cluster 0 – High Demand, Low Infrastructure**: จุดลงทุนเร่งด่วนที่สุด

**Top Provinces to Invest:**
นครราชสีมา • ขอนแก่น • พิษณุโลก • ตรัง • สระบุรี

กลยุทธ์แนะนำ: สร้าง Fast-Charging Hub + Partnership กับ Taxi / Ride-hailing / Logistics

## สรุปคุณค่าทางธุรกิจ (Business Value)

* ให้ภาพรวม EV ไทยแบบครบทุกมิติ (Demand, Supply, Infra, Geography, Cluster)
* ช่วยองค์กรตัดสินใจ “ลงทุนที่ไหนก่อน” ภายใต้งบประมาณจำกัด
* รองรับกลยุทธ์ขยายสถานีชาร์จให้ “คุ้มทุนที่สุด”
* ใช้เป็น Framework ตัวอย่างสำหรับ Data-Driven Market Expansion


## Tech Stack ที่ใช้

* **SQL, BigQuery** – Data Warehouse
* **Python (Pandas, NumPy, Scikit-learn)** – Data Cleaning, Feature Engineering, Clustering
* **Looker Studio** – Dashboard & Visualization
* **ETL Pipeline Design** – Staging → Transformation → Fact/Dimension Model

