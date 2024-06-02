# Setup Instructions

## Clone repositories
```bash
git clone https://github.com/vignesh4995/apigateway.git
git clone https://github.com/vignesh4995/claim_process.git
git clone https://github.com/vignesh4995/payment.git
```

##Create Docker network
```bash
docker network create my_network
```

##Set up and run apigateway service
```bash
cd apigateway
docker-compose up --build -d
cd ..
```

##Set up and run claim_process service
```bash
cd claim_process
docker-compose up --build -d
cd ..
```

##Set up and run payment service
```bash
cd payment
docker-compose up --build -d
cd ..
```

##Verify Docker containers
```bash
docker ps
```

Test Instructions
Using venv (built into Python 3.3+):
Create a virtual environment:
bash
Copy code
python -m venv env_name
macOS/Linux:
bash
Copy code
source env_name/bin/activate
Install test dependencies and run tests for claim_process:
Go to the test directory of claim_process:
bash
Copy code
cd claim_process/test
Install the requirements:
bash
Copy code
pip install -r requirements.txt
Run the tests:
bash
Copy code
python3 test_claims.py
By following these instructions, you can set up, run, and test the services to ensure the claim processing and data publishing to RabbitMQ are working as expected.

