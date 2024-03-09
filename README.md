# OTP Module for Spring Boot Rest API

<ul>
<li><p>I have developed OTP module</p></li>
<li><p>Spring Boot, Rest API</p></li>
</ul>

### Set up Twilio Account:

<p> If you haven't already, sign up for a Twilio account at <a href="https://www.twilio.com/" title="twilio">
Twilio </a> link. </p>
<p> Once signed up, navigate to the Twilio Console to obtain your Account SID and Auth Token. These credentials will be used to authenticate requests to Twilio's API. </p>

### Verify Email Sender:

<p> In the Twilio Console, verify the email address you'll be using to send emails. This is to ensure compliance with email regulations and to avoid messages being flagged as spam.</p>

#### <p>This is a Properties File:</p>

<pre><code>
# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/yourdb
spring.datasource.username=root
spring.datasource.password=password

spring.jpa.hibernate.ddl-auto=update

# Gmail SMTP Server Configuration
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=yourgmail@gmail.com
spring.mail.password=gmailGeneratedPassword
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true
</code></pre>

## Postman

<p> POST Email register </p>

<pre><code>http://localhost:8080/api/register</code></pre>
<pre><code>
{
  "name": "John Doe",
  "email": "youremail@gmail.com",
  "password": "password",
  "mobile": "0"
}
</code></pre>

<p> POST verify Otp </p>

<pre><code>http://localhost:8080/api/verify-otp-for-login?email=youremail@gmail.com&otp=296607</code></pre>

#### Thanks for visiting
