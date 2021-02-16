---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187494"
---
# Modulo Az.ManagedServices
## Descrizione
Questa funzionalità viene usata dai clienti di Provider di servizi gestiti (MSP). I clienti offrono a MSP la possibilità di gestire la sottoscrizione o il gruppo di risorse. Oltre a concedere l'accesso, il cliente può anche rimuovere l'accesso o visualizzare l'accesso esistente. I criteri di gestione dei dati sono in grado di visualizzare l'elenco dei clienti che hanno concesso loro l'accesso alle sottoscrizioni. Questo processo implica due oggetti: una definizione di registrazione che identifica l'MSP e le definizioni di ruolo concesse agli utenti MSP. L'MSP può facoltativamente definire questo oggetto usando un marketplace di Servizi gestiti che offre assegnazioni di Access che associano una sottoscrizione alla definizione.

## Cmdlet di Az.ManagedServices
### [Get-AzManagedServicesAssignment](Get-AzManagedServicesAssignment.md)
Ottiene una specifica attività di registrazione o un elenco delle assegnazioni di registrazione.

### [Get-AzManagedServicesDefinition](Get-AzManagedServicesDefinition.md)
Ottiene una definizione di registrazione specifica o un elenco delle definizioni di registrazione.

### [New-AzManagedServicesAssignment](New-AzManagedServicesAssignment.md)
Crea o aggiorna un'assegnazione di registrazione.

### [New-AzManagedServicesDefinition](New-AzManagedServicesDefinition.md)
Crea o aggiorna una definizione di registrazione.

### [Remove-AzManagedServicesAssignment](Remove-AzManagedServicesAssignment.md)
Rimuove un'attività di registrazione.

### [Remove-AzManagedServicesDefinition](Remove-AzManagedServicesDefinition.md)
Rimuove una definizione di registrazione.
