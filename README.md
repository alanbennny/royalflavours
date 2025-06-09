
# RoyalFlavours Food Delivery System

**Student Name:** Alan Benny  
**Student ID:** 35642348  
**Live Demo:** [royalflavours.store](https://royalflavours.store)  
**Public IP:** `13.250.220.174`  
**Domain Provider:** Namecheap.com  
**GitHub Repository:** [GitHub Repo](https://github.com/alanbennny/royalflavours)
**Video Explainer** https://murdochuniversity-my.sharepoint.com/:p:/g/personal/35642348_student_murdoch_edu_au/EXE5Z8Q7o9RGp-HTAd71LtcBTNbuMTr36lXVT7doz-96TQ?e=IJmqX9

---

## 🌐 Overview

RoyalFlavours is a modern, responsive food delivery website built using HTML, CSS, and JavaScript. It features a persistent shopping cart, secure checkout, and order confirmation system. The project is deployed on an Amazon EC2 instance and accessible via a custom domain with HTTPS enabled.

---

## 📁 Project Structure

```
royalflavours/
├── css/
│   └── style.css                # Website styles
├── js/
│   ├── cart.js                  # Cart management logic
│   └── checkout.js              # Checkout and order persistence
├── images/                      # Product images, branding assets
├── index.html                   # Homepage
├── menu.html                    # Product listing page
├── about.html                   # About the service
├── contact.html                 # Contact form
├── checkout.html                # Order form and customer info
└── order-confirmation.html      # Receipt and confirmation page
```

---

## 📄 HTML Pages Description

### `index.html`
- Landing page with menu categories, offers, and highlights.

index.html
https://github.com/alanbennny/royalflavours/blob/main/codes

### `menu.html`
- Displays all food items by category.
- "Add to Cart" functionality integrated.
  index.html
https://github.com/alanbennny/royalflavours/blob/main/codes

### `about.html`
- Brief overview of RoyalFlavours, mission, and services.

https://github.com/alanbennny/royalflavours/blob/main/codes
### `contact.html`
- User contact and feedback form.
https://github.com/alanbennny/royalflavours/blob/main/codes
### `checkout.html`
- Captures customer details and order summary.
- LocalStorage-enabled order persistence.

### `order-confirmation.html`
https://github.com/alanbennny/royalflavours/blob/main/codes
## 🛒 Core JavaScript: `cart.js`

Handles cart initialization, item add/remove, quantity update, and localStorage operations.

```javascript
let cart = JSON.parse(localStorage.getItem('cart')) || [];

function addToCart(name, price) {
  const existing = cart.find(item => item.name === name);
  if (existing) existing.quantity++;
  else cart.push({ name, price: parseFloat(price), quantity: 1 });
  updateCart();
}

function updateCart() {
  localStorage.setItem('cart', JSON.stringify(cart));
  const cartItems = document.getElementById('cart-items');
  const cartTotal = document.getElementById('cart-total');
  if (!cartItems || !cartTotal) return;

  cartItems.innerHTML = '';
  let total = 0;
  cart.forEach(item => {
    total += item.price * item.quantity;
    cartItems.innerHTML += `<li>${item.name} x${item.quantity} 
    <button class="remove-item" data-name="${item.name}">×</button></li>`;
  });
  cartTotal.textContent = `Total: $${total.toFixed(2)}`;

  document.querySelectorAll('.remove-item').forEach(button => {
    button.addEventListener('click', removeCartItem);
  });
}

function removeCartItem(e) {
  const itemName = e.target.dataset.name;
  cart = cart.filter(item => item.name !== itemName);
  updateCart();
}

updateCart();
```

---

## 🚀 Deployment Guide

### Step 1: Launch EC2 Instance
- Instance Type: `t2.micro`
- OS: Amazon Linux 2023 or Ubuntu 22.04 LTS
- Security Group: Allow HTTP(80), HTTPS(443), SSH(22)

### Step 2: Connect to Instance
```bash
chmod 400 royalflavours-key.pem
ssh -i "royalflavours-key.pem" ec2-user@13.250.220.174
# Use 'ubuntu' if Ubuntu OS
```

### Step 3: Install Apache & Upload Files
```bash
# Amazon Linux
sudo yum update -y && sudo yum install httpd -y
# Ubuntu
sudo apt update && sudo apt install apache2 -y

# Upload or clone files
sudo git clone https://github.com/[yourusername]/royalflavours.git /var/www/html/

# Set permissions
sudo chown -R apache:apache /var/www/html     # For Amazon Linux
sudo chown -R www-data:www-data /var/www/html # For Ubuntu
sudo chmod -R 755 /var/www/html

# Start Apache
sudo systemctl start httpd     # Amazon Linux
sudo systemctl start apache2   # Ubuntu
sudo systemctl enable httpd
sudo systemctl enable apache2
```

### Step 4: Configure Apache Document Root
```apache
DocumentRoot "/var/www/html"
<Directory "/var/www/html">
    AllowOverride All
    Require all granted
</Directory>
```

### Step 5: Configure DNS (Namecheap)
- A Record:
  - Host: `@`
  - Value: `13.250.220.174`
- Optional CNAME:
  - Host: `www`
  - Value: `royalflavours.store`

### Step 6: Install SSL (Let's Encrypt)
```bash
# Amazon Linux
sudo yum install certbot python3-certbot-apache -y
# Ubuntu
sudo apt install certbot python3-certbot-apache -y

# Run Certbot
sudo certbot --apache -d royalflavours.store
```

---

## ✅ Verification

```bash
curl -I http://localhost
# Should return HTTP/1.1 200 OK
```

---

## 🛠 Troubleshooting

| Issue | Solution |
|-------|----------|
| Connection Refused | Verify EC2 security group |
| 403 Forbidden | Check file/folder permissions |
| Cart Not Saving | Enable localStorage in browser |
| SSL Issue | `sudo certbot renew` and restart Apache |

---

## 📅 Development Timeline

| Week | Milestone |
|------|-----------|
| 1    | HTML/CSS base setup |
| 2    | JS cart functionality |
| 3    | Checkout form and localStorage |
| 4    | EC2 deployment & domain integration |

---


## 🔗 References

- [AWS EC2 Docs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/)
- [Certbot (Let's Encrypt)](https://certbot.eff.org/)
- [GitHub Docs](https://docs.github.com/)
- [Namecheap DNS Guide](https://www.namecheap.com/support/knowledgebase/article.aspx/319/2237/how-can-i-set-up-an-a-address-record-for-my-domain/)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
