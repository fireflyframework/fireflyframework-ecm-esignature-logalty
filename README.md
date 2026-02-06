# Firefly ECM eSignature - Logalty

Logalty eSignature adapter for Firefly ECM. This module provides a placeholder implementation of a Logalty eSignature provider following the same hexagonal architecture and integration patterns used by the DocuSign and Adobe Sign adapters.

Status: Prototype (skeleton) — stubs in place ready for full API mapping.

## Features
- eIDAS-compliant signature workflows (planned)
- Envelope creation and sending (skeleton)
- Webhook support (planned)
- Resilience (CircuitBreaker + Retry)

## Getting Started

### Add dependency
```xml
<dependency>
  <groupId>org.fireflyframework</groupId>
  <artifactId>fireflyframework-ecm-esignature-logalty</artifactId>
  <version>1.0.0-SNAPSHOT</version>
</dependency>
```

### Enable provider
```yaml
firefly:
  ecm:
    features:
      esignature: true
    esignature:
      provider: logalty
```

### Configure properties
```yaml
firefly:
  ecm:
    adapter:
      logalty:
        client-id: ${LOGALTY_CLIENT_ID}
        client-secret: ${LOGALTY_CLIENT_SECRET}
        base-url: https://api-sandbox.logalty.com
        api-version: v1
        webhook-url: https://your.service/logalty/webhooks
        webhook-secret: ${LOGALTY_WEBHOOK_SECRET}
        sandbox-mode: true
```

## Notes
- SignatureProvider.LOGALTY is now available in fireflyframework-ecm-core
- Full implementation pending Logalty API documentation and credentials
- Placeholder methods ready for actual API integration
