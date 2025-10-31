# Dynamic Email - Link Dialog

#### **Overview**

The **Link dialog** is used to insert or edit hyperlinks within text content. It allows you to define how a link appears, where it points, and how it should behave when clicked. The dialog is divided into three tabs: **Link Info**, **Target**, and **Upload**.

#### **Tabs & Their Functionality**

<figure><img src="../../.gitbook/assets/image (347).png" alt=""><figcaption></figcaption></figure>

**1. Link Info (default tab)**

This tab controls the basic properties of the hyperlink.

* **Display Text**
  * The visible text in the editor that will be clickable.
  * Example: _Testlink_.
* **Link Type**
  * Defines the kind of link being created.
  * Options include:
    * **URL** (standard web address)
    * **Anchor** (linking to a location within the same page/document)
    * **E-mail** (creates a clickable email address link).
* **Protocol**
  * Defines the link’s protocol (e.g., `http://`, `https://`, `ftp://`).
  * When inserting **variables** as hyperlinks, select **\<other>**.
    * This ensures the system interprets the variable correctly instead of treating it as a standard web URL.
    * Example: If inserting a confirmation variable like `(`\[Hash-key-link]`)`, the correct setup is:
      * **Protocol:** `<other>`
      * **URL:** \[Hash-key-link]
* **URL**
  * The actual destination of the hyperlink.
  * Can be a standard web link (e.g., `https://example.com`) or a system variable (e.g., `(`\[Hash-key-link]`)`).
* **Browse Server**
  * Opens the file browser to link to files or media already uploaded to the system.

<figure><img src="../../.gitbook/assets/image (346).png" alt=""><figcaption></figcaption></figure>

**2. Target**

This tab defines how the link should open when clicked.

* Options may include:
  * **\<not set>** (default behavior)
  * **New Window (\_blank)** – Opens link in a new tab/window.
  * **Same Window (\_self)** – Opens link in the same window/tab.
  * **Parent Frame (\_parent)** – Opens link in the parent frame (if applicable).
  * **Topmost Window (\_top)** – Opens link in the full browser window.

**3. Upload**

This tab allows direct file upload to the server and creates a link to the uploaded file.

* **Choose File** → Select a file from your computer.
* **Upload to Server** → Sends the file to the server.
* Once uploaded, the system automatically fills in the file’s URL, making it linkable.

#### **Variables in Hyperlinks**

In some cases, you may need to insert system variables (placeholders) as hyperlinks.

* Example: `(confirmation link)` or `(unsubscribe link)`.
* **Important:** Always set **Protocol** to **\<other>** when using variables.
  * This prevents the editor from trying to force a standard `http://` or `https://` prefix, which would break the variable.
* Correct setup for a variable hyperlink:
  * **Display Text:** Confirmation Link
  * **Link Type:** URL
  * **Protocol:** \<other>
  * **URL:** (\[Hash-key-link])
