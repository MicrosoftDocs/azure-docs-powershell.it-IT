---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192950"
---
# <span data-ttu-id="ae9f0-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="ae9f0-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="ae9f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae9f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9f0-103">Crea un nuovo argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="ae9f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae9f0-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae9f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae9f0-105">DESCRIPTION</span></span>
<span data-ttu-id="ae9f0-106">Crea un nuovo argomento della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="ae9f0-107">Dopo aver creato l'argomento, un'applicazione può pubblicare gli eventi nell'endpoint dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="ae9f0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae9f0-108">EXAMPLES</span></span>

### <span data-ttu-id="ae9f0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae9f0-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="ae9f0-110">Crea un argomento della griglia dell'evento \` Topic1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ae9f0-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ae9f0-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ae9f0-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="ae9f0-112">Crea un argomento della griglia dell'evento \` Topic1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo di risorse \` MyResourceGroupName \` con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="ae9f0-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="ae9f0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae9f0-113">PARAMETERS</span></span>

### <span data-ttu-id="ae9f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9f0-114">-DefaultProfile</span></span>
<span data-ttu-id="ae9f0-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ae9f0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae9f0-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="ae9f0-116">-InboundIpRule</span></span>
<span data-ttu-id="ae9f0-117">Hashtable che rappresenta l'elenco delle regole IP in ingresso.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="ae9f0-118">Ogni regola specifica l'indirizzo IP nella notazione CIDR, ad esempio 10.0.0.0/8, insieme all'azione corrispondente da eseguire in base alla corrispondenza o alla mancata corrispondenza di IpMask.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="ae9f0-119">I valori di azione possibili includono Consenti solo</span><span class="sxs-lookup"><span data-stu-id="ae9f0-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="ae9f0-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="ae9f0-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="ae9f0-121">Hashtable che rappresenta i campi di mapping di input con il valore predefinito in space separated Key = Value format.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="ae9f0-122">I nomi di chiave consentiti sono: subject, eventType e dataversion.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="ae9f0-123">Viene usato quando InputSchemaHelp è solo customeventschema.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="ae9f0-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="ae9f0-124">-InputMappingField</span></span>
<span data-ttu-id="ae9f0-125">Hashtable che rappresenta i campi di mapping di input nel formato chiave separato da spazio = valore.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="ae9f0-126">I nomi di chiave consentiti sono: ID, Topic, EventTime, Subject, eventType e dataversion.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="ae9f0-127">Viene usato quando InputSchemaHelp è solo customeventschema.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="ae9f0-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="ae9f0-128">-InputSchema</span></span>
<span data-ttu-id="ae9f0-129">Schema degli eventi di input per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="ae9f0-130">I valori consentiti sono: eventgridschema, customeventschema o cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="ae9f0-131">Il valore predefinito è eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-131">Default value is eventgridschema.</span></span> <span data-ttu-id="ae9f0-132">Tieni presente che se customeventschema è specificato, anche i parametri InputMappingField o/e InputMappingDefaultValue devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9f0-133">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ae9f0-133">-Location</span></span>
<span data-ttu-id="ae9f0-134">Posizione dell'argomento</span><span class="sxs-lookup"><span data-stu-id="ae9f0-134">The location of the topic</span></span>

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

### <span data-ttu-id="ae9f0-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae9f0-135">-Name</span></span>
<span data-ttu-id="ae9f0-136">Nome dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-136">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9f0-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ae9f0-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="ae9f0-138">Determina se il traffico è consentito tramite rete pubblica.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="ae9f0-139">Per impostazione predefinita è abilitato.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-139">By default it is enabled.</span></span> <span data-ttu-id="ae9f0-140">Puoi limitare ulteriormente gli indirizzi IP specifici configurando i parametri di InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="ae9f0-141">I valori consentiti sono disabilitati e abilitati.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae9f0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae9f0-142">-ResourceGroupName</span></span>
<span data-ttu-id="ae9f0-143">Gruppo di risorse in cui deve essere creato l'argomento.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-143">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="ae9f0-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae9f0-144">-Tag</span></span>
<span data-ttu-id="ae9f0-145">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-145">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="ae9f0-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae9f0-146">-Confirm</span></span>
<span data-ttu-id="ae9f0-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae9f0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae9f0-148">-WhatIf</span></span>
<span data-ttu-id="ae9f0-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae9f0-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae9f0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9f0-151">CommonParameters</span></span>
<span data-ttu-id="ae9f0-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9f0-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae9f0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9f0-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae9f0-154">INPUTS</span></span>

### <span data-ttu-id="ae9f0-155">System. String</span><span class="sxs-lookup"><span data-stu-id="ae9f0-155">System.String</span></span>

### <span data-ttu-id="ae9f0-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae9f0-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ae9f0-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae9f0-157">OUTPUTS</span></span>

### <span data-ttu-id="ae9f0-158">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ae9f0-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="ae9f0-159">Note</span><span class="sxs-lookup"><span data-stu-id="ae9f0-159">NOTES</span></span>

## <span data-ttu-id="ae9f0-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae9f0-160">RELATED LINKS</span></span>
