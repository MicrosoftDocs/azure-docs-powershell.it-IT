---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 050d6477a25922236dc2d9d2e28db1228f4666fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519878"
---
# <span data-ttu-id="34094-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="34094-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="34094-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34094-102">SYNOPSIS</span></span>
<span data-ttu-id="34094-103">Rigenera le stringhe di connessione primarie o secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="34094-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34094-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34094-104">SYNTAX</span></span>

### <span data-ttu-id="34094-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34094-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34094-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="34094-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34094-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="34094-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34094-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34094-108">DESCRIPTION</span></span>
<span data-ttu-id="34094-109">Il cmdlet **New-AzureRmRelayKey** genera le stringhe di connessione primarie e secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="34094-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="34094-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34094-110">EXAMPLES</span></span>

### <span data-ttu-id="34094-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34094-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="34094-112">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="34094-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="34094-113">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="34094-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="34094-114">Rigenera le stringhe di connessione primarie o secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="34094-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="34094-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34094-115">PARAMETERS</span></span>

### <span data-ttu-id="34094-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34094-116">-DefaultProfile</span></span>
<span data-ttu-id="34094-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34094-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34094-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="34094-118">-HybridConnection</span></span>
<span data-ttu-id="34094-119">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="34094-119">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34094-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="34094-120">-Name</span></span>
<span data-ttu-id="34094-121">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="34094-121">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34094-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34094-122">-Namespace</span></span>
<span data-ttu-id="34094-123">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="34094-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34094-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="34094-124">-RegenerateKey</span></span>
<span data-ttu-id="34094-125">Rigenera chiavi-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="34094-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34094-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34094-126">-ResourceGroupName</span></span>
<span data-ttu-id="34094-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34094-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34094-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="34094-128">-WcfRelay</span></span>
<span data-ttu-id="34094-129">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="34094-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34094-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34094-130">-Confirm</span></span>
<span data-ttu-id="34094-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34094-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34094-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34094-132">-WhatIf</span></span>
<span data-ttu-id="34094-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34094-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34094-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34094-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34094-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34094-135">CommonParameters</span></span>
<span data-ttu-id="34094-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34094-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34094-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34094-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34094-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34094-138">INPUTS</span></span>

### <span data-ttu-id="34094-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="34094-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="34094-140">System. String</span><span class="sxs-lookup"><span data-stu-id="34094-140">System.String</span></span> 

### <span data-ttu-id="34094-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="34094-141">-NamespaceName</span></span>
 <span data-ttu-id="34094-142">System. String</span><span class="sxs-lookup"><span data-stu-id="34094-142">System.String</span></span> 
 

### <span data-ttu-id="34094-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="34094-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="34094-144">System. String</span><span class="sxs-lookup"><span data-stu-id="34094-144">System.String</span></span> 

### <span data-ttu-id="34094-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="34094-145">-WcfRelayName</span></span>
 <span data-ttu-id="34094-146">System. String</span><span class="sxs-lookup"><span data-stu-id="34094-146">System.String</span></span> 

### <span data-ttu-id="34094-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="34094-147">-Name</span></span>
 <span data-ttu-id="34094-148">System. String</span><span class="sxs-lookup"><span data-stu-id="34094-148">System.String</span></span>

### <span data-ttu-id="34094-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="34094-149">-RegenerateKeys</span></span>
 <span data-ttu-id="34094-150">System. String</span><span class="sxs-lookup"><span data-stu-id="34094-150">System.String</span></span>

## <span data-ttu-id="34094-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34094-151">OUTPUTS</span></span>

### <span data-ttu-id="34094-152">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="34094-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="34094-153">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34094-153">Example 1 - Namespace</span></span>
<span data-ttu-id="34094-154">PrimaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SharedAccessKeyName = AuthoRule1; SharedAccessKey. # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="34094-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="34094-155">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="34094-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="34094-156">PrimaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #, # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="34094-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="34094-157">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="34094-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="34094-158">PrimaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #, # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="34094-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="34094-159">Note</span><span class="sxs-lookup"><span data-stu-id="34094-159">NOTES</span></span>

## <span data-ttu-id="34094-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34094-160">RELATED LINKS</span></span>

