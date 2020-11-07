---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 44e1571dbd6da015e163a69716f06d3ed3cebde5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685877"
---
# <span data-ttu-id="4bd4d-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="4bd4d-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="4bd4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd4d-103">Ottiene le stringhe di connessione primarie e secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="4bd4d-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bd4d-104">SYNTAX</span></span>

### <span data-ttu-id="4bd4d-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4bd4d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd4d-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd4d-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd4d-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd4d-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd4d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bd4d-108">DESCRIPTION</span></span>
<span data-ttu-id="4bd4d-109">Il cmdlet **Get-AzureRmRelayKey** restituisce le stringhe di connessione primarie e secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="4bd4d-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="4bd4d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bd4d-110">EXAMPLES</span></span>

### <span data-ttu-id="4bd4d-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4bd4d-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="4bd4d-112">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="4bd4d-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="4bd4d-113">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="4bd4d-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="4bd4d-114">Stringa di connessione primaria e secondaria alle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="4bd4d-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="4bd4d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bd4d-115">PARAMETERS</span></span>

### <span data-ttu-id="4bd4d-116">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="4bd4d-116">-HybridConnection</span></span>
<span data-ttu-id="4bd4d-117">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-117">HybridConnection Name.</span></span>

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

### <span data-ttu-id="4bd4d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bd4d-118">-Name</span></span>
<span data-ttu-id="4bd4d-119">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="4bd4d-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4bd4d-120">-Namespace</span></span>
<span data-ttu-id="4bd4d-121">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-121">Namespace Name.</span></span>

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

### <span data-ttu-id="4bd4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="4bd4d-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="4bd4d-124">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="4bd4d-124">-WcfRelay</span></span>
<span data-ttu-id="4bd4d-125">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-125">WcfRelay Name.</span></span>

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

### <span data-ttu-id="4bd4d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd4d-126">-DefaultProfile</span></span>
<span data-ttu-id="4bd4d-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bd4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd4d-128">CommonParameters</span></span>
<span data-ttu-id="4bd4d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd4d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd4d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd4d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bd4d-131">INPUTS</span></span>

### <span data-ttu-id="4bd4d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd4d-132">-ResourceGroupName</span></span>
 <span data-ttu-id="4bd4d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd4d-133">System.String</span></span> 

### <span data-ttu-id="4bd4d-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4bd4d-134">-NamespaceName</span></span>
 <span data-ttu-id="4bd4d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd4d-135">System.String</span></span> 
 

### <span data-ttu-id="4bd4d-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="4bd4d-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="4bd4d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd4d-137">System.String</span></span> 

### <span data-ttu-id="4bd4d-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="4bd4d-138">-WcfRelayName</span></span>
 <span data-ttu-id="4bd4d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd4d-139">System.String</span></span> 

### <span data-ttu-id="4bd4d-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bd4d-140">-Name</span></span>
 <span data-ttu-id="4bd4d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd4d-141">System.String</span></span>

## <span data-ttu-id="4bd4d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bd4d-142">OUTPUTS</span></span>

### <span data-ttu-id="4bd4d-143">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="4bd4d-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="4bd4d-144">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4bd4d-144">Example 1 - Namespace</span></span>
<span data-ttu-id="4bd4d-145">PrimaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SharedAccessKeyName = AuthoRule1; SharedAccessKey. # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="4bd4d-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="4bd4d-146">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="4bd4d-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="4bd4d-147">PrimaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #, # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="4bd4d-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="4bd4d-148">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="4bd4d-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="4bd4d-149">PrimaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #, # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="4bd4d-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="4bd4d-150">Note</span><span class="sxs-lookup"><span data-stu-id="4bd4d-150">NOTES</span></span>

## <span data-ttu-id="4bd4d-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bd4d-151">RELATED LINKS</span></span>

