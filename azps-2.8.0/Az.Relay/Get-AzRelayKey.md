---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 68ba115bb74bf0eae780944037532b0d37424704
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854989"
---
# <span data-ttu-id="29292-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="29292-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="29292-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29292-102">SYNOPSIS</span></span>
<span data-ttu-id="29292-103">Ottiene le stringhe di connessione primarie e secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="29292-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="29292-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29292-104">SYNTAX</span></span>

### <span data-ttu-id="29292-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29292-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29292-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="29292-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29292-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="29292-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29292-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29292-108">DESCRIPTION</span></span>
<span data-ttu-id="29292-109">Il cmdlet **Get-AzRelayKey** restituisce le stringhe di connessione primarie e secondarie per le entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="29292-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="29292-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29292-110">EXAMPLES</span></span>

### <span data-ttu-id="29292-111">Esempio 1-spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="29292-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="29292-112">Esempio 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="29292-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="29292-113">Esempio 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="29292-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="29292-114">Stringa di connessione primaria e secondaria alle entità di inoltro specificate (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="29292-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="29292-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29292-115">PARAMETERS</span></span>

### <span data-ttu-id="29292-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29292-116">-DefaultProfile</span></span>
<span data-ttu-id="29292-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29292-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29292-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="29292-118">-HybridConnection</span></span>
<span data-ttu-id="29292-119">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="29292-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="29292-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="29292-120">-Name</span></span>
<span data-ttu-id="29292-121">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="29292-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="29292-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="29292-122">-Namespace</span></span>
<span data-ttu-id="29292-123">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="29292-123">Namespace Name.</span></span>

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

### <span data-ttu-id="29292-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29292-124">-ResourceGroupName</span></span>
<span data-ttu-id="29292-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="29292-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="29292-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="29292-126">-WcfRelay</span></span>
<span data-ttu-id="29292-127">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="29292-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="29292-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29292-128">CommonParameters</span></span>
<span data-ttu-id="29292-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29292-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29292-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29292-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29292-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29292-131">INPUTS</span></span>

### <span data-ttu-id="29292-132">System. String</span><span class="sxs-lookup"><span data-stu-id="29292-132">System.String</span></span>

## <span data-ttu-id="29292-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29292-133">OUTPUTS</span></span>

### <span data-ttu-id="29292-134">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="29292-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="29292-135">Note</span><span class="sxs-lookup"><span data-stu-id="29292-135">NOTES</span></span>

## <span data-ttu-id="29292-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29292-136">RELATED LINKS</span></span>
