Quick Start
===============================

Setting up the Chipyard Repo
-------------------------------------------

Start by fetching Chipyard's sources. Run:

.. code-block:: shell

    git clone https://github.com/ucb-bar/chipyard.git
    cd chipyard
    ./scripts/init-submodules-no-riscv-tools.sh

This will have initialized the git submodules.

Installing the RISC-V Tools
-------------------------------------------

We need to install the RISC-V toolchain in order to be able to run RISC-V programs using the Chipyard infrastructure.
This will take about 20-30 minutes. You can expedite the process by setting a ``make`` environment variable to use parallel cores: ``export MAKEFLAGS=-j8``.
To build the toolchains, you should run:

.. code-block:: shell

    ./scripts/build-toolchains.sh

.. Note:: If you are planning to use the Hwacha vector unit, or other RoCC-based accelerators, you should build the esp-tools toolchains by adding the ``esp-tools`` argument to the script above.
  If you are running on an Amazon Web Services EC2 instance, intending to use FireSim, you can also use the ``--ec2fast`` flag for an expedited installation of a pre-compiled toolchain.

Finally, set up Chipyard's environment variables and put the newly built toolchain on your path:

.. code-block:: shell

    source ./env.sh

What's Next?
-------------------------------------------

This depends on what you are planning to do with Chipyard.

* To learn about the structure of Chipyard, see :ref:`chipyard-components`.

* To build one of the vanilla Chipyard examples, see :ref:`build-a-chip`.

* To add a new accelerator, see :ref:`adding-an-accelerator`.

* To run a simulation of one of the Chipyard examples, see :ref:`sw-rtl-sim-intro`.

* To run a simulation of a custom Chipyard SoC Configuration, see <>.

* To run a FPGA-accelerated simulation using FireSim, see :ref:`firesim-sim-intro`.

* To run a VLSI flow using one of the vanilla Chipyard examples, see <>.
