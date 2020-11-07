---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687470"
---
# <span data-ttu-id="912c7-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="912c7-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="912c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="912c7-102">SYNOPSIS</span></span>
<span data-ttu-id="912c7-103">Ottiene le operazioni per un provider di risorse Azure che sono a protezione diretta con Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="912c7-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="912c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="912c7-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="912c7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="912c7-105">DESCRIPTION</span></span>
<span data-ttu-id="912c7-106">Il Get-AzureRmProviderOperation ottiene le operazioni esposte dai provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="912c7-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="912c7-107">Le operazioni possono essere composte per creare ruoli personalizzati in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="912c7-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="912c7-108">Il comando accetta come input una stringa di ricerca dell'operazione (con i possibili caratteri jolly (\*)) che determina i dettagli delle operazioni da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="912c7-108">The command takes as input an operation search string (with possible wildcard(\*) character(s)) which determines the operations details to display.</span></span>

<span data-ttu-id="912c7-109">Usare Get-AzureRmProviderOperation \* per ottenere tutte le operazioni per tutti i provider di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="912c7-109">Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers.</span></span>

<span data-ttu-id="912c7-110">USA Get-AzureRmProviderOperation Microsoft. COMPUTE/\* per ottenere tutte le operazioni del provider di risorse Microsoft. Compute.</span><span class="sxs-lookup"><span data-stu-id="912c7-110">Use Get-AzureRmProviderOperation Microsoft.Compute/\* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="912c7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="912c7-111">EXAMPLES</span></span>

### <span data-ttu-id="912c7-112">Ottenere tutte le azioni per tutti i provider</span><span class="sxs-lookup"><span data-stu-id="912c7-112">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="912c7-113">Ottenere azioni per un determinato provider di risorse</span><span class="sxs-lookup"><span data-stu-id="912c7-113">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="912c7-114">Ottenere tutte le azioni che è possibile eseguire nelle macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="912c7-114">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="912c7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="912c7-115">PARAMETERS</span></span>

### <span data-ttu-id="912c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912c7-116">-DefaultProfile</span></span>
<span data-ttu-id="912c7-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="912c7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912c7-118">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="912c7-118">-OperationSearchString</span></span>
<span data-ttu-id="912c7-119">Stringa di ricerca dell'operazione (con caratteri jolly possibili (\*))</span><span class="sxs-lookup"><span data-stu-id="912c7-119">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="912c7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912c7-120">CommonParameters</span></span>
<span data-ttu-id="912c7-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="912c7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912c7-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="912c7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912c7-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="912c7-123">INPUTS</span></span>

### <span data-ttu-id="912c7-124">Stringa</span><span class="sxs-lookup"><span data-stu-id="912c7-124">String</span></span>
<span data-ttu-id="912c7-125">Il parametro ' OperationSearchString ' accetta il valore di tipo ' String ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="912c7-125">Parameter 'OperationSearchString' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="912c7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="912c7-126">OUTPUTS</span></span>

### <span data-ttu-id="912c7-127">Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="912c7-127">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="912c7-128">Note</span><span class="sxs-lookup"><span data-stu-id="912c7-128">NOTES</span></span>
<span data-ttu-id="912c7-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="912c7-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="912c7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="912c7-130">RELATED LINKS</span></span>
