---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 18be852a8a44f55cbc159bdbc7b4dbf3f276582a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991281"
---
# <span data-ttu-id="22b1f-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="22b1f-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="22b1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="22b1f-103">Crea un nuovo argomento Dominio griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="22b1f-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="22b1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22b1f-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22b1f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="22b1f-106">Crea un nuovo argomento Dominio griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="22b1f-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="22b1f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22b1f-107">EXAMPLES</span></span>

### <span data-ttu-id="22b1f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22b1f-108">Example 1</span></span>

<span data-ttu-id="22b1f-109">Crea un argomento Argomento dominio griglia eventi in Domain Domain1 nel gruppo \` di risorse \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="22b1f-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="22b1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22b1f-110">PARAMETERS</span></span>

### <span data-ttu-id="22b1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b1f-111">-DefaultProfile</span></span>
<span data-ttu-id="22b1f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22b1f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b1f-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="22b1f-113">-DomainName</span></span>
<span data-ttu-id="22b1f-114">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="22b1f-114">EventGrid domain name.</span></span>

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

### <span data-ttu-id="22b1f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="22b1f-115">-Name</span></span>
<span data-ttu-id="22b1f-116">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="22b1f-116">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="22b1f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b1f-117">-ResourceGroupName</span></span>
<span data-ttu-id="22b1f-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22b1f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="22b1f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22b1f-119">-Confirm</span></span>
<span data-ttu-id="22b1f-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22b1f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b1f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b1f-121">-WhatIf</span></span>
<span data-ttu-id="22b1f-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22b1f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b1f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22b1f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b1f-124">CommonParameters</span></span>
<span data-ttu-id="22b1f-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b1f-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22b1f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b1f-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="22b1f-127">INPUTS</span></span>

### <span data-ttu-id="22b1f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="22b1f-128">System.String</span></span>

## <span data-ttu-id="22b1f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22b1f-129">OUTPUTS</span></span>

### <span data-ttu-id="22b1f-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="22b1f-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="22b1f-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="22b1f-131">NOTES</span></span>

## <span data-ttu-id="22b1f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22b1f-132">RELATED LINKS</span></span>
