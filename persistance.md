# Client & Server Persistence
A Reference Document for various forms of Persistance

---

## LocalStorage
### Where this persistence lives:
Located on the user's hard drive, specifically behind the browser application.

### When the data would be deleted:
When removeItem(), clear(), or similar remove the data. If the user's hard drive is destroyed, this data is also lost. For the most part, it shouldn't be necessary to delete this data manually.

### Use Cases
Local Storage is a very simple sort of API. It is written all in JavaScript. It has been popularized in HTML5. It is easy to use and quite basic. It can be used for…
- Storing user settings, like whether dark mode is activated or not
- Storing info to be referenced by the application at an indefinitely later date

### Cons:
The fact that local storage is basic also leads to its downfall in places:
Totally not secure
- Synchronous
- ~5MB data cap
- Can only store strings

### Sources:
- https://dev.to/rdegges/please-stop-using-local-storage-1i04
- https://blog.logrocket.com/the-complete-guide-to-using-localstorage-in-javascript-apps-ba44edb53a36

---

## Persistent Cookies
### Where this persistence lives:
Located on the user's hard drive, specifically behind the browser application. However, cookies are created by the server itself.

### When the data would be deleted:
A persistent cookie is sometimes signed with an expiration date. When the date passes, the cookie is wiped from the user's hard drive unless it is updated. If the user's hard drive is destroyed, this data is also lost. For the most part, it shouldn't be necessary to delete this data manually.

### Use Cases:
Unlike Local Storage, Cookies can and will be accessed by the server. This means that using Cookies gives you more utility, where using Local Storage can save you valuable bandwidth.
- Storing user settings, like whether dark mode is activated or not.
- Storing data that will persist across computers when a user is logged in
- Storing low-security login information

### Cons:
Cookies are often used to communicate with the server. Despite their versatility, they can slow down web connections if there are too many.
- Indefinite file size…but browsers often limit it to a 4kb data cap
- Use network resources, a valuable asset

### Sources:
1. RFC 6265 https://tools.ietf.org/html/rfc6265#section-6.1
2. https://www.w3schools.com/js/js_cookies.asp
3. https://www.cisco.com/c/en/us/support/docs/security/web-security-appliance/117925-technote-csc-00.html

---

## Session Cookies
### Where this persistence lives:
Located on the user's Random Access Memory (RAM), specifically behind the current browser application processes. However, the cookies themselves are originally created from the server itself.

### When the data would be deleted:
Because the data is stored in RAM, the data is deleted as soon as the browser session is closed. This data can also be deleted from instructions in the code.

### Use Cases:
- Shopping Carts
- Online Game Sessions

### Cons:
Many of these pros and cons are double-edged swords when it comes to persistance and browser data storage. You might need to communicate with the server, and you might want the data to only last a session. On the other hand, there are many situation where you emphatically wouldn't want these things.
- Communicates with the server — uses network resources
- Data deletes when session is completed

### Sources:
1. https://www.sohamkamani.com/blog/2017/01/08/web-security-session-cookies/

---

## Sessions
### Where this persistence lives:


### When the data would be deleted:


### Use Cases:


### Cons:


### Sources:
1. http://www.lassosoft.com/Tutorial-Understanding-Cookies-and-Sessions
2. 

---

## Databases
### Where this persistence lives:


### When the data would be deleted:


### Use Cases:


### Cons:


### Sources:


---

## Client-Side Cache
### Where this persistence lives:

### When the data would be deleted:

### Use Cases:

### Cons:

### Sources:


---

## Serve-Side Cache
### Where this persistence lives:

### When the data would be deleted:

### Use Cases:

### Cons:

### Sources:


---

## Remote Cache
### Where this persistence lives:

### When the data would be deleted:

### Use Cases:

### Cons:

### Sources:


---

## Remote Services
### Where this persistence lives:

### When the data would be deleted:

### Use Cases:

### Cons:

### Sources: