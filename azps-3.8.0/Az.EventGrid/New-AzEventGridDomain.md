---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 442a88c7fe64fd8913e86ba0ee6be013f226061e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864720"
---
# <span data-ttu-id="583e4-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="583e4-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="583e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="583e4-102">SYNOPSIS</span></span>
<span data-ttu-id="583e4-103">Crea un nuovo dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="583e4-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="583e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="583e4-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="583e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="583e4-105">DESCRIPTION</span></span>
<span data-ttu-id="583e4-106">Crea un nuovo dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="583e4-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="583e4-107">Dopo aver creato il dominio, un'applicazione può pubblicare gli eventi nell'endpoint dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="583e4-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="583e4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="583e4-108">EXAMPLES</span></span>

### <span data-ttu-id="583e4-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="583e4-109">Example 1</span></span>

<span data-ttu-id="583e4-110">Crea un dominio della griglia eventi \` dominio1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="583e4-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="583e4-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="583e4-111">Example 2</span></span>

<span data-ttu-id="583e4-112">Crea un dominio della griglia eventi \` dominio1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo risorse \` MyResourceGroupName \` con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="583e4-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="583e4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="583e4-113">PARAMETERS</span></span>

### <span data-ttu-id="583e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583e4-114">-DefaultProfile</span></span>
<span data-ttu-id="583e4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="583e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="583e4-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="583e4-116">-Location</span></span>
<span data-ttu-id="583e4-117">Posizione del dominio.</span><span class="sxs-lookup"><span data-stu-id="583e4-117">The location of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583e4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="583e4-118">-Name</span></span>
<span data-ttu-id="583e4-119">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="583e4-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583e4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="583e4-120">-ResourceGroupName</span></span>
<span data-ttu-id="583e4-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="583e4-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583e4-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="583e4-122">-Tag</span></span>
<span data-ttu-id="583e4-123">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="583e4-123">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="583e4-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="583e4-124">-Confirm</span></span>
<span data-ttu-id="583e4-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="583e4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="583e4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="583e4-126">-WhatIf</span></span>
<span data-ttu-id="583e4-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="583e4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="583e4-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="583e4-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="583e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583e4-129">CommonParameters</span></span>
<span data-ttu-id="583e4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="583e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583e4-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="583e4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583e4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="583e4-132">INPUTS</span></span>

### <span data-ttu-id="583e4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="583e4-133">System.String</span></span>

### <span data-ttu-id="583e4-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="583e4-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="583e4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="583e4-135">OUTPUTS</span></span>

### <span data-ttu-id="583e4-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="583e4-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="583e4-137">Note</span><span class="sxs-lookup"><span data-stu-id="583e4-137">NOTES</span></span>

## <span data-ttu-id="583e4-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="583e4-138">RELATED LINKS</span></span>
