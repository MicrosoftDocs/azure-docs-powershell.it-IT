---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473914"
---
# <span data-ttu-id="c36b6-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="c36b6-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="c36b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c36b6-102">SYNOPSIS</span></span>
<span data-ttu-id="c36b6-103">Crea un nuovo argomento del dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="c36b6-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="c36b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c36b6-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c36b6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c36b6-105">DESCRIPTION</span></span>
<span data-ttu-id="c36b6-106">Crea un nuovo argomento del dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="c36b6-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="c36b6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c36b6-107">EXAMPLES</span></span>

### <span data-ttu-id="c36b6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c36b6-108">Example 1</span></span>

<span data-ttu-id="c36b6-109">Crea un argomento di dominio griglia eventi \` Topic1 \` in Domain \` dominio1 \` in Resource Group \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c36b6-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="c36b6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c36b6-110">PARAMETERS</span></span>

### <span data-ttu-id="c36b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36b6-111">-DefaultProfile</span></span>
<span data-ttu-id="c36b6-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c36b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c36b6-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="c36b6-113">-DomainName</span></span>
<span data-ttu-id="c36b6-114">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c36b6-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36b6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c36b6-115">-Name</span></span>
<span data-ttu-id="c36b6-116">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c36b6-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="c36b6-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c36b6-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c36b6-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c36b6-119">-Confirm</span></span>
<span data-ttu-id="c36b6-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c36b6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c36b6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c36b6-121">-WhatIf</span></span>
<span data-ttu-id="c36b6-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c36b6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c36b6-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c36b6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c36b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36b6-124">CommonParameters</span></span>
<span data-ttu-id="c36b6-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36b6-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c36b6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36b6-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c36b6-127">INPUTS</span></span>

### <span data-ttu-id="c36b6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c36b6-128">System.String</span></span>

## <span data-ttu-id="c36b6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c36b6-129">OUTPUTS</span></span>

### <span data-ttu-id="c36b6-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="c36b6-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="c36b6-131">Note</span><span class="sxs-lookup"><span data-stu-id="c36b6-131">NOTES</span></span>

## <span data-ttu-id="c36b6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c36b6-132">RELATED LINKS</span></span>
