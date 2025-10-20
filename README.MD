## wip

- compiled trackpad information (why did I crtl+h to touchpad....) looking to see what I could swap into a t14s gen2. Ordered 5M11G56210, not yet confirmed to work, but I do not see why it would not.

---

### **Lenovo ThinkPad Touchpad FRU Reference (CS21–CS23)**
| FRU                            | Family       | Lenovo Descriptor                                                   | Vendor                     | Material (Actual)                                            | Finish Color  | Controller    | Compatible Systems                           |
| ------------------------------ | ------------ | ------------------------------------------------------------------- | -------------------------- | ------------------------------------------------------------ | ------------- | ------------- | -------------------------------------------- |
| **5M11B95843–848**             | CS21         | GL-Mylar VB1 (Sunrex / Trantek / Chicony)                           | Sunrex / Trantek / Chicony | PET film (fluoropolymer hard-coat)                           | Villi Black 1 | Elan          | T14s Gen 2 / X13 Gen 2                       |
| **5M11B95853**                 | CS21 Refresh | GL-Mylar + Elan PCB, Storm Gray (SOVP & MP)                         | Sunrex                     | PET film (revised low-friction formulation)                  | Storm Gray    | Elan          | T14s Gen 3                                   |
| **5M11G56181 / 56221 / 56222** | CS22         | GL-Mylar VB1 (SUN / TRA / CHY)                                      | Sunrex / Trantek / Chicony | PET film (silica-hybrid coat)                                | Villi Black 1 | Elan          | T14s Gen 4 / X13 Gen 4                       |
| **5M11G56210**                 | CS23         | Glass-laminate, Elan PCB, Gray, Non-NFC (SOVP & MP Transimage)      | **Transimage / LCFC**      | **Glass-laminate (aluminosilicate glass bonded to carrier)** | Graphite Gray | **Elan**      | X1 2-in-1 Gen 9 / Gen 10 → fits T14s Gen 2–3 |
| **5M11G56211 / 56212**         | CS23         | Glass-laminate, Synaptics PCB, Gray, Non-NFC (SOVP & MP Transimage) | **Transimage / Chicony**   | **Glass-laminate (aluminosilicate glass bonded to carrier)** | Graphite Gray | **Synaptics** | X1 2-in-1 Gen 9 / Gen 10 → fits T14s Gen 2–3 |
| **SM10P36008**                 | CS20         | Glass touchpad assembly                                             | Sunrex                     | **Tempered glass (monolithic substrate)**                    | Black         | Elan          | T14 / P14s (non-S)                           |
| **01LX660**                    | CS20         | Glass touchpad assembly                                             | Chicony                    | **Tempered glass (monolithic substrate)**                    | Black         | Elan          | X1 Extreme / P1 Gen 1–2                      |


### **CS23-series “glass-laminate” graphite pads**
| FRU            | Controller        | OEM Vendor     | Descriptor (Lenovo)                                      | Notes                              |
| -------------- | ----------------- | -------------- | -------------------------------------------------------- | ---------------------------------- |
| **5M11G56210** | **Elan PCB**      | **Transimage** | CS23 3+2bCP Glass, Elan PCB, Gray, Non-NFC, SOVP&MP      | Baseline part; X1 2-in-1 Gen 9/10  |
| **5M11G56209** | **Elan PCB**      | **Chicony**    | CS23 3+2bCP Glass, Elan PCB, Gray, Non-NFC, SOVP&MP      | Same part, Chicony build           |
| **5M11G56211** | **Synaptics PCB** | **Chicony**    | CS23 3+2bCP Glass, Synaptics PCB, Gray, Non-NFC, SOVP&MP | Same surface; Synaptics controller |
| **5M11G56212** | **Synaptics PCB** | **Transimage** | CS23 3+2bCP Glass, Synaptics PCB, Gray, Non-NFC, SOVP&MP | Same as 56211, different supplier  |


### **Chain**

| Generation                 | Descriptor        | Substrate                                                 | Notes                                |
| -------------------------- | ----------------- | --------------------------------------------------------- | ------------------------------------ |
| CS21 / CS22                | “GL-Mylar”        | PET film                                                  | Fluoropolymer hard-coat plastic      |
| **CS23 (X1 Gen 9 / 10)**   | **“Glass”**       | **Glass-laminate** (≈0.3 mm aluminosilicate over carrier) | Supplied by **Transimage / Chicony** |
| CS23 G (X1 Carbon Gen 11+) | “Glass Substrate” | Thicker full glass slab                                   | No top buttons; haptic               |

| Type                    | Used In                                        | Structure                                                                                        | Thickness                             | Flexibility                      | Click Support                         | Example FRU                |
| ----------------------- | ---------------------------------------------- | ------------------------------------------------------------------------------------------------ | ------------------------------------- | -------------------------------- | ------------------------------------- | -------------------------- |
| **Glass-laminate**      | CS23 pads (e.g. 5M11G56210)                    | Ultra-thin aluminosilicate or soda-lime glass **bonded to a metal carrier or polymer sub-layer** | ~0.25–0.35 mm glass + 0.2 mm adhesive | Slightly flexible                | ✅ Mechanical dome buttons underneath | 5M11G56210 / 56211 / 56212 |
| **Full tempered glass** | Haptic / button-less pads (e.g. X1 Carbon, P1) | Single thick (~0.8–1.2 mm) **tempered sheet**, no backing film                                   | Rigid                                 | ❌ (uses piezo / haptic actuator) | 01LX660 / SM10P36008                 |                            |

5M11G56210 / 56209 / 56211 / 56212 → Glass-laminate Touchpads (CS23 series).
5M11G56181 / 56222 etc. → Mylar (CS22 series).
SM10P36008 / 01LX660 → Full tempered glass (thick, non-Touchpad).

---

### **Lenovo ThinkPad Mylar & Glass Touchpad Reference**
| FRU / Part Number                      | Family / Generation            | Lenovo Descriptor String                                         | Supplier (OEM)  | Color Code          | Controller | Material / Surface                                    | Notes / Compatibility / Substitutes                        |
| -------------------------------------- | ------------------------------ | ---------------------------------------------------------------- | --------------- | ------------------- | ---------- | ----------------------------------------------------- | ---------------------------------------------------------- |
| **5M11B95843**                         | CS21 Gen 2                     | CS21 3+2b GL-Mylar VB1 SUN                                       | Sunrex          | VB1 (Villi Black 1) | Elan       | 1st-gen GL-Mylar (PET film + fluoropolymer hard-coat) | Base unit; T14s Gen 2 / X13 Gen 2                          |
| **5M11B95844**                         | CS21 Gen 2                     | CS21 3+2b GL-Mylar VB1 SUN                                       | Sunrex          | VB1                 | Elan       | Same as 95843 (identical spec)                        | Interchangeable with 95845–95848                           |
| **5M11B95845**                         | CS21 Gen 2                     | CS21 3+2b GL-Mylar VB1 TRA                                       | Trantek         | VB1                 | Elan       | Same GL-Mylar                                         | Equivalent to Sunrex units                                 |
| **5M11B95846**                         | CS21 Gen 2                     | MECH_ASM CS21 3+2b GL-Mylar VB1 CHY                              | Chicony         | VB1                 | Elan       | Same GL-Mylar                                         | OEM Chicony assembly                                       |
| **5M11B95847**                         | CS21 Gen 2                     | CS21 3+2b GL-Mylar VB1 SUN                                       | Sunrex          | VB1                 | Elan       | Same coating (Sunrex lot 2)                           | Equivalent to 95844                                        |
| **5M11B95848**                         | CS21 Gen 2                     | CS21 3+2b GL-Mylar VB1 TRA                                       | Trantek         | VB1                 | Elan       | Same coating (Trantek lot 2)                          | Equivalent to 95845                                        |
| **5M11B95853**                         | CS21 Gen 2 Refresh             | CS21 3+2bCP Medium GL-Mylar + Elan PCB Storm Gray SOVP&MP Sunrex | Sunrex          | Storm Gray          | Elan       | 2nd-gen GL-Mylar (enhanced low-friction coating)      | Successor to 9584x series (T14s Gen 3)                     |
| **5M11G56222**                         | CS22 Gen 4                     | CS22 3+2b GL-Mylar VB1 SUN                                       | Sunrex          | VB1                 | Elan       | 3rd-gen GL-Mylar (hybrid silica top-coat)             | T14s Gen 4 / X13 Gen 4; replaces 95853                     |
| **5M11G56181**                         | CS22 Gen 4                     | CS22 3+2b GL-Mylar VB1 TRA                                       | Trantek         | VB1                 | Elan       | Same as 56222                                         | Substitute part                                            |
| **5M11G56221 / 56180 / 56183 / 56184** | CS22 Gen 4                     | CS22 3+2b GL-Mylar variants                                      | Mixed (Vendors) | VB1                 | Elan       | Same surface family                                   | All interchangeable variants                               |
| **5M11G56210**                         | **CS23 Gen 5 (X1 Gen 9 / 10)** | **CS23 3+2bCP GL GR NONFC TRI**                                  | LCFC / Chicony  | GR (Graphite Gray)  | Elan       | **Glass-Laminate**                                    | Works in T14s Gen 2/3; same mechanical fit; premium finish |
| **5M11G56209 / 56211 / 56212**         | CS23 Gen 5                     | CS23 3+2bCP GL GR variants                                       | LCFC / Trantek  | GR                  | Elan       | Same as 56210                                         | Regional substitutes (X1 2-in-1 Gen 9/10)                  |
| **SM10P36008**                         | T14 / P14s (non-S)             | CS20 3+2b Glass                                                  | Sunrex          | Black               | Elan       | **True Glass** (tempered)                             | Real glass pad – larger non-S chassis                      |
| **01LX660**                            | X1 Extreme / P1                | CS20 3+2b Glass                                                  | Chicony         | Black               | Elan       | **True Glass**                                        | Used in high-end models only                               |

### **Substitution and Compatibility Chain**
| Original FRU                               | Direct Replacements / Substitutes          | Generation Shift          | Notes                          |
| ------------------------------------------ | ------------------------------------------ | ------------------------- | ------------------------------ |
| 5M11B95843 → 95844                         | Same spec, Sunrex lot change               | —                         | interchangeable                |
| 5M11B95844 → 95845–95848                   | Vendor change (Sunrex ↔ Trantek ↔ Chicony) | —                         | identical surface              |
| 5M11B95853 → 5M11G56222 / 56181            | CS21 → CS22                                | new silica hard-coat      |                                |
| 5M11G56222 ↔ 56181 / 56221 / 56183 / 56184 | CS22 intra-family swap                     | —                         | interchangeable across vendors |
| 5M11G56210 ↔ 56209 / 56211 / 56212         | CS23 intra-family                          | —                         | same design and connector      |
| SM10P36008 / 01LX660                       | —                                          | different chassis (non-S) | true glass pads only           |

### **Material and Coating Evolution**
| Generation / Family           | Surface Composition                                          | Hard-Coat System             | Color Options      | Notes                                                            |
| ----------------------------- | ------------------------------------------------------------ | ---------------------------- | ------------------ | ---------------------------------------------------------------- |
| **CS21 (T14s Gen 2)**         | PET Mylar film                                               | Fluoropolymer (“glass-feel”) | VB1 Black          | Original GL-Mylar design                                         |
| **CS21 Refresh (95853)**      | PET Mylar                                                    | Improved fluoropolymer       | Storm Gray         | Lower friction rev 2 surface                                     |
| **CS22 (T14s Gen 4)**         | PET Mylar                                                    | Silica-polymer hybrid        | VB1 Black          | 3rd-generation coating update                                    |
| **CS23 (X1 Gen 9 / 10)**      | **Glass-laminate (aluminosilicate glass bonded to carrier)** | Hard-coat glass surface      | Graphite Gray (GR) | First generation of real glass-laminate Touchpads (with buttons) |
| **CS23 G (X1 Carbon Gen 11)** | **Tempered glass substrate (monolithic)**                    | —                            | Jet Black          | Full glass slab; non-Touchpad haptic variant                     |



### **Cross-Compatibility**
| Donor FRU                    | Fits In                                          | Result                                |
| ---------------------------- | ----------------------------------------------   |  ------------------------------------ |
| 5M11G56210 (CS23 X1 Gen 9)   | Yes T14s Gen 2 / Gen 3                           | Full fit + function (same FFC pinout) |
| 5M11G56222 (CS22 T14s Gen 4) | Yes-ish T14s Gen 2 / 3 with minor bracket adjust | Slight bracket mismatch possible      |
| SM10P36008 (glass)           | No T14s Gen 2                                    | Too thick / different mount points    |
