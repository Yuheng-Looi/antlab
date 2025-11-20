First, clone the repo.
Then follow the steps below to import the image. From the repo you get `IOSvL2.yaml` and a `.qcow2` image file.

1. Login to the CML web UI, go to `TOOLS` -> `Node and Image Definitions`.

	![Tools -> Node and Image Definitions](images/firstpage.png)

2. Click `Import` on the upper right, beside the `Add` button.

	![Import button](images/import.png)

3. Click the node definition field to open the File Explorer, select `IOSvL2.yaml` from this repo, then click `Import`.

	![Select YAML to import](images/importyaml.png)

4. After the import completes click the `GO TO NODE DEFINITION` button.

	![Go to node definition](images/gotodefinition.png)

5. Click `CREATE NEW IMAGE DEFINITION`.

	![Create new image definition](images/createimage-button.png)

6. Click `MANAGE IMAGE UPLOADS` (or similar) to upload the disk image.

	![Manage image uploads](images/manageImageUploads.png)

7. Click the Image File field, choose the provided `vios_l2-adventerprisek9-m.ssa.high_iron_20200929.qcow2` and upload it.

	![Upload qcow2 file](images/uploadqcow.png)

8. When the upload finishes you should see the file listed under **Uploaded Images**.

	![Uploaded image listed](images/qcowuploaded.png)

9. Click back to return to the Image Definition Editor. Select the imported node definition (the IOSvL2 node) as the **Node Definition** and choose the uploaded `.qcow2` file as the **Disk Image**. Fill in the `ID`, `Label`, and `Description` for the image definition.

	![Image definition editor](images/nodedefinition.png)

10. Then scroll down to click `CREATE IMAGE DEFINITION`.

11. You will now see the new node in `TOOLS` -> `Node and Image Definitions` and it should be available in the topology editor's node palette.

	![New node available](images/final.png)

TESTING

- Add the new IOSvL2 node to a topology, connect it to other nodes and start the lab.
- Open the node console and apply a small configuration change, then save the running configuration.
- If you see "written to disk successfully" when saving, the node is functioning and configuration persistence is working.

	![Save running config confirmation](images/save.png)