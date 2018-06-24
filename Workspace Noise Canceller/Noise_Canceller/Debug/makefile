################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: Noise_Canceller.axf

# Tool invocations
Noise_Canceller.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"C:\Users\Martin\Desktop\Proyecto PES\Workspace Noise Canceller\lpc_board_nxp_lpcxpresso_1769\Debug" -L"C:\Users\Martin\Desktop\Proyecto PES\Workspace Noise Canceller\lpc_chip_175x_6x\Debug" -Xlinker -Map="Noise_Canceller.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "Noise_Canceller_Debug.ld" -o "Noise_Canceller.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) Noise_Canceller.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "Noise_Canceller.axf"; # arm-none-eabi-objcopy -v -O binary "Noise_Canceller.axf" "Noise_Canceller.bin" ; # checksum -p LPC1769 -d "Noise_Canceller.bin";
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
