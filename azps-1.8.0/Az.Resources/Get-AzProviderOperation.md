---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bd0483cf03ac5cff224824cc41b3fab994006acb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677385"
---
# <span data-ttu-id="b2f3c-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b2f3c-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="b2f3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f3c-103">Ottiene le operazioni per un provider di risorse Azure che sono a protezione diretta con Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b2f3c-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="b2f3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2f3c-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2f3c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f3c-106">Il Get-AzProviderOperation ottiene le operazioni esposte dai provider di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f3c-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="b2f3c-107">Le operazioni possono essere composte per creare ruoli personalizzati in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b2f3c-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="b2f3c-108">Il comando accetta come input una stringa di ricerca dell'operazione (con i caratteri jolly () possibili) *che determina i dettagli delle operazioni da visualizzare. Usare Get-AzProviderOperation \* per ottenere tutte le operazioni per tutti i provider di risorse di Azure. USA Get-AzProviderOperation Microsoft. Compute/* per ottenere tutte le operazioni del provider di risorse Microsoft. Compute.</span><span class="sxs-lookup"><span data-stu-id="b2f3c-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="b2f3c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2f3c-109">EXAMPLES</span></span>

### <span data-ttu-id="b2f3c-110">Ottenere tutte le azioni per tutti i provider</span><span class="sxs-lookup"><span data-stu-id="b2f3c-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="b2f3c-111">Ottenere azioni per un determinato provider di risorse</span><span class="sxs-lookup"><span data-stu-id="b2f3c-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="b2f3c-112">Ottenere tutte le azioni che è possibile eseguire nelle macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="b2f3c-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="b2f3c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2f3c-113">PARAMETERS</span></span>

### <span data-ttu-id="b2f3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f3c-114">-DefaultProfile</span></span>
<span data-ttu-id="b2f3c-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b2f3c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2f3c-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="b2f3c-116">-OperationSearchString</span></span>
<span data-ttu-id="b2f3c-117">Stringa di ricerca dell'operazione (con caratteri jolly possibili (\*))</span><span class="sxs-lookup"><span data-stu-id="b2f3c-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="b2f3c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f3c-118">CommonParameters</span></span>
<span data-ttu-id="b2f3c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f3c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f3c-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f3c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f3c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2f3c-121">INPUTS</span></span>

### <span data-ttu-id="b2f3c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b2f3c-122">System.String</span></span>

## <span data-ttu-id="b2f3c-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2f3c-123">OUTPUTS</span></span>

### <span data-ttu-id="b2f3c-124">Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b2f3c-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="b2f3c-125">Note</span><span class="sxs-lookup"><span data-stu-id="b2f3c-125">NOTES</span></span>
<span data-ttu-id="b2f3c-126">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="b2f3c-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b2f3c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2f3c-127">RELATED LINKS</span></span>
