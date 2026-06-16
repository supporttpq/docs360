# Payments Integration

Tourpaq supports integration with multiple external payment service providers to enable secure online payments, automated reconciliation, and flexible checkout flows across booking processes.

The payment integrations are designed to work as a middleware layer between Tourpaq and the payment gateway, ensuring consistent handling of authorization, capture, refunds, and transaction status updates regardless of provider.

***

### Supported Payment Providers

| Provider    | Purpose in Tourpaq                                                                                        |
| ----------- | --------------------------------------------------------------------------------------------------------- |
| Nets (DIBS) | Card payments processing, 3D Secure authentication, payment authorization and capture for online bookings |
| Reepay      | Subscription and recurring payments, invoice-based flows, card tokenization and automated charging        |
| Altapay     | Multi-acquirer card processing, advanced fraud screening, flexible payment routing and settlement options |
| ePay        | Online card payments, payment window integration, refunds and transaction status synchronization          |

***

### Common Capabilities Across Providers

All supported payment integrations in Tourpaq typically expose a shared set of capabilities, depending on provider support:

* Payment authorization and capture
* Full and partial refunds
* Transaction status synchronization
* Secure card handling via tokenization (where supported)
* 3D Secure / SCA compliance support
* Payment callbacks (webhooks) for real-time updates
* Multi-currency support (provider dependent)

***

### Integration Model in Tourpaq

Tourpaq implements a provider-agnostic payment layer. This means:

* The booking system communicates with a unified payment interface
* Each provider is mapped to a standardized transaction model
* Payment states are normalized (e.g., pending, authorized, paid, failed, refunded)
* Webhook handlers ensure external updates are reflected in Tourpaq in real time

***

### Typical Payment Flow

1. Booking is created in Tourpaq
2. Payment request is generated based on booking rules
3. User is redirected or embedded into provider checkout
4. Provider processes authorization (including 3D Secure if required)
5. Tourpaq receives callback with transaction status
6. Booking is updated accordingly (confirmed or pending payment rules applied)
7. Refunds or adjustments can be triggered from back-office if needed
