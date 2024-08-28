A simple blink example to use FreeRTOS in Raspberry Pi Pico. FreeRTOS-Kernel is added as a git submodule in the `third_party` directory.

## Compile
`bazel build --platforms=@pico-sdk//bazel/platform:rp2040 //:freertos_blink`

## Flash
`openocd -f interface/cmsis-dap.cfg -f target/rp2040.cfg -c "adapter speed 5000" -c "program bazel-bin/freertos_blink verify reset
 exit"`

## References
* https://github.com/FreeRTOS/FreeRTOS-Kernel/blob/main/portable/ThirdParty/GCC/RP2040/README.md
* https://github.com/FreeRTOS/FreeRTOS-SMP-Demos/tree/main/FreeRTOS/Demo/CORTEX_M0%2B_RP2040
