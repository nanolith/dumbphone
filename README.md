"Dumb" phone
------------

The "dumb" phone project is my attempt to build a simple cellular phone from an
ARMv7 Cortex-M architecture and off-the-shelf components.  The phone performs
basic services (voice and SMS) along with some integrations with some of my
other IoT projects.

At the core of this project is an NXP / Freescale Kinetis MCU with support for
an MPU and SDRAM.  A simple OS on this MCU provides the ability to run separate
processes and to run both drivers and services as user space processes.  This
isn't the most performant setup, but it provides a high degree of process
isolation, which ensures better stability and security.  The OS consists of a
simple microkernel that can pass messages and notifications between processes.
Any supervisor specific lifting is performed by this microkernel, but everything
else happens in user space.
