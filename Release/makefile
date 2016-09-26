################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
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
LSS += \
Copy of LCD3_2-AutoWrap.lss \

FLASH_IMAGE += \
Copy of LCD3_2-AutoWrap.hex \

EEPROM_IMAGE += \
Copy of LCD3_2-AutoWrap.eep \

SIZEDUMMY += \
sizedummy \


# All Target
all: Copy\ of\ LCD3_2-AutoWrap.elf secondary-outputs

# Tool invocations
Copy\ of\ LCD3_2-AutoWrap.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: AVR C Linker'
	avr-gcc -Wl,-Map,Copy of LCD3_2-AutoWrap.map -mmcu=atmega328p -o "Copy of LCD3_2-AutoWrap.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

Copy\ of\ LCD3_2-AutoWrap.lss: Copy\ of\ LCD3_2-AutoWrap.elf
	@echo 'Invoking: AVR Create Extended Listing'
	-avr-objdump -h -S Copy of LCD3_2-AutoWrap.elf  >"Copy of LCD3_2-AutoWrap.lss"
	@echo 'Finished building: $@'
	@echo ' '

Copy\ of\ LCD3_2-AutoWrap.hex: Copy\ of\ LCD3_2-AutoWrap.elf
	@echo 'Create Flash image (ihex format)'
	-avr-objcopy -R .eeprom -R .fuse -R .lock -R .signature -O ihex Copy of LCD3_2-AutoWrap.elf  "Copy of LCD3_2-AutoWrap.hex"
	@echo 'Finished building: $@'
	@echo ' '

Copy\ of\ LCD3_2-AutoWrap.eep: Copy\ of\ LCD3_2-AutoWrap.elf
	@echo 'Create eeprom image (ihex format)'
	-avr-objcopy -j .eeprom --no-change-warnings --change-section-lma .eeprom=0 -O ihex Copy of LCD3_2-AutoWrap.elf  "Copy of LCD3_2-AutoWrap.eep"
	@echo 'Finished building: $@'
	@echo ' '

sizedummy: Copy\ of\ LCD3_2-AutoWrap.elf
	@echo 'Invoking: Print Size'
	-avr-size --format=avr --mcu=atmega328p Copy of LCD3_2-AutoWrap.elf
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(FLASH_IMAGE)$(ELFS)$(OBJS)$(ASM_DEPS)$(EEPROM_IMAGE)$(S_DEPS)$(SIZEDUMMY)$(S_UPPER_DEPS)$(LSS)$(C_DEPS) "Copy of LCD3_2-AutoWrap.elf"
	-@echo ' '

secondary-outputs: $(LSS) $(FLASH_IMAGE) $(EEPROM_IMAGE) $(SIZEDUMMY)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
