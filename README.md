# buzzline-02-arnold

Streaming data is often too big for any one machine. Apache Kafka is a popular streaming platform that uses publish-subscribe patterns:

- **Producers** publish streaming data to topics
- **Consumers** subscribe to topics to process data in real-time


## Task 1. Fork project

1. Forked <https://github.com/denisecase/buzzline-02-case> into my GitHub account and created my own version of this project to run and experiment with.
2. Named my new project `buzzline-02-arnold`.

## Task 2. Start Kafka (using WSL if Windows)

In order to use kafka:
1. Ensure that Windows Subsystem for linux is installed and running.
2. Ensure Python 3.11 is install within WSL and our python virtual environment.
3. Ensure that kafka and all its dependencies are installed within WSL.
4. Ensure VS Code is installed.

start a local Kafka service with WSL using VS Code.

1. Start the Kafka server in the foreground
    ```cd ~/kafka```
    ```bin/kafka-server-start.sh config/kraft/server.properties```
2. Keep this terminal open - Kafka will run here
3. Watch for "started (kafka.server.KafkaServer)" message


## Task 3. Manage Local Project Virtual Environment

Open your project in VS Code and use the commands for your operating system to:

1. Create a Python virtual environment
    ```python -3.11 -m ven .venv```
2. Activate the virtual environment
        ```.venv\Scripts\Activate```
3. Upgrade pip
    ```python -m pip install --upgrade pip```
    ```py -m pip install --upgrade pip wheel setuptools```
4. Install from requirements.txt
    ```python -m pip install -r requirements.txt```

## Task 4. Start a Kafka Producer

Producers generate streaming data for our topics.

In VS Code, open a terminal.
Use the commands below to activate .venv, and start the producer.

Windows:

```shell
.venv\Scripts\activate
py -m producers.kafka_producer_arnold
```

## Task 5. Start a Kafka Consumer

Consumers process data from topics or logs in real time.

In VS Code, open a NEW terminal in your root project folder.
Use the commands below to activate .venv, and start the consumer.

Windows:

```shell
.venv\Scripts\activate
py -m consumers.kafka_consumer_case
```

## Later Work Sessions

When resuming work on this project:

1. Open the folder in VS Code.
2. Start the Kafka service.
3. Activate your local project virtual environment (.venv).

## Save Space

To save disk space, you can delete the .venv folder when not actively working on this project.
You can always recreate it, activate it, and reinstall the necessary packages later.
Managing Python virtual environments is a valuable skill.

## License

This project is licensed under the MIT License as an example project.
You are encouraged to fork, copy, explore, and modify the code as you like.
See the [LICENSE](LICENSE.txt) file for more.
