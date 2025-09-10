# VM Lifecycle on GCP and OCI — Tutorial

## Video
Loom/Zoom: <pashttps://protect.checkpoint.com/v2/r01/___https://www.loom.com/share/c2535e52010541b2978139b8389dd6cd?t=293&sid=eb4f503a-8f04-4e2e-948c-a8f8a7c9ad5b___.YzJ1OnN0b255YnJvb2s6YzpnOmZhZTVlN2ViNmU2NGY5OWZjMTc3NmFmM2FmM2VkMTZiOjc6M2EzMTo1M2MxMmQ4Yzk3YTUwMTA4NDdlMDJlOTljYWRhOTlmNWI2MjM3ZDE0NmI5ZTMwNmY5NGRkYmJiOGUzM2EzNjE0Omg6VDpG>

<(https://protect.checkpoint.com/v2/r01/___https://www.loom.com/share/c2535e52010541b2978139b8389dd6cd?t=293&sid=eb4f503a-8f04-4e2e-948c-a8f8a7c9ad5b___.YzJ1OnN0b255YnJvb2s6YzpnOmZhZTVlN2ViNmU2NGY5OWZjMTc3NmFmM2FmM2VkMTZiOjc6M2EzMTo1M2MxMmQ4Yzk3YTUwMTA4NDdlMDJlOTljYWRhOTlmNWI2MjM3ZDE0NmI5ZTMwNmY5NGRkYmJiOGUzM2EzNjE0Omg6VDpG)>

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

![OCI cleaned](<Screenshot opi5.png)

---

## Reflections
### Similarities
- <brief bullets>

### Differences
- <brief bullets>

### Preference (OCI vs GCP) and Why
- <one short paragraph>