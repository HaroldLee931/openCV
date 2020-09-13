# Place Holder

## Install OpenCV

- Install with Python Only
  - MacOS

    ```bash  
        # Perpare Python3
        brew install python3
        brew link python3
        brew upgrade python3 #(Anaconda is more recommend)
        which python3
        # install opencv
        cvVersion="4.1.0"
        cwd=$(pwd)
        # create virtual environment
        python3 -m venv OpenCV-"$cvVersion"-py3
        echo "# Virtual Environment Wrapper" >> ~/.bash_profile
        echo "alias workoncv-$cvVersion=\"source $cwd/OpenCV-$cvVersion-py3/bin/activate\"" >> ~/.bash_profile
        source "$cwd"/OpenCV-"$cvVersion"-py3/bin/activate

        # now install python libraries within this virtual environment
        pip install wheel numpy scipy matplotlib scikit-image scikit-learn ipython

        # quit virtual environment
        deactivate

        # Install openCV
        source ~/.bash_profile
        # Activate virtual environment
        workoncv-4.1.0
        # Install OpenCV and Dlib modules
        pip install opencv-contrib-python==4.1.0.25

        # Verify
        ipython
    ```

    ```python
        import cv2
        print(cv2.__version__)
        # If OpenCV is installed correctly, the above command should give output 4.1.0
    ```

    ```bash
        deactivate
    ```

  - Ubuntu 16/18 (I haven't verify it on 20 I used anaconda env with pip install)

    ```bash
        sudo apt -y update
        sudo apt -y upgrade

        sudo apt-get install python3-dev python3-pip python3-venv
        sudo -H pip3 install -U pip numpy
        sudo apt-get install libx11-dev libgtk-3-dev libboost-python-dev
        sudo apt-get install python3-testresources
        sudo apt-get install build-essential checkinstall cmake pkg-config yasm

        # setup virtual env (same as MacOS)
        # Done
        # Install openCV with pip (same as MacOS)
        # Done
        # Check install (same as MacOS)
    ```

  - With anaconda

    ```bash
        pip install cmake
        pip install numpy scipy matplotlib scikit-learn jupyter ipython
        pip install opencv-contrib-python==4.1.0.25
        # If you see ERROR like this:
        # ERROR: Could not find a version that satisfies the requirement opencv-contrib-python==4.1.0.25 (from versions: 3.4.8.29, 3.4.9.31, 3.4.9.33, 3.4.10.35, 3.4.10.37, 3.4.11.39, 3.4.11.41, 4.1.2.30, 4.2.0.32, 4.2.0.34, 4.3.0.36, 4.3.0.38, 4.4.0.40, 4.4.0.42)
        # ERROR: No matching distribution found for opencv-contrib-python==4.1.0.25
        # Just modify the version Number
        conda install -c conda-forge dlib
    ```

- Install with Docker(TODO)
- Install from source(not recommend unless you are familiar with CLI)

## Vocabulary

interpolating


## Play Docker

- install docker