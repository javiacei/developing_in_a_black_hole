           _____      __          __  _
          / ___/___  / /__  _____/ /_(_)___  ____
          \__ \/ _ \/ / _ \/ ___/ __/ / __ \/ __ \
         ___/ /  __/ /  __/ /__/ /_/ / /_/ / / / /
        /____/\___/_/\___/\___/\__/_/\____/_/ /_/

        • In visual mode `v`
        • Block selection `c-v`

        # Example
        from django.db import models

        class Incident(models.Model):
            INCIDENT_ACTIONS = (
                (ASSIGN_DRIVER, 'Assign driver'),
                (UNASSIGN_DRIVER, 'Unassign driver'),
                (UPLOAD_CARGO_MANIFEST, 'Upload cargo manifest'),
                (DELETE_CARGO_MANIFEST, 'Delete cargo manifest'),
            )

            action = models.CharField(max_length=30, choices=INCIDENT_ACTIONS, default=ACTION_OTHER)
















































































slide 007
