---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194407"
---
# <span data-ttu-id="02fce-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="02fce-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="02fce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02fce-102">SYNOPSIS</span></span>
<span data-ttu-id="02fce-103">Crea un nuovo dominio della griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="02fce-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="02fce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02fce-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02fce-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="02fce-105">DESCRIPTION</span></span>
<span data-ttu-id="02fce-106">Crea un nuovo dominio della griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="02fce-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="02fce-107">Dopo aver creato il dominio, un'applicazione può pubblicare eventi nell'endpoint dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="02fce-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="02fce-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02fce-108">EXAMPLES</span></span>

### <span data-ttu-id="02fce-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02fce-109">Example 1</span></span>

<span data-ttu-id="02fce-110">Crea un dominio Della griglia eventi Domain1 nella località geografica specificata \` \` \` westus2, nel \` gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="02fce-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="02fce-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="02fce-111">Example 2</span></span>

<span data-ttu-id="02fce-112">Crea un dominio Della griglia eventi Domain1 nella località geografica specificata westus2, nel gruppo di risorse MyResourceGroupName con i tag \` \` \` \` \` \` "Department" e "Environment" specificati.</span><span class="sxs-lookup"><span data-stu-id="02fce-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

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

## <span data-ttu-id="02fce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02fce-113">PARAMETERS</span></span>

### <span data-ttu-id="02fce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02fce-114">-DefaultProfile</span></span>
<span data-ttu-id="02fce-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02fce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02fce-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="02fce-116">-InboundIpRule</span></span>
<span data-ttu-id="02fce-117">Hashtable che rappresenta l'elenco delle regole IP in ingresso.</span><span class="sxs-lookup"><span data-stu-id="02fce-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="02fce-118">Ogni regola specifica l'indirizzo IP nella notazione CIDR, ad esempio 10.0.0.0/8 insieme all'azione corrispondente da eseguire in base alla corrispondenza o a nessuna corrispondenza di IpMask.</span><span class="sxs-lookup"><span data-stu-id="02fce-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="02fce-119">I valori di Azione possibili includono Consenti solo</span><span class="sxs-lookup"><span data-stu-id="02fce-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="02fce-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="02fce-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="02fce-121">Tabella hash che rappresenta i campi di mapping di input con il valore predefinito in formato tasto separato da spazio = valore.</span><span class="sxs-lookup"><span data-stu-id="02fce-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="02fce-122">I nomi di chiave consentiti sono subject, eventtype e dataversion.</span><span class="sxs-lookup"><span data-stu-id="02fce-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="02fce-123">Viene usato solo quando InputSchemaHelp è customeventschema.</span><span class="sxs-lookup"><span data-stu-id="02fce-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="02fce-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="02fce-124">-InputMappingField</span></span>
<span data-ttu-id="02fce-125">Tabella hash che rappresenta i campi di mapping di input in formato chiave separata da spazio = formato valore.</span><span class="sxs-lookup"><span data-stu-id="02fce-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="02fce-126">I nomi di chiave consentiti sono id, topic, eventtime, subject, eventtype e dataversion.</span><span class="sxs-lookup"><span data-stu-id="02fce-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="02fce-127">Viene usato solo quando InputSchemaHelp è customeventschema.</span><span class="sxs-lookup"><span data-stu-id="02fce-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="02fce-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="02fce-128">-InputSchema</span></span>
<span data-ttu-id="02fce-129">Schema degli eventi di input per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="02fce-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="02fce-130">I valori consentiti sono: eventgridschema, customeventschema o cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="02fce-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="02fce-131">Il valore predefinito è eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="02fce-131">Default value is eventgridschema.</span></span> <span data-ttu-id="02fce-132">Si noti che se si specifica customeventschema, è necessario specificare anche i parametri InputMappingField o/e InputMappingDefaultValue.</span><span class="sxs-lookup"><span data-stu-id="02fce-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="02fce-133">-Location</span><span class="sxs-lookup"><span data-stu-id="02fce-133">-Location</span></span>
<span data-ttu-id="02fce-134">Posizione del dominio.</span><span class="sxs-lookup"><span data-stu-id="02fce-134">The location of the domain.</span></span>

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

### <span data-ttu-id="02fce-135">-Name</span><span class="sxs-lookup"><span data-stu-id="02fce-135">-Name</span></span>
<span data-ttu-id="02fce-136">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="02fce-136">EventGrid domain name.</span></span>

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

### <span data-ttu-id="02fce-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="02fce-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="02fce-138">Questo determina se il traffico è consentito su una rete pubblica.</span><span class="sxs-lookup"><span data-stu-id="02fce-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="02fce-139">Per impostazione predefinita, è abilitata.</span><span class="sxs-lookup"><span data-stu-id="02fce-139">By default it is enabled.</span></span> <span data-ttu-id="02fce-140">È possibile limitare ulteriormente l'accesso a specifici IP configurando parametri InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="02fce-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="02fce-141">I valori consentiti sono disabilitati e abilitati.</span><span class="sxs-lookup"><span data-stu-id="02fce-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="02fce-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02fce-142">-ResourceGroupName</span></span>
<span data-ttu-id="02fce-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="02fce-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="02fce-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="02fce-144">-Tag</span></span>
<span data-ttu-id="02fce-145">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="02fce-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="02fce-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02fce-146">-Confirm</span></span>
<span data-ttu-id="02fce-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02fce-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02fce-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02fce-148">-WhatIf</span></span>
<span data-ttu-id="02fce-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02fce-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02fce-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02fce-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02fce-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02fce-151">CommonParameters</span></span>
<span data-ttu-id="02fce-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02fce-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02fce-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="02fce-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02fce-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="02fce-154">INPUTS</span></span>

### <span data-ttu-id="02fce-155">System.String</span><span class="sxs-lookup"><span data-stu-id="02fce-155">System.String</span></span>

### <span data-ttu-id="02fce-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="02fce-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="02fce-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02fce-157">OUTPUTS</span></span>

### <span data-ttu-id="02fce-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="02fce-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="02fce-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="02fce-159">NOTES</span></span>

## <span data-ttu-id="02fce-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02fce-160">RELATED LINKS</span></span>
