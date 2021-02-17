---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 87682e5aa7b3c6ab5f7cc5ba4200d73f45960001
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206090"
---
# <span data-ttu-id="08f50-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="08f50-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="08f50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08f50-102">SYNOPSIS</span></span>
<span data-ttu-id="08f50-103">Ottiene le stringhe di connessione primaria e secondaria per le entità di inoltro specificate (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="08f50-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="08f50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08f50-104">SYNTAX</span></span>

### <span data-ttu-id="08f50-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08f50-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08f50-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="08f50-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08f50-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="08f50-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08f50-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="08f50-108">DESCRIPTION</span></span>
<span data-ttu-id="08f50-109">Il cmdlet **Get-AzRelayKey** restituisce le stringhe di connessione primaria e secondaria per le entità di inoltro specificate (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="08f50-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="08f50-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08f50-110">EXAMPLES</span></span>

### <span data-ttu-id="08f50-111">Esempio 1: Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08f50-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="08f50-112">Esempio 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="08f50-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="08f50-113">Esempio 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="08f50-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="08f50-114">Stringa di connessione primaria e secondaria alle entità di inoltro specificate (Spazio dei nomi/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="08f50-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="08f50-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08f50-115">PARAMETERS</span></span>

### <span data-ttu-id="08f50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f50-116">-DefaultProfile</span></span>
<span data-ttu-id="08f50-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08f50-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f50-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="08f50-118">-HybridConnection</span></span>
<span data-ttu-id="08f50-119">Nome HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="08f50-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="08f50-120">-Name</span><span class="sxs-lookup"><span data-stu-id="08f50-120">-Name</span></span>
<span data-ttu-id="08f50-121">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="08f50-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="08f50-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08f50-122">-Namespace</span></span>
<span data-ttu-id="08f50-123">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="08f50-123">Namespace Name.</span></span>

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

### <span data-ttu-id="08f50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f50-124">-ResourceGroupName</span></span>
<span data-ttu-id="08f50-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="08f50-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="08f50-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="08f50-126">-WcfRelay</span></span>
<span data-ttu-id="08f50-127">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="08f50-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="08f50-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f50-128">CommonParameters</span></span>
<span data-ttu-id="08f50-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f50-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f50-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08f50-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f50-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="08f50-131">INPUTS</span></span>

### <span data-ttu-id="08f50-132">System.String</span><span class="sxs-lookup"><span data-stu-id="08f50-132">System.String</span></span>

## <span data-ttu-id="08f50-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08f50-133">OUTPUTS</span></span>

### <span data-ttu-id="08f50-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="08f50-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="08f50-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="08f50-135">NOTES</span></span>

## <span data-ttu-id="08f50-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08f50-136">RELATED LINKS</span></span>
