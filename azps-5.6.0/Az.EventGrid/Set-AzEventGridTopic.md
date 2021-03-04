---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 9fe0fad7ec353b3805bb941b62f6f6b6ee83e157
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986074"
---
# <span data-ttu-id="e54e6-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="e54e6-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="e54e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e54e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e54e6-103">Imposta le proprietà di un argomento Griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="e54e6-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="e54e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e54e6-104">SYNTAX</span></span>

### <span data-ttu-id="e54e6-105">TopicNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e54e6-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e54e6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e54e6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e54e6-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e54e6-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e54e6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e54e6-108">DESCRIPTION</span></span>
<span data-ttu-id="e54e6-109">Imposta le proprietà di un argomento Griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="e54e6-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="e54e6-110">Questa opzione può essere usata per sostituire i tag di un argomento griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="e54e6-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="e54e6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e54e6-111">EXAMPLES</span></span>

### <span data-ttu-id="e54e6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e54e6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="e54e6-113">Imposta le proprietà dell'argomento Griglia eventi Argomento1 nel gruppo di risorse MyResourceGroupName per sostituire i tag con i tag \` \` specificati \` \` "Department" e "Environment".</span><span class="sxs-lookup"><span data-stu-id="e54e6-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="e54e6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e54e6-114">PARAMETERS</span></span>

### <span data-ttu-id="e54e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54e6-115">-DefaultProfile</span></span>
<span data-ttu-id="e54e6-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e54e6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e54e6-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="e54e6-117">-InboundIpRule</span></span>
<span data-ttu-id="e54e6-118">Hashtable che rappresenta l'elenco delle regole IP in ingresso.</span><span class="sxs-lookup"><span data-stu-id="e54e6-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="e54e6-119">Ogni regola specifica l'indirizzo IP nella notazione CIDR, ad esempio 10.0.0.0/8 insieme all'azione corrispondente da eseguire in base alla corrispondenza o a nessuna corrispondenza di IpMask.</span><span class="sxs-lookup"><span data-stu-id="e54e6-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="e54e6-120">I valori di Azione possibili includono Consenti solo</span><span class="sxs-lookup"><span data-stu-id="e54e6-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e54e6-121">-InputObject</span></span>
<span data-ttu-id="e54e6-122">Oggetto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="e54e6-122">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e54e6-123">-Name</span></span>
<span data-ttu-id="e54e6-124">Nome dell'argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e54e6-124">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e54e6-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="e54e6-126">Questo determina se il traffico è consentito su una rete pubblica.</span><span class="sxs-lookup"><span data-stu-id="e54e6-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="e54e6-127">Per impostazione predefinita, è abilitata.</span><span class="sxs-lookup"><span data-stu-id="e54e6-127">By default it is enabled.</span></span> <span data-ttu-id="e54e6-128">È possibile limitare ulteriormente l'accesso a specifici IP configurando parametri InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="e54e6-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="e54e6-129">I valori consentiti sono disabilitati e abilitati.</span><span class="sxs-lookup"><span data-stu-id="e54e6-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54e6-130">-ResourceGroupName</span></span>
<span data-ttu-id="e54e6-131">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e54e6-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e54e6-132">-ResourceId</span></span>
<span data-ttu-id="e54e6-133">ResourceID dell'argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="e54e6-133">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="e54e6-134">-Tag</span></span>
<span data-ttu-id="e54e6-135">Hashtables che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e54e6-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e54e6-136">-Confirm</span></span>
<span data-ttu-id="e54e6-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e54e6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e54e6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e54e6-138">-WhatIf</span></span>
<span data-ttu-id="e54e6-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e54e6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e54e6-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e54e6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e54e6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54e6-141">CommonParameters</span></span>
<span data-ttu-id="e54e6-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e54e6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54e6-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e54e6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54e6-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="e54e6-144">INPUTS</span></span>

### <span data-ttu-id="e54e6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="e54e6-145">System.String</span></span>

### <span data-ttu-id="e54e6-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="e54e6-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="e54e6-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e54e6-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e54e6-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e54e6-148">OUTPUTS</span></span>

### <span data-ttu-id="e54e6-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="e54e6-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="e54e6-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="e54e6-150">NOTES</span></span>

## <span data-ttu-id="e54e6-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e54e6-151">RELATED LINKS</span></span>
