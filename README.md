<!--

 Copyright (C) 2019 Intel Corporation
 Copyright (C) 2019 IOTech Ltd
 SPDX-License-Identifier: Apache-2.0

-->

# EdgeX Test Automation Framework Common ( edgex-taf-common )

## Overview
Contains common code or scripts such as TUC which will be common for all the project specific TAF code.
TUC - Test Util Catalog.

# Usage

1. Create a edgex-taf project which contains a TAF folder.
2. Install required lib:
    ```shell script
    pip3 install git+ssh://git@github.com:edgexfoundry/edgex-taf-common.git
    pip3 install -r requirements.txt
    ```
   
    Then your project structure will be:
    ```
    edgex-taf-project
    ├── TAF
    │   ├── README.md
    │   ├── __init__.py
    │   ├── config
    │   ├── testArtifacts
    │   ├── testCaseApps
    │   ├── testScenarios
    │   └── utils
    ├── .gitignore
    ├── .gitmodules
    ├── Jenkinsfile
    ├── README.md
    ```
3. Run test scripts via the edgex-taf-common:
    ```shell script
    # Run use cases
    python3 -m TUC -u UC_coredata -u UC_metadata
    
    # Run test cases
    python3 -m TUC -t UC_coredata/event.robot -t UC_metadata/device.robot
    ```
   
4. Develop with IDE

   Since we use edgex-taf-common as module, we need to add it to the IDE. [For the pycharm example, add interpreter paths.](https://www.jetbrains.com/help/pycharm/installing-uninstalling-and-reloading-interpreter-paths.html)

5. Build docker image
    ```shell script
    docker build .
    ```

## Community
- Chat: https://edgexfoundry.slack.com
- Mailing lists: https://lists.edgexfoundry.org/mailman/listinfo

## License
[Apache-2.0](LICENSE)
