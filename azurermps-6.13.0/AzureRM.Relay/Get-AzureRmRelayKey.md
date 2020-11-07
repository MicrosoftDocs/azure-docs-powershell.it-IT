---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 69f6b1bc50681bafe7a860dcebaa7616c8f14e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688377"
---
# <span data-ttu-id="96dd6-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="96dd6-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="96dd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="96dd6-103">Ottiene le stringhe di connessione primarie e secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="96dd6-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96dd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96dd6-104">SYNTAX</span></span>

### <span data-ttu-id="96dd6-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96dd6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96dd6-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="96dd6-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96dd6-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="96dd6-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96dd6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96dd6-108">DESCRIPTION</span></span>
<span data-ttu-id="96dd6-109">Il cmdlet **Get-AzureRmRelayKey** restituisce le stringhe di connessione primarie e secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="96dd6-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="96dd6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96dd6-110">EXAMPLES</span></span>

### <span data-ttu-id="96dd6-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="96dd6-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="96dd6-112">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="96dd6-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="96dd6-113">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="96dd6-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="96dd6-114">Stringa di connessione primaria e secondaria alle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="96dd6-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="96dd6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96dd6-115">PARAMETERS</span></span>

### <span data-ttu-id="96dd6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96dd6-116">-DefaultProfile</span></span>
<span data-ttu-id="96dd6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96dd6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96dd6-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="96dd6-118">-HybridConnection</span></span>
<span data-ttu-id="96dd6-119">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="96dd6-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="96dd6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="96dd6-120">-Name</span></span>
<span data-ttu-id="96dd6-121">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="96dd6-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="96dd6-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="96dd6-122">-Namespace</span></span>
<span data-ttu-id="96dd6-123">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="96dd6-123">Namespace Name.</span></span>

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

### <span data-ttu-id="96dd6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96dd6-124">-ResourceGroupName</span></span>
<span data-ttu-id="96dd6-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96dd6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="96dd6-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="96dd6-126">-WcfRelay</span></span>
<span data-ttu-id="96dd6-127">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="96dd6-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="96dd6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96dd6-128">CommonParameters</span></span>
<span data-ttu-id="96dd6-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96dd6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="96dd6-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96dd6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96dd6-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96dd6-131">INPUTS</span></span>

### <span data-ttu-id="96dd6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="96dd6-132">System.String</span></span>


## <span data-ttu-id="96dd6-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96dd6-133">OUTPUTS</span></span>

### <span data-ttu-id="96dd6-134">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="96dd6-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>


## <span data-ttu-id="96dd6-135">Note</span><span class="sxs-lookup"><span data-stu-id="96dd6-135">NOTES</span></span>

## <span data-ttu-id="96dd6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96dd6-136">RELATED LINKS</span></span>