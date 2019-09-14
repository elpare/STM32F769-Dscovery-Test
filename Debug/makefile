################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM7/r0p1/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
-include Drivers/STM32F769I-Discovery/subdir.mk
-include Drivers/Components/wm8994/subdir.mk
-include Drivers/Components/ts3510/subdir.mk
-include Drivers/Components/stmpe811/subdir.mk
-include Drivers/Components/st7789h2/subdir.mk
-include Drivers/Components/st7735/subdir.mk
-include Drivers/Components/s5k5cag/subdir.mk
-include Drivers/Components/ov9655/subdir.mk
-include Drivers/Components/otm8009a/subdir.mk
-include Drivers/Components/mfxstm32l152/subdir.mk
-include Drivers/Components/ft6x06/subdir.mk
-include Drivers/Components/ft5336/subdir.mk
-include Drivers/Components/exc7200/subdir.mk
-include Drivers/Components/adv7533/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(CC_DEPS)),)
-include $(CC_DEPS)
endif
ifneq ($(strip $(C++_DEPS)),)
-include $(C++_DEPS)
endif
ifneq ($(strip $(C_UPPER_DEPS)),)
-include $(C_UPPER_DEPS)
endif
ifneq ($(strip $(CXX_DEPS)),)
-include $(CXX_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
ifneq ($(strip $(CPP_DEPS)),)
-include $(CPP_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
769FileTest.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
769FileTest.list \


# All Target
all: 769FileTest.elf secondary-outputs

# Tool invocations
769FileTest.elf: $(OBJS) $(USER_OBJS) C:\CUBEIDEPROJECTS\769FileTest\STM32F769NIHX_FLASH.ld
	arm-none-eabi-g++ -o "769FileTest.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"C:\CUBEIDEPROJECTS\769FileTest\STM32F769NIHX_FLASH.ld" --specs=nosys.specs -Wl,-Map="769FileTest.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -lstdc++ -lsupc++ -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

769FileTest.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "769FileTest.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
