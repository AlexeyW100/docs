# Switch to another cloud

---

**[!TAB Management console]**

1. Click on the name of the current folder in the upper-right corner.

    ![image](../../../_assets/resource-manager/switch-cloud.png)

1. Choose the cloud or folder you want to switch to.

**[!TAB CLI]**

There are two ways to choose the cloud that is used in the CLI by default:

* Select the cloud during your [profile initialization](../../../cli/quickstart.md#initialize).
* Change the `cloud-id` parameter in the profile configuration.

To change the `cloud-id` parameter for the current profile:

1. See the description of the command to change configuration parameters:

    ```
    $ yc config set --help
    ```

2. Find out the ID of the cloud you want to use. To do this, get a list of available clouds:

    ```
    $ yc resource-manager cloud list
    +----------------------+----------------------+-------------------------------+
    |          ID          |         NAME         |          DESCRIPTION          |
    +----------------------+----------------------+-------------------------------+
    | b1gg8sgd16g7qch5onqs | cloud-b1gg8sgd1g23qc | ...                           |
    | b1gjqgj3hhvjen5iqakp | cloud-b1gjqgj3hhvjen | ...                           |
    +----------------------+----------------------+-------------------------------+
    ```

    > [!NOTE]
    >
    > If the list contains only one cloud, it means you don't have access to any other clouds. To access the cloud you need, ask the [owner](../../concepts/resources-hierarchy.md#owner) of that cloud to [add](../../../iam/operations/users/create.md) you to it.

3. Specify the ID of the cloud to be used by default:

    ```
    $ yc config set cloud-id b1gjqgj3hhvjen5iqakp
    ```

---

