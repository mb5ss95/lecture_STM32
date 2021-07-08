################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
lec11_mymy.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
lec11_mymy.list \

OBJCOPY_BIN += \
lec11_mymy.bin \


# All Target
all: lec11_mymy.elf secondary-outputs

# Tool invocations
lec11_mymy.elf: $(OBJS) $(USER_OBJS) C:\Users\moon\STM32CubeIDE\workspace_1.3.0\lec11_mymy\STM32F401RETX_FLASH.ld
	arm-none-eabi-gcc -o "lec11_mymy.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\moon\STM32CubeIDE\workspace_1.3.0\lec11_mymy\STM32F401RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="lec11_mymy.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

lec11_mymy.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "lec11_mymy.list"
	@echo 'Finished building: $@'
	@echo ' '

lec11_mymy.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "lec11_mymy.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
