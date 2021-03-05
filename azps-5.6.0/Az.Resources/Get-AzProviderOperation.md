---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 61e38afcccccd6a96e92983d24442740351320ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016045"
---
# <span data-ttu-id="3b96a-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3b96a-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="3b96a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b96a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b96a-103">Ottiene le operazioni per un provider di risorse di Azure a protezione diretta con il controllo degli accessi in base al ruolo di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b96a-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="3b96a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b96a-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b96a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3b96a-105">DESCRIPTION</span></span>
<span data-ttu-id="3b96a-106">LGet-AzProviderOperation ottiene le operazioni esposte dai provider di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b96a-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="3b96a-107">Le operazioni possono essere composte per creare ruoli personalizzati in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3b96a-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="3b96a-108">Il comando accetta come input una stringa di ricerca dell'operazione (con possibili caratteri jolly( ) caratteri che determina i *dettagli delle operazioni da visualizzare. Usare Get-AzProviderOperation \* per ottenere tutte le operazioni per tutti i provider di risorse di Azure. Usare Get-AzProviderOperation Microsoft.Compute/* per ottenere tutte le operazioni del provider di risorse Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="3b96a-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="3b96a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b96a-109">EXAMPLES</span></span>

### <span data-ttu-id="3b96a-110">Esempio 1: Ottenere tutte le azioni per tutti i provider</span><span class="sxs-lookup"><span data-stu-id="3b96a-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="3b96a-111">Esempio 2: Ottenere le azioni per un determinato provider di risorse</span><span class="sxs-lookup"><span data-stu-id="3b96a-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="3b96a-112">Esempio 3: Ottenere tutte le azioni che possono essere eseguite nelle macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="3b96a-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="3b96a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b96a-113">PARAMETERS</span></span>

### <span data-ttu-id="3b96a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b96a-114">-DefaultProfile</span></span>
<span data-ttu-id="3b96a-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3b96a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b96a-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="3b96a-116">-OperationSearchString</span></span>
<span data-ttu-id="3b96a-117">Stringa di ricerca dell'operazione (con possibili caratteri jolly (\*)</span><span class="sxs-lookup"><span data-stu-id="3b96a-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="3b96a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b96a-118">CommonParameters</span></span>
<span data-ttu-id="3b96a-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b96a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b96a-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b96a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b96a-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="3b96a-121">INPUTS</span></span>

### <span data-ttu-id="3b96a-122">System.String</span><span class="sxs-lookup"><span data-stu-id="3b96a-122">System.String</span></span>

## <span data-ttu-id="3b96a-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b96a-123">OUTPUTS</span></span>

### <span data-ttu-id="3b96a-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3b96a-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="3b96a-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="3b96a-125">NOTES</span></span>
<span data-ttu-id="3b96a-126">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="3b96a-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3b96a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b96a-127">RELATED LINKS</span></span>
