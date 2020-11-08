---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 1ee29a4183dd78e9ced6d48e5f52c724e1b9a985
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020575"
---
# <span data-ttu-id="9a022-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="9a022-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="9a022-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a022-102">SYNOPSIS</span></span>
<span data-ttu-id="9a022-103">Ottiene le operazioni per un provider di risorse Azure che sono a protezione diretta con Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="9a022-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="9a022-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a022-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a022-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a022-105">DESCRIPTION</span></span>
<span data-ttu-id="9a022-106">Il Get-AzProviderOperation ottiene le operazioni esposte dai provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="9a022-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="9a022-107">Le operazioni possono essere composte per creare ruoli personalizzati in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="9a022-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="9a022-108">Il comando accetta come input una stringa di ricerca dell'operazione (con i caratteri jolly () possibili) *che determina i dettagli delle operazioni da visualizzare. Usare Get-AzProviderOperation \* per ottenere tutte le operazioni per tutti i provider di risorse di Azure. USA Get-AzProviderOperation Microsoft. Compute/* per ottenere tutte le operazioni del provider di risorse Microsoft. Compute.</span><span class="sxs-lookup"><span data-stu-id="9a022-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="9a022-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a022-109">EXAMPLES</span></span>

### <span data-ttu-id="9a022-110">Ottenere tutte le azioni per tutti i provider</span><span class="sxs-lookup"><span data-stu-id="9a022-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="9a022-111">Ottenere azioni per un determinato provider di risorse</span><span class="sxs-lookup"><span data-stu-id="9a022-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="9a022-112">Ottenere tutte le azioni che è possibile eseguire nelle macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="9a022-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="9a022-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a022-113">PARAMETERS</span></span>

### <span data-ttu-id="9a022-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a022-114">-DefaultProfile</span></span>
<span data-ttu-id="9a022-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9a022-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a022-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="9a022-116">-OperationSearchString</span></span>
<span data-ttu-id="9a022-117">Stringa di ricerca dell'operazione (con caratteri jolly possibili (\*))</span><span class="sxs-lookup"><span data-stu-id="9a022-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="9a022-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a022-118">CommonParameters</span></span>
<span data-ttu-id="9a022-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a022-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a022-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a022-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a022-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a022-121">INPUTS</span></span>

### <span data-ttu-id="9a022-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9a022-122">System.String</span></span>

## <span data-ttu-id="9a022-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a022-123">OUTPUTS</span></span>

### <span data-ttu-id="9a022-124">Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="9a022-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="9a022-125">Note</span><span class="sxs-lookup"><span data-stu-id="9a022-125">NOTES</span></span>
<span data-ttu-id="9a022-126">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="9a022-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9a022-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a022-127">RELATED LINKS</span></span>
