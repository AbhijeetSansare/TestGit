################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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
bitfieldstructure.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
bitfieldstructure.list \

OBJCOPY_BIN += \
bitfieldstructure.bin \


# All Target
all: bitfieldstructure.elf secondary-outputs

# Tool invocations
bitfieldstructure.elf: $(OBJS) $(USER_OBJS) D:\Embedded\ System\ Development\Embedded\ C\ Course\My_workspace\bitfieldstructure\STM32F446RETX_FLASH.ld
	arm-none-eabi-gcc -o "bitfieldstructure.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Embedded System Development\Embedded C Course\My_workspace\bitfieldstructure\STM32F446RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="bitfieldstructure.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

bitfieldstructure.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "bitfieldstructure.list"
	@echo 'Finished building: $@'
	@echo ' '

bitfieldstructure.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "bitfieldstructure.bin"
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
