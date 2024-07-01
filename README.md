import yagmail

def create_newsletter():
    # Compose your HTML newsletter content
    html_content = """
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Special Offer Form</title>
</head>
<body style="background-color: #FFFFFF; font-family: Arial, sans-serif;">
  <div style=" background-color: #FFFFFF;">
    <h1 style="color: #333333;">Welcome to Our Company!</h1>
    <p style="color: #666666;">Dear Student,</p>
    <p style="color: #666666;">We're excited to offer you an exclusive internship in our Company!</p>
    <p style="color: #666666;">Your commitment to advancing your knowledge and skills is truly commendable, and we are thrilled to have you join our learning community.</p>
   <form action="https://script.google.com/macros/s/AKfycbxUQs859bDvvvLR8oHBdQV8qvOp-F51T7PkpoovvzHxfWTWjZah8p_Wi8OngF2WKPFZVw/exec" method="get" style="background-color:#FFA500; padding: 20px; border-radius: 5px;">
      <label for="name" style="font-weight: bold;">Name:</label>
      <input type="text" id="name" name="name" required style="width: 100%; padding: 10px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box;">
      <label for="email" style="font-weight: bold;">Email:</label>
      <input type="email" id="email" name="email" required style="width: 100%; padding: 10px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box;">

      <label for="how" style="font-weight: bold;">How did you hear about us?</label>
      <select id="how" name="how" required style="width: 100%; padding: 10px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box;">
        <option value="">Select</option>
        <option value="Search engine">Search engine</option>
        <option value="Social media">Social media</option>
        <option value="Word of mouth">Word of mouth</option>
        <option value="Advertisement">Advertisement</option>
        <option value="Other">Other</option>
      </select>

      <label for="why" style="font-weight: bold;">Choose your interested Domain:</label>
      <select id="why" name="why" required style="width: 100%; padding: 10px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box;">
        <option value="">Select</option>
        <option value="JAVA">JAVA</option>
        <option value="PYTHON">PYTHON</option>
        <option value="DATA SCIENCE">DATA SCIENCE</option>
        <option value="DATA STRUCTURE">DATA STRUCTURE</option>
        <option value="Other">Other</option>
      </select>
       <label for="duration">How long do you intend to work with us?</label><br>
       <select id="duration" name="duration" required style="width: 100%; padding: 10px; margin-bottom: 15px; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box;">
    <option value="">Select</option>
    <option value="less_than_1_month">Less than 1 month</option>
    <option value="1_to_3_months">1 to 3 months</option>
    <option value="3_to_5_months">3 to 5 months</option>
    <option value="more_than_5_months">More than 5 months</option>
    <option value="indefinitely">Indefinitely</option>
  </select>
      <input type="submit" value="Submit" style="background-color: #4CAF50; color: white; padding: 15px 25px; text-align: center; text-decoration: none; display: inline-block; border: none; border-radius: 5px; cursor: pointer;">
    </form>
    <p style="color: #666666;">Best regards,<br>Your Organisation</p>
  </div>
</body>
</html>
    """
    return html_content
    
def send_newsletter(html_content):
    # Initialize Yagmail with your Gmail credentials
    yag = yagmail.SMTP('invitha1234@gmail.com', 'ehuv velp jnaf ybxh')

    # Send the newsletter to your subscribers
    yag.send(
        to=['induendluri@gmail.com','chitrasreelakshmi@gmail.com','deepeshp.j.2004@gmail.com','bhopibhavitha@gmail.com'],
        subject='GREETINGS FROM SURE TRUST',
        contents=html_content
    )

    # Close the Yagmail connection
    yag.close()

if __name__ == "__main__":
    newsletter_content = create_newsletter()
    send_newsletter(newsletter_content)
