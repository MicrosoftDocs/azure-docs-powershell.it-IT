---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 9946c065a572333062c512c3ce5fa866c5d3ce20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674482"
---
# <span data-ttu-id="ba22a-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ba22a-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="ba22a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba22a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba22a-103">Crea un nuovo argomento del dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ba22a-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="ba22a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba22a-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba22a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba22a-105">DESCRIPTION</span></span>
<span data-ttu-id="ba22a-106">Crea un nuovo argomento del dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ba22a-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="ba22a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba22a-107">EXAMPLES</span></span>

### <span data-ttu-id="ba22a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba22a-108">Example 1</span></span>

<span data-ttu-id="ba22a-109">Crea un argomento di dominio griglia eventi \` Topic1 \` in Domain \` dominio1 \` in Resource Group \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ba22a-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="ba22a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba22a-110">PARAMETERS</span></span>

### <span data-ttu-id="ba22a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba22a-111">-DefaultProfile</span></span>
<span data-ttu-id="ba22a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba22a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba22a-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ba22a-113">-DomainName</span></span>
<span data-ttu-id="ba22a-114">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba22a-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="ba22a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba22a-115">-Name</span></span>
<span data-ttu-id="ba22a-116">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba22a-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="ba22a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba22a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba22a-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ba22a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba22a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ba22a-119">-Confirm</span></span>
<span data-ttu-id="ba22a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba22a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba22a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba22a-121">-WhatIf</span></span>
<span data-ttu-id="ba22a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba22a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba22a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba22a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba22a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba22a-124">CommonParameters</span></span>
<span data-ttu-id="ba22a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba22a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba22a-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba22a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba22a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba22a-127">INPUTS</span></span>

### <span data-ttu-id="ba22a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ba22a-128">System.String</span></span>

## <span data-ttu-id="ba22a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba22a-129">OUTPUTS</span></span>

### <span data-ttu-id="ba22a-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ba22a-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="ba22a-131">Note</span><span class="sxs-lookup"><span data-stu-id="ba22a-131">NOTES</span></span>

## <span data-ttu-id="ba22a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba22a-132">RELATED LINKS</span></span>