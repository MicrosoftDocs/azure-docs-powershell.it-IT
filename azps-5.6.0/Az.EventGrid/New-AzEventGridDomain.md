---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 9d24a8f3355c885a610cf371f4fadb716c6b159e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991295"
---
# <span data-ttu-id="37666-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="37666-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="37666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37666-102">SYNOPSIS</span></span>
<span data-ttu-id="37666-103">Crea un nuovo dominio della griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="37666-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="37666-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37666-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37666-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="37666-105">DESCRIPTION</span></span>
<span data-ttu-id="37666-106">Crea un nuovo dominio della griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="37666-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="37666-107">Dopo aver creato il dominio, un'applicazione può pubblicare eventi nell'endpoint dell'argomento.</span><span class="sxs-lookup"><span data-stu-id="37666-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="37666-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37666-108">EXAMPLES</span></span>

### <span data-ttu-id="37666-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37666-109">Example 1</span></span>

<span data-ttu-id="37666-110">Crea un dominio Della griglia eventi Domain1 nella località \` \` geografica specificata \` westus2, \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="37666-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="37666-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="37666-111">Example 2</span></span>

<span data-ttu-id="37666-112">Crea un dominio Della griglia eventi Domain1 nella località geografica specificata westus2, nel gruppo di risorse MyResourceGroupName con i tag \` \` \` \` \` \` "Department" e "Environment" specificati.</span><span class="sxs-lookup"><span data-stu-id="37666-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

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

## <span data-ttu-id="37666-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37666-113">PARAMETERS</span></span>

### <span data-ttu-id="37666-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37666-114">-DefaultProfile</span></span>
<span data-ttu-id="37666-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37666-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37666-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="37666-116">-InboundIpRule</span></span>
<span data-ttu-id="37666-117">Hashtable che rappresenta l'elenco delle regole IP in ingresso.</span><span class="sxs-lookup"><span data-stu-id="37666-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="37666-118">Ogni regola specifica l'indirizzo IP nella notazione CIDR, ad esempio 10.0.0.0/8 insieme all'azione corrispondente da eseguire in base alla corrispondenza o a nessuna corrispondenza di IpMask.</span><span class="sxs-lookup"><span data-stu-id="37666-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="37666-119">I valori di Azione possibili includono Consenti solo</span><span class="sxs-lookup"><span data-stu-id="37666-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="37666-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="37666-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="37666-121">Tabella hash che rappresenta i campi di mapping di input con il valore predefinito in formato tasto separato da spazi = valore.</span><span class="sxs-lookup"><span data-stu-id="37666-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="37666-122">I nomi di chiave consentiti sono subject, eventtype e dataversion.</span><span class="sxs-lookup"><span data-stu-id="37666-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="37666-123">Viene usato solo quando InputSchemaHelp è customeventschema.</span><span class="sxs-lookup"><span data-stu-id="37666-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="37666-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="37666-124">-InputMappingField</span></span>
<span data-ttu-id="37666-125">Tabella hash che rappresenta i campi di mapping di input in formato chiave separata da spazio = formato valore.</span><span class="sxs-lookup"><span data-stu-id="37666-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="37666-126">I nomi di chiave consentiti sono id, topic, eventtime, subject, eventtype e dataversion.</span><span class="sxs-lookup"><span data-stu-id="37666-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="37666-127">Viene usato solo quando InputSchemaHelp è customeventschema.</span><span class="sxs-lookup"><span data-stu-id="37666-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="37666-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="37666-128">-InputSchema</span></span>
<span data-ttu-id="37666-129">Schema degli eventi di input per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="37666-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="37666-130">I valori consentiti sono: eventgridschema, customeventschema o cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="37666-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="37666-131">Il valore predefinito è eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="37666-131">Default value is eventgridschema.</span></span> <span data-ttu-id="37666-132">Si noti che se si specifica customeventschema, è necessario specificare anche i parametri InputMappingField o/e InputMappingDefaultValue.</span><span class="sxs-lookup"><span data-stu-id="37666-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="37666-133">-Location</span><span class="sxs-lookup"><span data-stu-id="37666-133">-Location</span></span>
<span data-ttu-id="37666-134">Posizione del dominio.</span><span class="sxs-lookup"><span data-stu-id="37666-134">The location of the domain.</span></span>

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

### <span data-ttu-id="37666-135">-Name</span><span class="sxs-lookup"><span data-stu-id="37666-135">-Name</span></span>
<span data-ttu-id="37666-136">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="37666-136">EventGrid domain name.</span></span>

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

### <span data-ttu-id="37666-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="37666-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="37666-138">Questo determina se il traffico è consentito su una rete pubblica.</span><span class="sxs-lookup"><span data-stu-id="37666-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="37666-139">Per impostazione predefinita, è abilitata.</span><span class="sxs-lookup"><span data-stu-id="37666-139">By default it is enabled.</span></span> <span data-ttu-id="37666-140">È possibile limitare ulteriormente l'accesso a specifici IP configurando parametri InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="37666-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="37666-141">I valori consentiti sono disabilitati e abilitati.</span><span class="sxs-lookup"><span data-stu-id="37666-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="37666-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37666-142">-ResourceGroupName</span></span>
<span data-ttu-id="37666-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37666-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="37666-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="37666-144">-Tag</span></span>
<span data-ttu-id="37666-145">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="37666-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="37666-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37666-146">-Confirm</span></span>
<span data-ttu-id="37666-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37666-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37666-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37666-148">-WhatIf</span></span>
<span data-ttu-id="37666-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37666-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37666-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37666-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37666-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37666-151">CommonParameters</span></span>
<span data-ttu-id="37666-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37666-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37666-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37666-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37666-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="37666-154">INPUTS</span></span>

### <span data-ttu-id="37666-155">System.String</span><span class="sxs-lookup"><span data-stu-id="37666-155">System.String</span></span>

### <span data-ttu-id="37666-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="37666-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="37666-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37666-157">OUTPUTS</span></span>

### <span data-ttu-id="37666-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="37666-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="37666-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="37666-159">NOTES</span></span>

## <span data-ttu-id="37666-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37666-160">RELATED LINKS</span></span>
