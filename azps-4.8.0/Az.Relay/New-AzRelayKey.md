---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192654"
---
# <span data-ttu-id="fc9ae-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="fc9ae-101">New-AzRelayKey</span></span>

## <span data-ttu-id="fc9ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fc9ae-103">Rigenera le stringhe di connessione primarie o secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="fc9ae-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="fc9ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc9ae-104">SYNTAX</span></span>

### <span data-ttu-id="fc9ae-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc9ae-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc9ae-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc9ae-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc9ae-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc9ae-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc9ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc9ae-108">DESCRIPTION</span></span>
<span data-ttu-id="fc9ae-109">Il cmdlet **New-AzRelayKey** genera le stringhe di connessione primarie e secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fc9ae-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="fc9ae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc9ae-110">EXAMPLES</span></span>

### <span data-ttu-id="fc9ae-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fc9ae-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="fc9ae-112">Rigenera le stringhe di connessione primarie o secondarie per l'entità Relay-Namespace specificata.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="fc9ae-113">Esempio 1,1-valore della valorizzazione di spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="fc9ae-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="fc9ae-114">genera le stringhe di connessione primarie o secondarie per l'entità Relay-Namespace specificata con il valore di chiave specificato</span><span class="sxs-lookup"><span data-stu-id="fc9ae-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="fc9ae-115">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="fc9ae-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="fc9ae-116">Rigenera le stringhe di connessione primarie o secondarie per l'entità Relay-WcfRelay specificata.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="fc9ae-117">Esempio 2,1-valore di WcfRelay fornito</span><span class="sxs-lookup"><span data-stu-id="fc9ae-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="fc9ae-118">genera le stringhe di connessione primarie o secondarie per l'entità Relay-WcfRelay specificata con il valore di chiave specificato</span><span class="sxs-lookup"><span data-stu-id="fc9ae-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="fc9ae-119">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="fc9ae-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="fc9ae-120">Rigenera le stringhe di connessione primarie o secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="fc9ae-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="fc9ae-121">Esempio 3,1-valore di HybridConnection fornito</span><span class="sxs-lookup"><span data-stu-id="fc9ae-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="fc9ae-122">genera le stringhe di connessione primarie o secondarie per l'entità Relay-HybridConnection specificata con il valore di chiave specificato</span><span class="sxs-lookup"><span data-stu-id="fc9ae-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="fc9ae-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc9ae-123">PARAMETERS</span></span>

### <span data-ttu-id="fc9ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc9ae-124">-DefaultProfile</span></span>
<span data-ttu-id="fc9ae-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc9ae-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="fc9ae-126">-HybridConnection</span></span>
<span data-ttu-id="fc9ae-127">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="fc9ae-128">-Valore della stessa</span><span class="sxs-lookup"><span data-stu-id="fc9ae-128">-KeyValue</span></span>
<span data-ttu-id="fc9ae-129">Una chiave a 256 bit con codifica Base64 per la firma e la convalida del token SAS.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="fc9ae-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc9ae-130">-Name</span></span>
<span data-ttu-id="fc9ae-131">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="fc9ae-132">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fc9ae-132">-Namespace</span></span>
<span data-ttu-id="fc9ae-133">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-133">Namespace Name.</span></span>

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

### <span data-ttu-id="fc9ae-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="fc9ae-134">-RegenerateKey</span></span>
<span data-ttu-id="fc9ae-135">Rigenera chiavi-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="fc9ae-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc9ae-136">-ResourceGroupName</span></span>
<span data-ttu-id="fc9ae-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc9ae-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="fc9ae-138">-WcfRelay</span></span>
<span data-ttu-id="fc9ae-139">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="fc9ae-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fc9ae-140">-Confirm</span></span>
<span data-ttu-id="fc9ae-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc9ae-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc9ae-142">-WhatIf</span></span>
<span data-ttu-id="fc9ae-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc9ae-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc9ae-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc9ae-145">CommonParameters</span></span>
<span data-ttu-id="fc9ae-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc9ae-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc9ae-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc9ae-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc9ae-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc9ae-148">INPUTS</span></span>

### <span data-ttu-id="fc9ae-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fc9ae-149">System.String</span></span>

## <span data-ttu-id="fc9ae-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc9ae-150">OUTPUTS</span></span>

### <span data-ttu-id="fc9ae-151">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="fc9ae-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="fc9ae-152">Note</span><span class="sxs-lookup"><span data-stu-id="fc9ae-152">NOTES</span></span>

## <span data-ttu-id="fc9ae-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc9ae-153">RELATED LINKS</span></span>
