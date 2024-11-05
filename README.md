## ImageResize
The project aims at RESIZING a still image, first using Processing System (PS) using Python on an ARM9 processor, and the other executed in hardware using a kernel contained within a hardware overlay in the Programmable Logic (PL).

## Technical Description

### PS Implementation (Python on ARM9):
- The `RESIZE` function is executed on the ARM9 processor within the Processing System (PS).
- The ARM9 processor accesses the input image and performs the `RESIZE` operation using Python code.
- The `RESIZE` operation involves resampling the input image and applying filtering/interpolation techniques to generate the output image.
- The execution time of the `RESIZE` function is measured on the ARM9 processor.

### Hardware Implementation (PL with Hardware Overlay):
- The `RESIZE` function is implemented in hardware using a kernel contained within a hardware overlay in the Programmable Logic (PL).
- The input image is passed from the ARM9 processor to the DDR Memory (DRAM).
- The `Resize IP` block is configured to execute the `RESIZE` function within the hardware overlay.
- The DMA controller is set up to transfer source pixels from DRAM to the `Resize IP` block and to transfer destination pixels from the `Resize IP` block back to DRAM.
- The ARM9 processor can access the resulting resized image stored in DRAM after the hardware acceleration.

## Observation:
- FPGA implementation is X4 times faster than Software Implementation.

---
