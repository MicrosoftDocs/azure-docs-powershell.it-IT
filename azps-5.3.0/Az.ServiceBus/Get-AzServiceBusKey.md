---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486116"
---
# <span data-ttu-id="28fe5-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="28fe5-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="28fe5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="28fe5-103">Ottiene le stringhe di connessione primarie e secondarie per lo spazio dei nomi o la coda o l'argomento o l'alias (configurazioni GeoDR) specificati.</span><span class="sxs-lookup"><span data-stu-id="28fe5-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="28fe5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28fe5-104">SYNTAX</span></span>

### <span data-ttu-id="28fe5-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28fe5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28fe5-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="28fe5-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28fe5-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="28fe5-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28fe5-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="28fe5-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28fe5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28fe5-109">DESCRIPTION</span></span>
<span data-ttu-id="28fe5-110">Il cmdlet **Get-AzServiceBusKey** restituisce le stringhe di connessione primarie e secondarie per lo spazio dei nomi o la coda o l'argomento o l'alias specificato (configurazioni GeoDR).</span><span class="sxs-lookup"><span data-stu-id="28fe5-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="28fe5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28fe5-111">EXAMPLES</span></span>

### <span data-ttu-id="28fe5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28fe5-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="28fe5-113">Stringa di connessione primaria e secondaria allo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="28fe5-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="28fe5-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="28fe5-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="28fe5-115">Stringa di connessione primaria e secondaria alla coda specificata.</span><span class="sxs-lookup"><span data-stu-id="28fe5-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="28fe5-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="28fe5-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="28fe5-117">Stringa di connessione primaria e secondaria all'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="28fe5-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="28fe5-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="28fe5-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="28fe5-119">Stringa di connessione primaria e secondaria allo spazio dei nomi e all'alias specificati.</span><span class="sxs-lookup"><span data-stu-id="28fe5-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="28fe5-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28fe5-120">PARAMETERS</span></span>

### <span data-ttu-id="28fe5-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="28fe5-121">-AliasName</span></span>
<span data-ttu-id="28fe5-122">Nome alias</span><span class="sxs-lookup"><span data-stu-id="28fe5-122">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28fe5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28fe5-123">-DefaultProfile</span></span>
<span data-ttu-id="28fe5-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28fe5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28fe5-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="28fe5-125">-Name</span></span>
<span data-ttu-id="28fe5-126">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="28fe5-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28fe5-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="28fe5-127">-Namespace</span></span>
<span data-ttu-id="28fe5-128">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="28fe5-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28fe5-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="28fe5-129">-Queue</span></span>
<span data-ttu-id="28fe5-130">Nome coda</span><span class="sxs-lookup"><span data-stu-id="28fe5-130">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28fe5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28fe5-131">-ResourceGroupName</span></span>
<span data-ttu-id="28fe5-132">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="28fe5-132">Resource Group Name</span></span>

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

### <span data-ttu-id="28fe5-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="28fe5-133">-Topic</span></span>
<span data-ttu-id="28fe5-134">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="28fe5-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28fe5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28fe5-135">CommonParameters</span></span>
<span data-ttu-id="28fe5-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28fe5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28fe5-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28fe5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28fe5-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28fe5-138">INPUTS</span></span>

### <span data-ttu-id="28fe5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="28fe5-139">System.String</span></span>

## <span data-ttu-id="28fe5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28fe5-140">OUTPUTS</span></span>

### <span data-ttu-id="28fe5-141">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="28fe5-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="28fe5-142">Note</span><span class="sxs-lookup"><span data-stu-id="28fe5-142">NOTES</span></span>

## <span data-ttu-id="28fe5-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28fe5-143">RELATED LINKS</span></span>
