# Dockitup_assignment
my assignment for dockitup
Assignment-1
# Dockitup Assignment – 1



---

## Steps Performed

### Step 1: Create HTML File
Created an `index.html` file containing basic static content.

---

### Step 2: Write Dockerfile
Created a `Dockerfile` to serve the `index.html` file using **Nginx**.

---

### Step 3: Build Docker Image
Built a Docker image from the Dockerfile using the command:

```bash
docker build -t srida-site .
```
---
### Step 4: Run Docker Container

Started a container named srida-container from the created image and exposed it on port 7070:
```bash
docker run -d --name srida-container -p 7070:80 srida-site
```
### Step 5: Verify Using curl

Verified that the container is running correctly using:
```bash
curl http://localhost:7070
```
output of curl
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b9d4a57b-ef9f-4ac9-b6c3-c0d26ce5b957" />
and localhost is
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7e40ed26-df40-49b1-a732-276f4748646c" />
container is
<img width="1920" height="1080" alt="Screenshot (1093)" src="https://github.com/user-attachments/assets/f250c3a2-9048-403c-a011-729adb972a09" />


# Dockitup Assignment – 1



---

## Steps Performed
### Step-1:created docker network using command
```bash
docker network create webnet
```
### Step-2:reate a simple API container with command
```bash
docker run -d --name api --network webnet hashicorp/http-echo -text="Hello from API"
```

### step-3:Wrote a index.html file and ngnix.config and docker file

### Step-4 then build a image called web using command
```bash
docker build -t web .
```
### Step-5 Then created a container ngnix connected to web image using command
```bash
docker run -d --name ngnix --network webnet -p 8080:80 web
```
### Step-6:Then tested the connection using the following curl command
```bash
docker exec -it ngnix curl http://api:5678
```

Output is
<img width="1206" height="73" alt="image" src="https://github.com/user-attachments/assets/eeef9771-0131-4eb2-b30d-f967703a5d56" />

containers are
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9df90c4b-f8a1-4982-8224-e52fb717e506" />
<img width="1282" height="134" alt="image" src="https://github.com/user-attachments/assets/2e7f3d36-49c5-4adc-92a5-e6ac4c0f7852" />
and in port before clicking
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b28aa0b0-7e5a-41fe-be7b-4e40c46026bc" />
after clicking
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/18d4bf34-e48f-4f13-a61d-d0e182b1d937" />







