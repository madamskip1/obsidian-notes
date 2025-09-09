```
from django.contrib.auth import get_user_model
user = User.objects.get(email="admin@admin.pl")
customer = Customer.objects.get(subscriber=user)
```

```
from djstripe.models import Subscription, Customer

subscription = Subscription.objects.filter(customer=customer, status="active")
```

```
active_subscriptions = Subscription.objects.filter(
    customer__email='admin@admin.pl',
    stripe_data__status="active"
)
```