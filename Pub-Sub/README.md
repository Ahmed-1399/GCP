# 🚀 Pub/Sub Guide

Welcome! This README will walk you through the basics of Google Cloud Pub/Sub: creating a topic, publishing messages, setting up subscriptions, and pulling messages.  
Let’s get started! 😃

---

## 🗂️ How Pub/Sub works?

- A publisher sends a message to a topic.
- Pub/Sub service stores and delivers the message.
- Subscribers receive the message via a subscription (either push or pull model).

![SNS = Pub/Sub](./assets/SNS.png)

---

## 📝 Create a Pub/Sub Topic

1. Go to **Solutions → All products → Analytics → Pub/Sub → Topics → Create topic**  
   ![Topic](./assets/Topic.png)

---

## ➕ Add a Subscription

1. Click **Create subscription**  
   ![subscription](./assets/Create-subscription.png)
2. Choose:
   ```
   Delivery type: Pull
   ```
3. Subscription created!  
   ![subscription](./assets/subscription.png)

---

## 📤 Publish a Message

1. Navigate to **pub/sub → Topics → <Topic-Name> → Messages → Publish Message "Hello World" → Publish**  
   ![Publish a message](./assets/Publish-Message.png)

---

## 👀 View (Pull) the Message

**From CLI:**  
```bash
gcloud pubsub subscriptions pull --auto-ack <Sub-Name>
```
![Pull CLI](./assets/Pull-Message.png)

**From Console:**  
1. Go to **pub/sub → Topics → Topic-Name → Messages**
2. Select a Cloud Pub/Sub subscription to pull messages
3. Choose subscription, enable "ack", and click **Pull**
![Pull Console](./assets/Pull.png)

---

## 💡 Tips & Best Practices

- 📨 A publisher application creates and sends messages to a **topic**. Subscriber applications create a **subscription** to the topic to receive messages.
- ☁️ Cloud Pub/Sub is an **asynchronous** messaging service designed to be highly reliable and scalable.

---

Happy Messaging! 🎉