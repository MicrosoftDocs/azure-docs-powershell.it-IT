---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473918"
---
# <span data-ttu-id="525d9-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="525d9-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="525d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="525d9-102">SYNOPSIS</span></span>
<span data-ttu-id="525d9-103">Crea un nuovo dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="525d9-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="525d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="525d9-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="525d9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="525d9-105">DESCRIPTION</span></span>
<span data-ttu-id="525d9-106">Crea un nuovo dominio della griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="525d9-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="525d9-107">Dopo aver creato il dominio, un'applicazione può pubblicare gli eventi nell'endpoint dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="525d9-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="525d9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="525d9-108">EXAMPLES</span></span>

### <span data-ttu-id="525d9-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="525d9-109">Example 1</span></span>

<span data-ttu-id="525d9-110">Crea un dominio della griglia eventi \` dominio1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="525d9-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="525d9-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="525d9-111">Example 2</span></span>

<span data-ttu-id="525d9-112">Crea un dominio della griglia eventi \` dominio1 \` nella posizione geografica specificata \` westus2 \` , nel gruppo risorse \` MyResourceGroupName \` con i tag specificati "reparto" e "ambiente".</span><span class="sxs-lookup"><span data-stu-id="525d9-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

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

## <span data-ttu-id="525d9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="525d9-113">PARAMETERS</span></span>

### <span data-ttu-id="525d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="525d9-114">-DefaultProfile</span></span>
<span data-ttu-id="525d9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="525d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="525d9-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="525d9-116">-InboundIpRule</span></span>
<span data-ttu-id="525d9-117">Hashtable che rappresenta l'elenco delle regole IP in ingresso.</span><span class="sxs-lookup"><span data-stu-id="525d9-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="525d9-118">Ogni regola specifica l'indirizzo IP nella notazione CIDR, ad esempio 10.0.0.0/8, insieme all'azione corrispondente da eseguire in base alla corrispondenza o alla mancata corrispondenza di IpMask.</span><span class="sxs-lookup"><span data-stu-id="525d9-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="525d9-119">I valori di azione possibili includono Consenti solo</span><span class="sxs-lookup"><span data-stu-id="525d9-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="525d9-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="525d9-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="525d9-121">Hashtable che rappresenta i campi di mapping di input con il valore predefinito in space separated Key = Value format.</span><span class="sxs-lookup"><span data-stu-id="525d9-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="525d9-122">I nomi di chiave consentiti sono: subject, eventType e dataversion.</span><span class="sxs-lookup"><span data-stu-id="525d9-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="525d9-123">Viene usato quando InputSchemaHelp è solo customeventschema.</span><span class="sxs-lookup"><span data-stu-id="525d9-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="525d9-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="525d9-124">-InputMappingField</span></span>
<span data-ttu-id="525d9-125">Hashtable che rappresenta i campi di mapping di input nel formato chiave separato da spazio = valore.</span><span class="sxs-lookup"><span data-stu-id="525d9-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="525d9-126">I nomi di chiave consentiti sono: ID, Topic, EventTime, Subject, eventType e dataversion.</span><span class="sxs-lookup"><span data-stu-id="525d9-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="525d9-127">Viene usato quando InputSchemaHelp è solo customeventschema.</span><span class="sxs-lookup"><span data-stu-id="525d9-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="525d9-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="525d9-128">-InputSchema</span></span>
<span data-ttu-id="525d9-129">Schema degli eventi di input per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="525d9-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="525d9-130">I valori consentiti sono: eventgridschema, customeventschema o cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="525d9-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="525d9-131">Il valore predefinito è eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="525d9-131">Default value is eventgridschema.</span></span> <span data-ttu-id="525d9-132">Tieni presente che se customeventschema è specificato, anche i parametri InputMappingField o/e InputMappingDefaultValue devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="525d9-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="525d9-133">-Posizione</span><span class="sxs-lookup"><span data-stu-id="525d9-133">-Location</span></span>
<span data-ttu-id="525d9-134">Posizione del dominio.</span><span class="sxs-lookup"><span data-stu-id="525d9-134">The location of the domain.</span></span>

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

### <span data-ttu-id="525d9-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="525d9-135">-Name</span></span>
<span data-ttu-id="525d9-136">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="525d9-136">EventGrid domain name.</span></span>

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

### <span data-ttu-id="525d9-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="525d9-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="525d9-138">Determina se il traffico è consentito tramite rete pubblica.</span><span class="sxs-lookup"><span data-stu-id="525d9-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="525d9-139">Per impostazione predefinita è abilitato.</span><span class="sxs-lookup"><span data-stu-id="525d9-139">By default it is enabled.</span></span> <span data-ttu-id="525d9-140">Puoi limitare ulteriormente gli indirizzi IP specifici configurando i parametri di InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="525d9-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="525d9-141">I valori consentiti sono disabilitati e abilitati.</span><span class="sxs-lookup"><span data-stu-id="525d9-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="525d9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="525d9-142">-ResourceGroupName</span></span>
<span data-ttu-id="525d9-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="525d9-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="525d9-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="525d9-144">-Tag</span></span>
<span data-ttu-id="525d9-145">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="525d9-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="525d9-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="525d9-146">-Confirm</span></span>
<span data-ttu-id="525d9-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="525d9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="525d9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="525d9-148">-WhatIf</span></span>
<span data-ttu-id="525d9-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="525d9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="525d9-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="525d9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="525d9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525d9-151">CommonParameters</span></span>
<span data-ttu-id="525d9-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="525d9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="525d9-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="525d9-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525d9-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="525d9-154">INPUTS</span></span>

### <span data-ttu-id="525d9-155">System. String</span><span class="sxs-lookup"><span data-stu-id="525d9-155">System.String</span></span>

### <span data-ttu-id="525d9-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="525d9-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="525d9-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="525d9-157">OUTPUTS</span></span>

### <span data-ttu-id="525d9-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomin</span><span class="sxs-lookup"><span data-stu-id="525d9-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="525d9-159">Note</span><span class="sxs-lookup"><span data-stu-id="525d9-159">NOTES</span></span>

## <span data-ttu-id="525d9-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="525d9-160">RELATED LINKS</span></span>
