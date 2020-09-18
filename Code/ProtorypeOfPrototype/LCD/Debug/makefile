################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Prototype_Covid.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Prototype_Covid.list \

OBJCOPY_BIN += \
Prototype_Covid.bin \


# All Target
all: Prototype_Covid.elf secondary-outputs

# Tool invocations
Prototype_Covid.elf: $(OBJS) $(USER_OBJS) /home/mmont/Documents/Universidad/DesafioCovid/Code/ProtorypeOfPrototype/Prototype_Covid/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "Prototype_Covid.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/mmont/Documents/Universidad/DesafioCovid/Code/ProtorypeOfPrototype/Prototype_Covid/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Prototype_Covid.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Prototype_Covid.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Prototype_Covid.list"
	@echo 'Finished building: $@'
	@echo ' '

Prototype_Covid.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Prototype_Covid.bin"
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
