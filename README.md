# VM Lifecycle on GCP and OCI — Tutorial

## GCP Video link
Loom GCP video tutuorial of creating a Virtual Machine: https://protect.checkpoint.com/v2/r01/___https://www.loom.com/share/c2535e52010541b2978139b8389dd6cd?t=293&sid=eb4f503a-8f04-4e2e-948c-a8f8a7c9ad5b__



## Loom OPI video: 
Below is a link to the video file in which we are exploring the Oracle platform of building a Virtual Machine https://www.loom.com/share/2e324cb606b141b4a78f94b4a90d96cf?sid=42b060c4-7599-40bb-8cae-97ede9afe10a ]


## Prereqs
- Cloud access to GCP and OCI
- No PHI/PII; smallest/free-tier shapes

---

## Google Cloud (GCP)
### Create
1. Console → Compute Engine → Create instance
2. Region/zone: <your choice>
3. Machine type: <smallest available/free-eligible>
4. Image: Ubuntu LTS
5. Boot disk: default minimal
6. Network: default VPC; ephemeral public IP

![GCP create](<Screenshot 1GCP.png>)


### Start/Stop
- Start: <state shows RUNNING>
- Stop: <state shows TERMINATED/STOPPED>

![GCP running](<Screenshot 2GCP.png>)


### Delete
- Delete instance and verify no disks/IPs remain

![GCP cleaned](<Screenshot 3GCP.png>)


---

## Oracle Cloud (OCI)
### Create
1. Compartment: <name>
2. Networking: VCN with Internet Connectivity (defaults)
3. Shape: <smallest/free-eligible>
4. Image: Ubuntu (or Oracle Linux)
5. Public IP: ephemeral
6. Boot volume: default minimal

![OCI create](<Screenshot 1oracle.png>)



### Start/Stop
- Start: <state shows RUNNING>
- Stop: <state shows STOPPED>
![OCI running](<Screenshot 3POI.png>)
![OCI running](<Screenshot opi4.png>)


### Terminate
- Terminate and delete boot volume; verify cleanup
- 
![OIlt text](<Screenshot opi5.png>)


---

## Reflections
### Similarities
Creating virtual machines in Google Cloud Platform (GCP) and Oracle Cloud Infrastructure (OCI) follows similar fundamental steps: both platforms require selecting a machine type/shape, choosing an operating system image (like Ubuntu), and managing the VM lifecycle through start, stop, and termination operations. Both services also emphasize free-tier eligible options and provide web-based console interfaces for management, though their specific implementations and user experience differ.

### Differences
Google definitely simplifies the VM creation process with less steps involved and has a friendlier user interface
Oracle has many additional required steps that are needed in order to create a virtul machine such as configuring networking with a VPC and public IP, setting up minimal boot volumes.
Oracle also takes a bit longer to to terminate.

### Preference (OCI vs GCP) and Why
  I prefer GCP for a seamless VM creation instance for its easy to use steps and easy operation of terminating the VM once the service is no longer needed.