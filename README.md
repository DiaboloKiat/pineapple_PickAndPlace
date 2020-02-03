# pineapple_PickAndPlace
1. roslaunch zed_wrapper zedm.launch (open the camera)
2. rosrun robotiq_2f_gripper_control Robotiq2FGripperRtuNode.py /dev/ttyUSBX (connect the gripper)
   !!! checking the gripper is in which " USBX "
3. (run FCN)
4. roslaunch arm_operation ur5_real.launch tool_length:=0.18 robot_ip:=192.168.50.11 (connect the robot arm)
5. rosrun tf static_transform_publisher x y z qx qy qz qw base_link zed_left_camera_frame 10
6. rosrun arm_operation goto_pose (connect the function)

rosrun tf static_transform_publisher -0.604356 -0.039378 0.738536 -0.488204 0.486056 0.502361 0.522532 base_link zed_left_camera_frame 10
