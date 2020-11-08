---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192496"
---
# <span data-ttu-id="30ff8-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="30ff8-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="30ff8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="30ff8-103">Crea un nuovo argomento del dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="30ff8-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="30ff8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30ff8-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30ff8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="30ff8-106">Crea un nuovo argomento del dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="30ff8-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="30ff8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30ff8-107">EXAMPLES</span></span>

### <span data-ttu-id="30ff8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30ff8-108">Example 1</span></span>

<span data-ttu-id="30ff8-109">Crea un argomento di dominio griglia eventi \` Topic1 \` in Domain \` dominio1 \` in Resource Group \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="30ff8-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="30ff8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30ff8-110">PARAMETERS</span></span>

### <span data-ttu-id="30ff8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ff8-111">-DefaultProfile</span></span>
<span data-ttu-id="30ff8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30ff8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30ff8-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="30ff8-113">-DomainName</span></span>
<span data-ttu-id="30ff8-114">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="30ff8-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="30ff8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="30ff8-115">-Name</span></span>
<span data-ttu-id="30ff8-116">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="30ff8-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="30ff8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30ff8-117">-ResourceGroupName</span></span>
<span data-ttu-id="30ff8-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30ff8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="30ff8-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30ff8-119">-Confirm</span></span>
<span data-ttu-id="30ff8-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30ff8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30ff8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30ff8-121">-WhatIf</span></span>
<span data-ttu-id="30ff8-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30ff8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30ff8-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30ff8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30ff8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ff8-124">CommonParameters</span></span>
<span data-ttu-id="30ff8-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ff8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ff8-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30ff8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ff8-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30ff8-127">INPUTS</span></span>

### <span data-ttu-id="30ff8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="30ff8-128">System.String</span></span>

## <span data-ttu-id="30ff8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30ff8-129">OUTPUTS</span></span>

### <span data-ttu-id="30ff8-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="30ff8-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="30ff8-131">Note</span><span class="sxs-lookup"><span data-stu-id="30ff8-131">NOTES</span></span>

## <span data-ttu-id="30ff8-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30ff8-132">RELATED LINKS</span></span>
