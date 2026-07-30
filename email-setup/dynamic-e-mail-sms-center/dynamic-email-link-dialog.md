# Dynamic Email - Link Dialog

### Overview

Use the **Link dialog** to add a link in your email text. You can also use it to edit an existing link.

You control three things:

* what the link text looks like,
* where the link goes, and
* how it opens when someone clicks it.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (347).png" alt="Link dialog with Link Info, Target, and Upload tabs."><figcaption><p>Link dialog tabs.</p></figcaption></figure></div>

### Link dialog tabs

#### Link Info tab

This is the main tab. You will use it for most links.

* **Display Text**: the clickable text people see. Example: `Open booking`.
* **Link Type**:
  * **URL**: a normal web address.
  * **Anchor**: a jump to a place in the same content.
  * **E-mail**: a clickable email address.
* **Protocol**: the start of the address, like `https://`.
* **URL**: the address the link should open.
* **Browse Server**: pick a file or image you already uploaded.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (346).png" alt="Link Info settings with Protocol, URL, and Browse Server fields."><figcaption><p>Link Info tab settings.</p></figcaption></figure></div>

#### Target tab

This tab defines how the link should open when clicked.

* Options may include:
  * **\<not set>** (default behavior)
  * **New Window (\_blank)** – Opens link in a new tab/window.
  * **Same Window (\_self)** – Opens link in the same window/tab.
  * **Parent Frame (\_parent)** – Opens link in the parent frame (if applicable).
* **Topmost Window (\_top)** – Opens link in the full browser window.

#### Upload tab

Use this tab to upload a file and link to it.

1. Click **Choose File** and select the file.
2. Click **Upload to Server**.
3. After upload, the link address is filled in for you.

### Using placeholders (variables) as links

Some links are not normal web addresses. They are **placeholders** that the system replaces when sending. A common example is the customer link: `[Hash-key-link]`.

{% hint style="info" %}
When you use a placeholder as a link, set **Protocol** to .

This prevents the editor from adding `https://` in front of the placeholder.
{% endhint %}

Use these settings:

* **Link Type**: `URL`
* **Protocol**: `<other>`
* **URL**: `[Hash-key-link]`
