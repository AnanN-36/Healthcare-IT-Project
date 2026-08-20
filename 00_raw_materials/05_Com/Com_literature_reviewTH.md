# Com: สถาปัตยกรรม IT, แบบจำลองข้อมูล, การบูรณาการ และการกำกับดูแล

## วัตถุประสงค์ของงานวิจัย

กำหนดโครงสร้างทางเทคนิคเชิงแนวคิดสำหรับต้นแบบ Heat Risk Dashboard ระยะ Phase 0 โดยอ้างอิงจากแหล่งข้อมูลที่ศึกษา โครงสร้างนี้เชื่อมโยงข้อมูลต้นทาง ข้อมูลบริบทของประชากร มุมมอง Dashboard ระบบแจ้งเตือน การทำงานร่วมกันระหว่างระบบ และมาตรการกำกับดูแลข้อมูล

> หมายเหตุด้านขอบเขต: เอกสารนี้เป็นร่างด้านการวิจัย/การออกแบบที่สังเคราะห์จากแหล่งข้อมูลของ WHO และ WHO Global Digital Health Monitor (GDHM) ที่จัดหาให้ ไม่ได้หมายความว่า WHO กำหนดสถาปัตยกรรมต้นแบบนี้โดยตรง

---

## 1. ฐานหลักฐานที่ใช้

### 1.1 WHO Digital Transformation Handbook for Health Supply Chain Architecture (2024)

เอกสารแนะนำกระบวนการกำหนดสถาปัตยกรรมแบบเป็นขั้นตอน ได้แก่:

1. ประเมินสถานะปัจจุบันของระบบสารสนเทศที่มีอยู่
2. กำหนดสถาปัตยกรรมเป้าหมาย
3. ระบุกิจกรรมที่จะนำไปใช้และเชื่อมโยงกับเป้าหมายเชิงกลยุทธ์

เอกสารมองสถาปัตยกรรมเป็นเสมือนแบบแผนสำหรับประสานกิจกรรมด้านการเปลี่ยนผ่านสู่ดิจิทัล และเน้นเรื่อง interoperability, การมีส่วนร่วมของผู้มีส่วนได้ส่วนเสีย, การนำทรัพยากรเดิมกลับมาใช้, scalability, การออกแบบที่ครอบคลุม และ open standards

กรอบสถาปัตยกรรมของเอกสารประกอบด้วย:
- ชั้น Interoperability
- ระบบสารสนเทศสุขภาพ
- ระบบภายนอก
- Shared Services / Registries
- บริการข้อมูล
- ความสามารถด้าน การวิเคราะห์ และ Traceability

### 1.2 WHO Health Data Governance Policy Brief (2025)

เอกสารเน้นประเด็น:
- การกำกับดูแลข้อมูลสุขภาพที่เข้มแข็ง
- โครงสร้างพื้นฐานดิจิทัลที่ปลอดภัย
- คุณภาพข้อมูล
- กรอบด้านกฎหมายและจริยธรรม
- Interoperability และการแบ่งปันข้อมูล
- การประสานงานระหว่างผู้ให้ข้อมูล
- การมีส่วนร่วมของผู้มีส่วนได้ส่วนเสีย
- ความเป็นส่วนตัวและความปลอดภัย
- การใช้ AI อย่างน่าเชื่อถือ

เอกสารยังเน้นว่าข้อมูลที่มีคุณภาพต่ำ มีอคติ หรือแยกส่วน อาจส่งผลลบต่อผลลัพธ์ของ AI และการตัดสินใจด้านสุขภาพ

### 1.3 WHO Data Principles (2020)

WHO Data Principles กำหนดหลักการ 5 ประการ ได้แก่:
1. ถือว่าข้อมูลเป็นสาธารณประโยชน์ เมื่อสามารถเปิดเผยได้อย่างปลอดภัยและมีจริยธรรม
2. รักษาความไว้วางใจต่อข้อมูล
3. สนับสนุนขีดความสามารถด้านข้อมูลและระบบสารสนเทศสุขภาพ
4. ทำหน้าที่เป็นผู้จัดการและผู้ดูแลข้อมูลอย่างมีความรับผิดชอบ
5. ช่วยเติมเต็มช่องว่างของข้อมูลสาธารณสุข

ประเด็นที่เกี่ยวข้องกับต้นแบบ ได้แก่ ความโปร่งใส การจัดเก็บและประมวลผลอย่างปลอดภัย ความเป็นส่วนตัว ความสามารถในการตรวจสอบย้อนหลัง คุณภาพข้อมูล ปีอ้างอิงร่วม ความทันเวลา ความถูกต้อง ความสามารถในการเปรียบเทียบ และการใช้หลักการจัดการข้อมูลที่ได้รับการยอมรับ

### 1.4 WHO Global Digital Health Monitor (GDHM)

GDHM เป็นกรอบระดับประเทศสำหรับติดตามระบบนิเวศด้าน Digital Health โดยมี 7 เสาหลัก:
- Leadership and governance — ภาวะผู้นำและการกำกับดูแล
- Strategy and investment — ยุทธศาสตร์และการลงทุน
- Legislation, policy and compliance — กฎหมาย นโยบาย และการปฏิบัติตามข้อกำหนด
- Services and applications — บริการและแอปพลิเคชัน
- Infrastructure — โครงสร้างพื้นฐาน
- Standards and interoperability — มาตรฐานและการทำงานร่วมกันระหว่างระบบ
- Workforce — บุคลากร

กรอบนี้ประกอบด้วย 23 ตัวชี้วัด และมีประเด็นตัดขวาง เช่น เทคโนโลยีเกิดใหม่และความเท่าเทียม

---

## 2. สถาปัตยกรรมเชิงแนวคิดที่เสนอ

### 2.1 ชั้นของสถาปัตยกรรม

```text
                    ผู้ใช้งาน / ผู้มีส่วนได้ส่วนเสีย
                            |
             +--------------+--------------+
             |                             |
        Dashboard UI                  การแจ้งเตือน / รายงาน
             |                             |
             +--------------+--------------+
                            |
                     APPLICATION API
                            |
              +-------------+-------------+
              |                           |
        บริการข้อมูล / Query        ระบบแจ้งเตือน
              |                           |
              +-------------+-------------+
                            |
                  ชั้น INTEROPERABILITY
        การตรวจสอบความถูกต้อง | Transformation | Authentication
                 API / Exchange / Mapping
                            |
        +-------------------+-------------------+
        |                   |                   |
 ข้อมูลสิ่งแวดล้อม   ข้อมูลสุขภาพ/ข้อมูลบริบท   ข้อมูลการดำเนินงาน
 (เช่น ความร้อน/สภาพอากาศ)  (ข้อมูลรวม/ข้อมูลจำลอง)    (ตัวชี้วัดจากระบบ)
        |                   |                   |
        +-------------------+-------------------+
                            |
                     การจัดเก็บข้อมูล
        +-------------------+-------------------+
        |                   |                   |
      ข้อมูลดิบ        ข้อมูลมาตรฐาน     Metadata
        |                   |                   |
        +-------------------+-------------------+
                            |
                    มาตรการกำกับดูแล
```

นี่เป็นการประยุกต์เชิงแนวคิดสำหรับโครงการ โดย WHO Handbook สนับสนุนการใช้ Interoperability Layer, External Systems, Data Services และ Shared Services เป็นองค์ประกอบของสถาปัตยกรรม

---

## 3. แบบจำลองข้อมูลเชิงตรรกะ

แบบจำลองข้อมูลควรจัดให้อยู่บนหน่วยวิเคราะห์ร่วม:

**พื้นที่ + เวลา + ตัวชี้วัด + ค่า + แหล่งข้อมูล + บริบท**

### 3.1 Entity หลัก

| Entity | วัตถุประสงค์ | ตัวอย่างฟิลด์ |
|---|---|---|
| `area` | หน่วยพื้นที่ | `area_id`, `area_name`, `level`, `parent_area_id` |
| `time_period` | ช่วงเวลาอ้างอิงร่วม | `time_id`, `date`, `year`, `month` |
| `indicator` | นิยามสิ่งที่วัด | `indicator_id`, `name`, `unit`, `description` |
| `observation` | จัดเก็บค่าของตัวชี้วัด | `observation_id`, `area_id`, `time_id`, `indicator_id`, `value` |
| `data_source` | บันทึกที่มา/แหล่งข้อมูล | `source_id`, `name`, `url`, `version`, `retrieved_at` |
| `population_context` | ข้อมูลบริบทประชากรกลุ่มเปราะบางแบบรวม/จำลอง | `area_id`, `time_id`, `group`, `population_count`, `source_id` |
| `alert` | จัดเก็บการแจ้งเตือน | `alert_id`, `area_id`, `time_id`, `severity`, `rule_id`, `status` |
| `alert_rule` | กำหนดเงื่อนไขการแจ้งเตือน | `rule_id`, `indicator_id`, `operator`, `threshold`, `severity` |
| `data_quality` | บันทึกผลการตรวจสอบคุณภาพ | `observation_id`, `completeness`, `validity`, `quality_status` |
| `user_role` | บทบาทด้านการกำกับดูแล/สิทธิ์เข้าถึง | `role_id`, `name`, `permissions` |
| `audit_log` | บันทึกกิจกรรมสำคัญของระบบ | `log_id`, `actor`, `action`, `resource`, `timestamp` |

### 3.2 Relationships

```text
AREA 1 ---- N OBSERVATION N ---- 1 INDICATOR
  |                  |
  |                  +------------ 1 DATA_SOURCE
  |
  +---- N POPULATION_CONTEXT

TIME_PERIOD 1 ---- N OBSERVATION
TIME_PERIOD 1 ---- N POPULATION_CONTEXT
TIME_PERIOD 1 ---- N ALERT

INDICATOR 1 ---- N ALERT_RULE
ALERT_RULE 1 ---- N ALERT

USER_ROLE 1 ---- N AUDIT_LOG
```

The model deliberately separates the **indicator definition** from the **observation value** so that different sources can provide observations using the same conceptual indicator.

---

## 4. การทำข้อมูลให้เป็นมาตรฐาน

ก่อนนำข้อมูลไปใช้ใน Dashboard:

1. ระบุแหล่งที่มาและ provenance
2. ตรวจสอบฟิลด์ที่จำเป็น
3. ทำรหัสพื้นที่ให้เป็นมาตรฐานเดียวกัน
4. ทำวันที่/ช่วงเวลาให้เป็นมาตรฐาน
5. ทำหน่วยวัดให้เป็นมาตรฐาน
6. จับคู่ตัวแปรจากแหล่งข้อมูลเข้ากับตัวชี้วัดกลาง
7. บันทึกข้อมูลที่หายและสถานะคุณภาพ
8. จัดเก็บ Observation ที่ผ่านการทำมาตรฐาน
9. เก็บค่าต้นฉบับ/ข้อมูลดิบไว้เมื่อเหมาะสม

แนวทางนี้สอดคล้องกับการเน้นของ WHO เรื่อง interoperability, standards, data quality, transparency และการดูแลข้อมูลอย่างรับผิดชอบ

---

## 5. การออกแบบการบูรณาการ

### 5.1 รูปแบบการบูรณาการ

```text
แหล่งข้อมูลภายนอก
      |
      v
 ตัวรับข้อมูล
      |
      v
 การตรวจสอบความถูกต้อง
      |
      v
 การแปลง / การจับคู่ข้อมูล
      |
      v
 แบบจำลองข้อมูลกลาง
      |
      +------> ที่จัดเก็บข้อมูล
      |
      +------> การวิเคราะห์
      |
      +------> ระบบแจ้งเตือน
      |
      +------> Dashboard API
```

### 5.2 การควบคุมการบูรณาการ

| การควบคุม | วัตถุประสงค์ |
|---|---|
| Source identifier | ระบุว่า Observation มาจากแหล่งใด |
| Retrieval timestamp | ระบุเวลาที่ดึงข้อมูล |
| Schema validation | ตรวจจับข้อมูลที่มีรูปแบบผิด |
| Unit validation | ป้องกันหน่วยวัดที่ไม่เข้ากัน |
| Geographic mapping | ทำให้รหัสพื้นที่สอดคล้องกัน |
| Indicator mapping | แปลงฟิลด์ต้นทางเป็นตัวชี้วัดกลาง |
| Duplicate detection | ป้องกัน Observation ซ้ำ |
| Missing-data flag | แยกค่า 0 ออกจากข้อมูลที่ไม่มี |
| Versioning | เก็บประวัติการเปลี่ยนแปลงชุดข้อมูล |
| Audit trail | บันทึกกิจกรรมสำคัญของข้อมูล/ระบบ |

The WHO architecture handbook identifies interoperability capabilities such as authentication, orchestration, encryption, validation, transformation and translation as components supporting data exchange.

---

## 6. มาตรการกำกับดูแล

### 6.1 การกำกับดูแลข้อมูล

ต้นแบบควรกำหนด:
- เจ้าของข้อมูล
- Metadata ของแหล่งข้อมูล/Provenance
- กฎตรวจสอบคุณภาพข้อมูล
- สิทธิ์การเข้าถึง
- กฎการเก็บรักษาข้อมูล
- เงื่อนไขการแบ่งปันข้อมูล
- หน้าที่ในการทบทวน
- ขั้นตอนจัดการเหตุการณ์และการยกระดับปัญหา

### 6.2 ความเป็นส่วนตัวและความปลอดภัย

เมื่อมีข้อมูลสุขภาพหรือบริบทของกลุ่มเปราะบาง:
- ลดการใช้ข้อมูลที่ระบุตัวบุคคลได้
- ในต้นแบบควรใช้ข้อมูลแบบรวม หรือ de-identified เป็นหลัก
- ใช้การควบคุมการเข้าถึงตามบทบาท
- ป้องกันข้อมูลระหว่างส่งและขณะจัดเก็บ
- บันทึกกิจกรรมการดูแลระบบที่มีความสำคัญ
- กำหนดผู้ที่มีสิทธิ์ส่งออกข้อมูล
- บันทึกวัตถุประสงค์/ขอบเขตการใช้ข้อมูลที่อนุญาต

### 6.3 คุณภาพข้อมูล

การตรวจสอบขั้นต่ำ:
- ความครบถ้วน
- ความถูกต้องตามรูปแบบ/เงื่อนไข
- ความสอดคล้อง
- ความทันเวลา
- การตรวจข้อมูลซ้ำ
- การตรวจช่วงค่า
- ความใหม่ของแหล่งข้อมูล
- ความสอดคล้องของพื้นที่

### 6.4 ความสามารถในการตรวจสอบย้อนหลัง

กิจกรรมสำคัญควรสร้าง Audit Record เช่น:
- การเข้าสู่ระบบ/ยืนยันตัวตน
- การนำเข้าข้อมูล
- การแก้ไขข้อมูล
- การสร้าง Alert
- การรับทราบ Alert
- การเปลี่ยนแปลงการตั้งค่า
- การส่งออกข้อมูล
- การเปลี่ยนแปลงสิทธิ์ผู้ดูแลระบบ

---

## 7. สถาปัตยกรรม Dashboard และระบบแจ้งเตือน

### Dashboard

Dashboard สามารถแสดง:
- ตัวชี้วัดความเสี่ยงจากความร้อนปัจจุบัน
- แนวโน้มตามเวลา
- การเปรียบเทียบตามพื้นที่
- บริบทของกลุ่มประชากรเปราะบาง
- ข้อมูลแหล่งที่มา/Provenance
- สถานะคุณภาพข้อมูล

### ระบบแจ้งเตือน

ตัวอย่างกฎอย่างง่าย:

```text
IF indicator value >= threshold
AND data quality = valid
THEN create alert
WITH severity = configured level
FOR area + time period
```

For a more advanced prototype:

```text
Risk score =
    environmental indicator
  + population vulnerability context
  + temporal persistence
  + configurable weighting
```

สูตรคำนวณคะแนนความเสี่ยงควรถูกถือเป็น **การออกแบบเฉพาะของโครงการ** ไม่ใช่สูตรที่ WHO กำหนด

---

## 8. การใช้ GDHM เป็นกรอบอ้างอิงสำหรับการประเมิน

สามารถใช้ GDHM เป็นกรอบอ้างอิงระดับสูงสำหรับประเมิน maturity/landscape ไม่ควรใช้แทนรายละเอียดสถาปัตยกรรมของระบบ

| เสาหลัก GDHM | ความเกี่ยวข้องกับต้นแบบ |
|---|---|
| Leadership & Governance | เจ้าของข้อมูล ความรับผิดชอบ และบทบาทด้าน Governance |
| Strategy & Investment | ความยั่งยืนและการวางแผนดำเนินงาน |
| Legislation, Policy & Compliance | ความเป็นส่วนตัว การแบ่งปันข้อมูล และข้อกำหนดที่เกี่ยวข้อง |
| Services & Applications | Dashboard ระบบแจ้งเตือน และบริการวิเคราะห์ |
| Infrastructure | Hosting เครือข่าย การจัดเก็บ และความพร้อมใช้งาน |
| Standards & Interoperability | แบบจำลองข้อมูลกลางและการแลกเปลี่ยนข้อมูล |
| Workforce | ผู้ดูแลระบบ ผู้จัดการข้อมูล และผู้ใช้งาน |

ตารางนี้เป็นการนำกรอบ GDHM มาประยุกต์เชิงวิเคราะห์กับโครงการ

---

## 9. ผลลัพธ์ที่ควรได้ใน Phase 0

The Phase 0 architecture work should produce:

1. ภาพรวมสถานะปัจจุบันของระบบและข้อมูล
2. สถาปัตยกรรมเป้าหมายเชิงแนวคิด
3. แบบจำลองข้อมูลเชิงตรรกะ
4. การจับคู่ข้อมูลจากต้นทางสู่ข้อมูลเป้าหมาย
5. รายการ Integration / Interface
6. ตาราง Governance Controls
7. กฎคุณภาพข้อมูล
8. แบบจำลองการควบคุมการเข้าถึง
9. ข้อกำหนด Audit
10. Roadmap การดำเนินงานระดับสูง

---

## 10. การเชื่อมโยงแหล่งอ้างอิงกับการออกแบบ

| องค์ประกอบการออกแบบ | แหล่งอ้างอิงสนับสนุน |
|---|---|
| การประเมินสถานะปัจจุบัน | WHO Digital Transformation Handbook, Chapter 2 |
| สถาปัตยกรรมเป้าหมาย | WHO Digital Transformation Handbook, Chapter 2 |
| Interoperability Layer | WHO Digital Transformation Handbook, DHSC architecture framework |
| External Systems | WHO Digital Transformation Handbook, DHSC architecture framework |
| Shared Registries / Master Data | WHO Digital Transformation Handbook, DHSC architecture framework |
| Data Services / Analytics | WHO Digital Transformation Handbook, DHSC architecture framework |
| คุณภาพข้อมูล | WHO health data governance policy brief |
| ความเป็นส่วนตัว/ความปลอดภัย | WHO health data governance policy brief + WHO Data Principles |
| การตรวจสอบย้อนหลัง/ความโปร่งใส | WHO Data Principles |
| การมีส่วนร่วมของผู้มีส่วนได้ส่วนเสีย | WHO health data governance policy brief + WHO Digital Transformation Handbook |
| มาตรฐาน/Interoperability | WHO health data governance policy brief + GDHM |
| การประเมิน Digital Health Ecosystem | GDHM |
| สถาปัตยกรรมที่สามารถขยายได้ | WHO Digital Transformation Handbook |

---

## 11. ข้อจำกัดสำคัญ

- แหล่งข้อมูล WHO ให้หลักการ กรอบแนวคิด และตัวอย่างสถาปัตยกรรม แต่ **ไม่ได้กำหนด schema หรือ API ที่แน่นอนสำหรับโครงการนี้**
- ดังนั้น Entity Model ที่เสนอจึงเป็นแบบจำลองเชิงตรรกะเฉพาะของโครงการที่สังเคราะห์จากแนวคิดในแหล่งอ้างอิง
- สูตร Alert/Risk เป็นการออกแบบเฉพาะของโครงการและต้องผ่านการตรวจสอบก่อนนำไปใช้กับการตัดสินใจด้านคลินิกหรือสาธารณสุขจริง
- ข้อมูลกลุ่มเปราะบางควรอยู่ในรูปแบบรวม/de-identified เว้นแต่มีเหตุผลและการกำกับดูแลที่ชัดเจนสำหรับข้อมูลที่ละเอียดกว่านั้น
- หน้า GDHM ระบุว่าเว็บไซต์อยู่ในสถานะ beta และข้อมูลควรได้รับการทบทวนและตรวจสอบโดยประเทศสมาชิกที่เข้าร่วม ดังนั้นควรระบุสถานะนี้ไว้ในบันทึกการวิจัย

---

## เอกสารอ้างอิง

1. World Health Organization. *Digital transformation handbook for health supply chain architecture*. Geneva: WHO; 2024.
2. World Health Organization. *Health data governance in the age of artificial intelligence: policy imperatives for the WHO European Region*. Copenhagen: WHO Regional Office for Europe; 2025.
3. World Health Organization. *World Health Organization Data Principles*. 2020.
4. World Health Organization. *Global Digital Health Monitor*. WHO Data, ข้อมูลปี 2023 / แพลตฟอร์มปัจจุบัน.

