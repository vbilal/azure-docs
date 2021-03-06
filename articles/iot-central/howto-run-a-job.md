---
title: Create and run jobs in your Azure IoT Central application | Microsoft Docs
description: Azure IoT Central jobs allow for bulk device management capabilities, such as updating a device property, setting, or executing a command.
ms.service: iot-central
services: iot-central
author: sarahhubbard
ms.author: sahubbar
ms.date: 03/18/2019
ms.topic: conceptual
manager: peterpr
---

# Create and run a job in your Azure IoT Central Application

You can use Microsoft Azure IoT Central to manage your connected devices at scale using jobs. The jobs functionality enables you to perform bulk updates to device properties, settings, and commands. This article walks you through how to get started using jobs in your own application.

## Create and run a job

This section shows you how to create and run a job. Each step goes through an example that demonstrates how to run a job for refrigerated vending machine devices that need to have their fan speed increased.

1. Navigate to Jobs from the navigation pane.

1. Select **+ New** in order to start creating a new job.

    ![Create new job](./media/howto-run-a-job/createnewjob.png)

1. Enter a name and description that help you identify the job you are creating.

1. Select the device set you want your job to be applied to. After selecting the device set, you see the right-hand side populate with the devices within the selected device set. If you select a broken device set, no devices display and you see a message explaining that your device set is broken.

1. Next, choose the type of job to define (a setting, property, or command). Select **+** next to the type of job selected and add your desired operations.

    ![Configure job](./media/howto-run-a-job/configurejob.png)

1. On the right-hand side, pick and choose the devices you’d like to run the job on. By selecting the top check box, all devices are selected in the entire device set. By selecting the check box near **Name**, all devices on the current page are selected.

1. After selecting your devices, choose **Run** or **Save**. The job now appears on your main **Jobs** page. On this view, you can see your currently running job and the history of any previously run jobs. Your running job always shows up at the top of the list. Your saved job can be opened again at any time to continue editing or to run.

    ![View job](./media/howto-run-a-job/viewjob.png)

    > [!NOTE]
    > You can view the history of your previously run jobs for up to 30 days.

1. To get an overview of your job, select the job name you wish to view from the list. This overview contains the job details, devices, and device status values. From this overview, you can also select **Download Job Details** to download a .csv file of your job details, including the devices and their status values. This information can be useful for troubleshooting.

    ![View device status](./media/howto-run-a-job/downloaddetails.png)

### Stop a running job

If you would like to stop a job that is currently running, select the name of the running job that you would like to stop. Choose the **Stop** button on the panel. You’ll see the job status has changed to reflect that the job has been stopped.

   ![Stop job](./media/howto-run-a-job/stopjob.png)

### Run a stopped job

To run a job that is currently stopped, select the name of the stopped job that you would like to run. Choose the **Run** button on the panel. The job status changes to reflect that the job is now running again.

   ![Resumed job](./media/howto-run-a-job/resumejob.png)

## Copy a job

To copy an existing job you've created, select it from the main jobs page and select **Copy**. This opens a new copy of the job configuration for you to edit. You can save or run the new job. If any changes have been made to your selected device set, they are reflected in this copied job for you to edit.

   ![Copy job](./media/howto-run-a-job/copyjob.png)

## View the job status

After a job has been created, the **Status** column updates with the latest status message of the job. The status messages mean the following:

| Status message       | Status meaning                                          |
| -------------------- | ------------------------------------------------------- |
| Completed            | This job has been executed on all devices.              |
| Failed               | This job has failed and not fully executed on devices.  |
| Pending              | This job has not yet begun executing on devices.        |
| Running              | This job is currently executing on devices.             |
| Stopped              | This job has been manually stopped by a user.           |

The status message is followed by an overview of the devices within the job. These device statuses mean the following:

| Status message       | Status meaning                                                     |
| -------------------- | ------------------------------------------------------------------ |
| Succeeded            | The number of devices which the job has successfully executed on.  |
| Failed               | The number of devices which the job has failed to execute on.      |

### View the device status

To view the status of each device in the job, select the job name. You see the details of the job and all of the devices that were a part of it. You can select **Download job details** to download a .csv file that includes the job details, the devices and their status values. Next to each device name, you see one of the following status messages:

| Status message       | Status meaning                                                                |
| -------------------- | ----------------------------------------------------------------------------- |
| Completed            | The job has been executed on this device.                                     |
| Failed               | The job has failed to execute on this device. The accompanying error message shows more information.  |
| Pending              | The job has not yet executed on this device.                                  |

> [!NOTE]
> If a device has been deleted, you can't select the device and it displays as deleted with the device ID.

## Next steps

Now that you have learned how to create jobs in your Azure IoT Central application, here are some next steps:

- [Use device sets](howto-use-device-sets.md)
- [Manage your devices](howto-manage-devices.md)
- [Version your device template](howto-version-devicetemplate.md)
