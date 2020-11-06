---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: ff56fc9df0d2303938700d85323a98575d1fb0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513516"
---
# <span data-ttu-id="be292-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="be292-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="be292-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be292-102">SYNOPSIS</span></span>
<span data-ttu-id="be292-103">Ottiene le operazioni per un provider di risorse Azure che sono a protezione diretta con Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="be292-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be292-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be292-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be292-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be292-105">DESCRIPTION</span></span>
<span data-ttu-id="be292-106">Il Get-AzureRmProviderOperation ottiene le operazioni esposte dai provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="be292-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="be292-107">Le operazioni possono essere composte per creare ruoli personalizzati in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="be292-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="be292-108">Il comando accetta come input una stringa di ricerca dell'operazione (con i caratteri jolly () possibili) *che determina i dettagli delle operazioni da visualizzare. Usare Get-AzureRmProviderOperation \* per ottenere tutte le operazioni per tutti i provider di risorse di Azure. USA Get-AzureRmProviderOperation Microsoft. Compute/* per ottenere tutte le operazioni del provider di risorse Microsoft. Compute.</span><span class="sxs-lookup"><span data-stu-id="be292-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="be292-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be292-109">EXAMPLES</span></span>

### <span data-ttu-id="be292-110">Ottenere tutte le azioni per tutti i provider</span><span class="sxs-lookup"><span data-stu-id="be292-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="be292-111">Ottenere azioni per un determinato provider di risorse</span><span class="sxs-lookup"><span data-stu-id="be292-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="be292-112">Ottenere tutte le azioni che è possibile eseguire nelle macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="be292-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="be292-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be292-113">PARAMETERS</span></span>

### <span data-ttu-id="be292-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be292-114">-DefaultProfile</span></span>
<span data-ttu-id="be292-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="be292-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be292-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="be292-116">-OperationSearchString</span></span>
<span data-ttu-id="be292-117">Stringa di ricerca dell'operazione (con caratteri jolly possibili (\*))</span><span class="sxs-lookup"><span data-stu-id="be292-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be292-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be292-118">CommonParameters</span></span>
<span data-ttu-id="be292-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be292-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be292-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be292-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be292-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be292-121">INPUTS</span></span>

### <span data-ttu-id="be292-122">System. String</span><span class="sxs-lookup"><span data-stu-id="be292-122">System.String</span></span>
<span data-ttu-id="be292-123">Parametri: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be292-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="be292-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be292-124">OUTPUTS</span></span>

### <span data-ttu-id="be292-125">Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="be292-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="be292-126">Note</span><span class="sxs-lookup"><span data-stu-id="be292-126">NOTES</span></span>
<span data-ttu-id="be292-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="be292-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="be292-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be292-128">RELATED LINKS</span></span>
