Cuando habilitas las {% data variables.product.prodname_actions %}, los flujos de trabajo pueden ejecutar acciones {% ifversion actions-workflow-policy %}y los flujos de trabajo reutilizables{% endif %} ubicados en tu repositorio y en cualquier otro repositorio{% ifversion fpt %} público{% elsif ghec or ghes %} público o interno{% elsif ghae %}interno{% endif %}.