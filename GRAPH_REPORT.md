# Virtuoso SKILL API Knowledge Graph

Generated: 2026-04-08 16:56:12

## Summary

- **Total Functions**: 8,169
- **Modules**: 27
- **Key Functions Documented**: 30

## Top Modules by Function Count

| Module | Functions | Description |
|--------|-----------|-------------|
| DFII_SKILL | 1,807 | Database interface functions |
| Custom_Layout | 1,311 | Layout automation |
| User_Interface | 742 | UI development |
| ADE-L | 721 | Analog Design Environment L |
| Core_SKILL | 683 | Core language functions |
| OCEAN | 318 | Scripting language |
| ADE_XL | 260 | Advanced simulation |
| Schematics | 351 | Schematic editing |
| ViVA_SKILL | 321 | Waveform viewer |
| Pcells | 141 | Parameterized cells |

## Module Categories

### 🟢 Simulation Suite
- **ADE L**: Basic simulation environment
- **ADE XL**: Advanced simulation with corners
- **ADE Assembler**: Maestro API for modern workflows
- **OCEAN**: Scripting for batch simulation
- **OCEAN XL**: Advanced OCEAN features

### 🔵 Design Entry
- **Schematics**: Schematic capture
- **Custom Layout**: Physical design
- **Pcells**: Parameterized cells

### 🟠 Core Infrastructure
- **Core SKILL**: Language fundamentals
- **DFII SKILL**: Database access

### 🟣 Support Tools
- **User Interface**: Building custom UIs
- **ViVA**: Waveform analysis
- **ADE Verifier**: Design verification

## Key APIs

### ADE Assembler (Maestro)
```lisp
maeAddOutput(t_outputName t_testName ?outputType "...")
maeCloseSession(?session t_sessionName)
maeGetSetup(?typeName t_typeName)
maeSetVar(t_varName t_value)
maeRunSimulation()
```

### OCEAN
```lisp
ocnAddOutput(?outputName t_name ?expr t_expression)
openResults(t_resultsDir)
selectResults(t_result)
plot(getData("signal"))
```

### Custom Layout
```lisp
dbCreateInst(cv master name x:y "R0")
dbCreateRect(cv layer bBox)
dbCreatePath(cv layer points width)
schCreateWireLabel(cv netName center)
```

### Core SKILL
```lisp
append(l_list1 l_list2)      ; 连接列表
car(l_list)                   ; 取首元素
cdr(l_list)                   ; 取尾
cons(g_element l_list)        ; 构建列表
length(l_list)                ; 列表长度
```

## Tool Flow

```
Schematics → Netlisting → ADE L/XL/Assembler → Simulation → ViVA
     ↓              ↑
  Pcells        DFII Database
     ↓              ↑
Custom Layout ──────┘
```

## Surprising Connections

1. **Core SKILL is foundation for all** - Every module depends on core language
2. **ADE evolution path**: ADE L → ADE XL → ADE Assembler (Maestro)
3. **OCEAN integrates with all ADE versions** - Scripting works across tools
4. **Pcells and Custom Layout are tightly coupled** - Pcells extend layout automation

---
*Generated from Cadence Virtuoso SKILL documentation*
