Si dependes en el uso de bifurcaciones de tus repositorios privados, puedes configurar las políticas que controlan cómo los usuarios pueden ejecutar flujos de trabajo en los eventos de `pull_request`. Ya que están disponibles únicamente para repositorios privados {% ifversion ghec or ghes or ghae %}e internos{% endif %}, puedes configurar estos ajustes de política para {% ifversion ghec %}empresas, {% elsif ghes or ghae %}tu empresa, {% endif %}organizaciones o repositorios.