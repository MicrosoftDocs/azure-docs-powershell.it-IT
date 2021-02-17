---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208595"
---
# <span data-ttu-id="ca4b9-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="ca4b9-101">New-AzRelayKey</span></span>

## <span data-ttu-id="ca4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4b9-103">Rigenera le stringhe di connessione primaria o secondaria per le entità di inoltro specificate (Spazio dei nomi/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="ca4b9-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="ca4b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca4b9-104">SYNTAX</span></span>

### <span data-ttu-id="ca4b9-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca4b9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca4b9-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca4b9-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca4b9-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ca4b9-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca4b9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca4b9-108">DESCRIPTION</span></span>
<span data-ttu-id="ca4b9-109">Il cmdlet **New-AzRelayKey** genera le stringhe di connessione primaria e secondaria per le entità di inoltro specificate (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ca4b9-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ca4b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca4b9-110">EXAMPLES</span></span>

### <span data-ttu-id="ca4b9-111">Esempio 1 - Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca4b9-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ca4b9-112">Rigenera le stringhe di connessione primaria o secondaria per l'entità Relay-Namespace specificata.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="ca4b9-113">Esempio 1.1 - Spazio dei nomi keyValue fornito</span><span class="sxs-lookup"><span data-stu-id="ca4b9-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ca4b9-114">genera le stringhe di connessione primaria o secondaria per l'entità Relay-Namespace specificata con valore di chiave fornito</span><span class="sxs-lookup"><span data-stu-id="ca4b9-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="ca4b9-115">Esempio 2 - WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ca4b9-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ca4b9-116">Rigenera le stringhe di connessione primaria o secondaria per l'entità Relay-WcfRelay specificata.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="ca4b9-117">Esempio 2.1 - WcfRelay KeyValue fornito</span><span class="sxs-lookup"><span data-stu-id="ca4b9-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ca4b9-118">genera le stringhe di connessione primaria o secondaria per l'entità Relay-WcfRelay specificata con valore di chiave fornito</span><span class="sxs-lookup"><span data-stu-id="ca4b9-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="ca4b9-119">Esempio 3 - HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ca4b9-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ca4b9-120">Rigenera le stringhe di connessione primaria o secondaria per le entità di inoltro specificate (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ca4b9-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="ca4b9-121">Esempio 3.1 - Fornito HybridConnection KeyValue</span><span class="sxs-lookup"><span data-stu-id="ca4b9-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ca4b9-122">genera le stringhe di connessione primaria o secondaria per l'entità Relay-HybridConnection specificata con valore di chiave fornito</span><span class="sxs-lookup"><span data-stu-id="ca4b9-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="ca4b9-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca4b9-123">PARAMETERS</span></span>

### <span data-ttu-id="ca4b9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca4b9-124">-DefaultProfile</span></span>
<span data-ttu-id="ca4b9-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca4b9-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ca4b9-126">-HybridConnection</span></span>
<span data-ttu-id="ca4b9-127">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-127">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="ca4b9-128">-KeyValue</span></span>
<span data-ttu-id="ca4b9-129">Chiave a 256 bit codificata in base64 per firmare e convalidare il token di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-130">-Name</span><span class="sxs-lookup"><span data-stu-id="ca4b9-130">-Name</span></span>
<span data-ttu-id="ca4b9-131">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-131">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-132">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca4b9-132">-Namespace</span></span>
<span data-ttu-id="ca4b9-133">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-133">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="ca4b9-134">-RegenerateKey</span></span>
<span data-ttu-id="ca4b9-135">Rigenerare le chiavi - 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca4b9-136">-ResourceGroupName</span></span>
<span data-ttu-id="ca4b9-137">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ca4b9-138">-WcfRelay</span></span>
<span data-ttu-id="ca4b9-139">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-139">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca4b9-140">-Confirm</span></span>
<span data-ttu-id="ca4b9-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca4b9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca4b9-142">-WhatIf</span></span>
<span data-ttu-id="ca4b9-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca4b9-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca4b9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4b9-145">CommonParameters</span></span>
<span data-ttu-id="ca4b9-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4b9-147">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca4b9-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4b9-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca4b9-148">INPUTS</span></span>

### <span data-ttu-id="ca4b9-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ca4b9-149">System.String</span></span>

## <span data-ttu-id="ca4b9-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca4b9-150">OUTPUTS</span></span>

### <span data-ttu-id="ca4b9-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="ca4b9-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="ca4b9-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca4b9-152">NOTES</span></span>

## <span data-ttu-id="ca4b9-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca4b9-153">RELATED LINKS</span></span>
