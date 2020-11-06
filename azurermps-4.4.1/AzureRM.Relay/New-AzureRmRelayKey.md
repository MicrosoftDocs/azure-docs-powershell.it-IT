---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 7394ec382105b1d05bed589be95630f68ab79ae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519986"
---
# <span data-ttu-id="70e2e-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="70e2e-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="70e2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="70e2e-103">Rigenera le stringhe di connessione primarie o secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="70e2e-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70e2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70e2e-104">SYNTAX</span></span>

### <span data-ttu-id="70e2e-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70e2e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70e2e-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="70e2e-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70e2e-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="70e2e-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70e2e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70e2e-108">DESCRIPTION</span></span>
<span data-ttu-id="70e2e-109">Il cmdlet **New-AzureRmRelayKey** genera le stringhe di connessione primarie e secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="70e2e-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="70e2e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70e2e-110">EXAMPLES</span></span>

### <span data-ttu-id="70e2e-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70e2e-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="70e2e-112">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="70e2e-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="70e2e-113">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="70e2e-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="70e2e-114">Rigenera le stringhe di connessione primarie o secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="70e2e-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="70e2e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70e2e-115">PARAMETERS</span></span>

### <span data-ttu-id="70e2e-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="70e2e-116">-Confirm</span></span>
<span data-ttu-id="70e2e-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70e2e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70e2e-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="70e2e-118">-HybridConnection</span></span>
<span data-ttu-id="70e2e-119">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="70e2e-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="70e2e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="70e2e-120">-Name</span></span>
<span data-ttu-id="70e2e-121">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="70e2e-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="70e2e-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70e2e-122">-Namespace</span></span>
<span data-ttu-id="70e2e-123">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="70e2e-123">Namespace Name.</span></span>

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

### <span data-ttu-id="70e2e-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="70e2e-124">-RegenerateKey</span></span>
<span data-ttu-id="70e2e-125">Rigenera chiavi-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="70e2e-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="70e2e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e2e-126">-ResourceGroupName</span></span>
<span data-ttu-id="70e2e-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="70e2e-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="70e2e-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="70e2e-128">-WcfRelay</span></span>
<span data-ttu-id="70e2e-129">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="70e2e-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="70e2e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70e2e-130">-WhatIf</span></span>
<span data-ttu-id="70e2e-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70e2e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70e2e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70e2e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70e2e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e2e-133">-DefaultProfile</span></span>
<span data-ttu-id="70e2e-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70e2e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70e2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e2e-135">CommonParameters</span></span>
<span data-ttu-id="70e2e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e2e-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70e2e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e2e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70e2e-138">INPUTS</span></span>

### <span data-ttu-id="70e2e-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="70e2e-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="70e2e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="70e2e-140">System.String</span></span> 

### <span data-ttu-id="70e2e-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="70e2e-141">-NamespaceName</span></span>
 <span data-ttu-id="70e2e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="70e2e-142">System.String</span></span> 
 

### <span data-ttu-id="70e2e-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="70e2e-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="70e2e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="70e2e-144">System.String</span></span> 

### <span data-ttu-id="70e2e-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="70e2e-145">-WcfRelayName</span></span>
 <span data-ttu-id="70e2e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="70e2e-146">System.String</span></span> 

### <span data-ttu-id="70e2e-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="70e2e-147">-Name</span></span>
 <span data-ttu-id="70e2e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="70e2e-148">System.String</span></span>

### <span data-ttu-id="70e2e-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="70e2e-149">-RegenerateKeys</span></span>
 <span data-ttu-id="70e2e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="70e2e-150">System.String</span></span>

## <span data-ttu-id="70e2e-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70e2e-151">OUTPUTS</span></span>

### <span data-ttu-id="70e2e-152">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="70e2e-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="70e2e-153">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70e2e-153">Example 1 - Namespace</span></span>
<span data-ttu-id="70e2e-154">PrimaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SharedAccessKeyName = AuthoRule1; SharedAccessKey. # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="70e2e-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="70e2e-155">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="70e2e-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="70e2e-156">PrimaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #, # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="70e2e-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="70e2e-157">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="70e2e-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="70e2e-158">PrimaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #, # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="70e2e-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="70e2e-159">Note</span><span class="sxs-lookup"><span data-stu-id="70e2e-159">NOTES</span></span>

## <span data-ttu-id="70e2e-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70e2e-160">RELATED LINKS</span></span>

