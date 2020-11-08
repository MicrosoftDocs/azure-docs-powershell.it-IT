---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192934"
---
# <span data-ttu-id="787ae-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="787ae-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="787ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="787ae-102">SYNOPSIS</span></span>
<span data-ttu-id="787ae-103">Imposta le proprietà di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="787ae-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="787ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="787ae-104">SYNTAX</span></span>

### <span data-ttu-id="787ae-105">TopicNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="787ae-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="787ae-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="787ae-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="787ae-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="787ae-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="787ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="787ae-108">DESCRIPTION</span></span>
<span data-ttu-id="787ae-109">Imposta le proprietà di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="787ae-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="787ae-110">Questa operazione può essere usata per sostituire i tag di un argomento della griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="787ae-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="787ae-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="787ae-111">EXAMPLES</span></span>

### <span data-ttu-id="787ae-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="787ae-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="787ae-113">Imposta le proprietà dell'argomento griglia dell'evento \` Topic1 \` nel gruppo \` di risorse MyResourceGroupName \` per sostituire i tag con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="787ae-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="787ae-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="787ae-114">PARAMETERS</span></span>

### <span data-ttu-id="787ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787ae-115">-DefaultProfile</span></span>
<span data-ttu-id="787ae-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="787ae-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="787ae-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="787ae-117">-InboundIpRule</span></span>
<span data-ttu-id="787ae-118">Hashtable che rappresenta l'elenco delle regole IP in ingresso.</span><span class="sxs-lookup"><span data-stu-id="787ae-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="787ae-119">Ogni regola specifica l'indirizzo IP nella notazione CIDR, ad esempio 10.0.0.0/8, insieme all'azione corrispondente da eseguire in base alla corrispondenza o alla mancata corrispondenza di IpMask.</span><span class="sxs-lookup"><span data-stu-id="787ae-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="787ae-120">I valori di azione possibili includono Consenti solo</span><span class="sxs-lookup"><span data-stu-id="787ae-120">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="787ae-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="787ae-121">-InputObject</span></span>
<span data-ttu-id="787ae-122">Oggetto argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="787ae-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="787ae-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="787ae-123">-Name</span></span>
<span data-ttu-id="787ae-124">Nome argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="787ae-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="787ae-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="787ae-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="787ae-126">Determina se il traffico è consentito tramite rete pubblica.</span><span class="sxs-lookup"><span data-stu-id="787ae-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="787ae-127">Per impostazione predefinita è abilitato.</span><span class="sxs-lookup"><span data-stu-id="787ae-127">By default it is enabled.</span></span> <span data-ttu-id="787ae-128">Puoi limitare ulteriormente gli indirizzi IP specifici configurando i parametri di InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="787ae-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="787ae-129">I valori consentiti sono disabilitati e abilitati.</span><span class="sxs-lookup"><span data-stu-id="787ae-129">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="787ae-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="787ae-130">-ResourceGroupName</span></span>
<span data-ttu-id="787ae-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="787ae-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="787ae-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="787ae-132">-ResourceId</span></span>
<span data-ttu-id="787ae-133">EventGrid argomento ResourceID.</span><span class="sxs-lookup"><span data-stu-id="787ae-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="787ae-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="787ae-134">-Tag</span></span>
<span data-ttu-id="787ae-135">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="787ae-135">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="787ae-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="787ae-136">-Confirm</span></span>
<span data-ttu-id="787ae-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="787ae-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="787ae-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="787ae-138">-WhatIf</span></span>
<span data-ttu-id="787ae-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="787ae-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="787ae-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="787ae-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="787ae-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787ae-141">CommonParameters</span></span>
<span data-ttu-id="787ae-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787ae-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787ae-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="787ae-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787ae-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="787ae-144">INPUTS</span></span>

### <span data-ttu-id="787ae-145">System. String</span><span class="sxs-lookup"><span data-stu-id="787ae-145">System.String</span></span>

### <span data-ttu-id="787ae-146">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="787ae-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="787ae-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="787ae-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="787ae-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="787ae-148">OUTPUTS</span></span>

### <span data-ttu-id="787ae-149">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="787ae-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="787ae-150">Note</span><span class="sxs-lookup"><span data-stu-id="787ae-150">NOTES</span></span>

## <span data-ttu-id="787ae-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="787ae-151">RELATED LINKS</span></span>
