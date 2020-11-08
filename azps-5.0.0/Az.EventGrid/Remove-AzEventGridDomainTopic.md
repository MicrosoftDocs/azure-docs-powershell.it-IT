---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193424"
---
# <span data-ttu-id="fa529-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="fa529-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="fa529-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa529-102">SYNOPSIS</span></span>
<span data-ttu-id="fa529-103">Rimuove un argomento del dominio della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="fa529-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="fa529-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa529-104">SYNTAX</span></span>

### <span data-ttu-id="fa529-105">DomainTopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa529-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa529-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa529-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa529-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa529-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa529-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa529-108">DESCRIPTION</span></span>
<span data-ttu-id="fa529-109">Rimuove un argomento del dominio della griglia dell'evento Azure.</span><span class="sxs-lookup"><span data-stu-id="fa529-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="fa529-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa529-110">EXAMPLES</span></span>

### <span data-ttu-id="fa529-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fa529-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="fa529-112">Rimuove l'argomento relativo al dominio della griglia dell'evento \` Topic1 in \` Domain \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="fa529-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fa529-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fa529-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="fa529-114">Rimuove l'argomento relativo al dominio della griglia dell'evento \` Topic1 in \` Domain \` dominio1 \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="fa529-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="fa529-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa529-115">PARAMETERS</span></span>

### <span data-ttu-id="fa529-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa529-116">-DefaultProfile</span></span>
<span data-ttu-id="fa529-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa529-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa529-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="fa529-118">-DomainName</span></span>
<span data-ttu-id="fa529-119">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="fa529-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa529-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa529-120">-InputObject</span></span>
<span data-ttu-id="fa529-121">Oggetto argomento del dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="fa529-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa529-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa529-122">-Name</span></span>
<span data-ttu-id="fa529-123">Nome dell'argomento di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="fa529-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa529-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa529-124">-PassThru</span></span>
<span data-ttu-id="fa529-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fa529-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa529-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa529-126">-ResourceGroupName</span></span>
<span data-ttu-id="fa529-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fa529-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa529-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa529-128">-ResourceId</span></span>
<span data-ttu-id="fa529-129">Identificatore delle risorse che rappresenta l'argomento Domain Grid dell'evento.</span><span class="sxs-lookup"><span data-stu-id="fa529-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa529-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fa529-130">-Confirm</span></span>
<span data-ttu-id="fa529-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa529-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa529-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa529-132">-WhatIf</span></span>
<span data-ttu-id="fa529-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa529-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa529-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa529-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa529-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa529-135">CommonParameters</span></span>
<span data-ttu-id="fa529-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa529-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa529-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa529-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa529-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa529-138">INPUTS</span></span>

### <span data-ttu-id="fa529-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fa529-139">System.String</span></span>

### <span data-ttu-id="fa529-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="fa529-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="fa529-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa529-141">OUTPUTS</span></span>

### <span data-ttu-id="fa529-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa529-142">System.Boolean</span></span>

## <span data-ttu-id="fa529-143">Note</span><span class="sxs-lookup"><span data-stu-id="fa529-143">NOTES</span></span>

## <span data-ttu-id="fa529-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa529-144">RELATED LINKS</span></span>