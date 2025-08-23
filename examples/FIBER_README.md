# Optical Fiber Cable Examples

This directory contains examples demonstrating WireViz's support for optical fiber cables.

## Examples

### fiber01.yml - Basic Single-Mode Fiber
- Demonstrates single-mode OS2 fiber cable
- LC duplex connectors
- Shows fiber specifications: core/cladding diameter, wavelength
- Standard yellow color for single-mode fiber

### fiber02.yml - Multi-Mode Trunk Cable
- Demonstrates multi-mode OM3 fiber trunk cable
- MPO/MTP connectors (12-fiber)
- Shows multi-mode specifications: numerical aperture, bandwidth
- Uses standard 12-fiber color code

### fiber03.yml - Comprehensive Fiber Types
- Multiple fiber connector types (SC, FC, ST, MTRJ)
- Both single-mode (OS2) and multi-mode (OM4) cables
- Different fiber specifications and colors
- Demonstrates various optical characteristics

## Supported Features

### Fiber Types
- `single-mode`: Single-mode optical fiber
- `multi-mode`: Multi-mode optical fiber  
- `plastic`: Plastic optical fiber

### Fiber Attributes
- `core_diameter`: Core diameter in microns (e.g., 9, 50, 62.5)
- `cladding_diameter`: Cladding diameter in microns (typically 125)
- `numerical_aperture`: NA for multi-mode fibers (e.g., 0.2, 0.275)
- `wavelength`: Operating wavelength(s) in nm (850, 1310, 1550, or list)
- `attenuation`: Signal loss in dB/km
- `bandwidth`: Bandwidth in MHz·km (multi-mode only)

### Fiber Color Codes
- `FIBER12`: Standard 12-fiber color sequence
- `FIBER24`: 24-fiber color sequence (2 groups of 12)

### Common Fiber Specifications
- **OS2 Single-Mode**: 9/125μm, 1310nm/1550nm, yellow jacket
- **OM1 Multi-Mode**: 62.5/125μm, 850nm/1300nm, orange jacket
- **OM2 Multi-Mode**: 50/125μm, 850nm/1300nm, orange jacket  
- **OM3 Multi-Mode**: 50/125μm, 850nm, aqua jacket, laser-optimized
- **OM4 Multi-Mode**: 50/125μm, 850nm, aqua jacket, extended reach
- **OM5 Multi-Mode**: 50/125μm, 850nm/950nm, lime green jacket, wideband

## Usage

```yaml
cables:
  F1:
    category: fiber              # Required for optical fiber
    type: OS2 G.652.D           # Descriptive type
    fiber_type: single-mode     # single-mode, multi-mode, or plastic
    core_diameter: 9            # Core diameter in microns
    cladding_diameter: 125      # Cladding diameter in microns
    wavelength: [1310, 1550]    # Operating wavelengths in nm
    attenuation: 0.4            # Signal loss in dB/km
    length: 50                  # Cable length
    wirecount: 2                # Number of fibers
    colors: [YE, YE]           # Fiber colors
```

The fiber specifications will be automatically displayed in the cable diagram as "9/125μm SM 1310/1550nm" for single-mode or "50/125μm MM 850nm NA 0.2" for multi-mode fibers.