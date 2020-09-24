################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/FreeRTOS/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/subdir.mk
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
nucleo-f401re-freertos-drone.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
nucleo-f401re-freertos-drone.list \

OBJCOPY_BIN += \
nucleo-f401re-freertos-drone.bin \


# All Target
all: nucleo-f401re-freertos-drone.elf secondary-outputs

# Tool invocations
nucleo-f401re-freertos-drone.elf: $(OBJS) $(USER_OBJS) C:\SOFT\bis\do_przeniesienia\repozytoria\drone\nucleo-f401re-freertos-drone\STM32F401RETX_FLASH.ld
	arm-none-eabi-gcc -o "nucleo-f401re-freertos-drone.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\SOFT\bis\do_przeniesienia\repozytoria\drone\nucleo-f401re-freertos-drone\STM32F401RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="nucleo-f401re-freertos-drone.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

nucleo-f401re-freertos-drone.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "nucleo-f401re-freertos-drone.list"
	@echo 'Finished building: $@'
	@echo ' '

nucleo-f401re-freertos-drone.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "nucleo-f401re-freertos-drone.bin"
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
