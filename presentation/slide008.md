            __  ___
           /  |/  /___ _______________  _____
          / /|_/ / __ `/ ___/ ___/ __ \/ ___/
         / /  / / /_/ / /__/ /  / /_/ (__  )
        /_/  /_/\__,_/\___/_/   \____/____/

        • Create a new macro `q + <macro register>`
        • Apply macro `@ + <macro>`

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
















































































slide 008
