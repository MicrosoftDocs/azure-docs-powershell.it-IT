---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: da2794fc390ecce13c466fc4ff2d2efb92205a8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512284"
---
# <span data-ttu-id="77cb6-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="77cb6-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="77cb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="77cb6-103">Ottiene le stringhe di connessione primarie e secondarie per lo spazio dei nomi o la coda o l'argomento o l'alias (configurazioni GeoDR) specificati.</span><span class="sxs-lookup"><span data-stu-id="77cb6-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77cb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77cb6-104">SYNTAX</span></span>

### <span data-ttu-id="77cb6-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77cb6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77cb6-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="77cb6-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77cb6-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="77cb6-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77cb6-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="77cb6-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77cb6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77cb6-109">DESCRIPTION</span></span>
<span data-ttu-id="77cb6-110">Il cmdlet **Get-AzureRmServiceBusKey** restituisce le stringhe di connessione primarie e secondarie per lo spazio dei nomi o la coda o l'argomento o l'alias specificato (configurazioni GeoDR).</span><span class="sxs-lookup"><span data-stu-id="77cb6-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="77cb6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77cb6-111">EXAMPLES</span></span>

### <span data-ttu-id="77cb6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77cb6-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="77cb6-113">Stringa di connessione primaria e secondaria allo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="77cb6-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="77cb6-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="77cb6-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="77cb6-115">Stringa di connessione primaria e secondaria alla coda specificata.</span><span class="sxs-lookup"><span data-stu-id="77cb6-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="77cb6-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="77cb6-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="77cb6-117">Stringa di connessione primaria e secondaria all'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="77cb6-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="77cb6-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="77cb6-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="77cb6-119">Stringa di connessione primaria e secondaria allo spazio dei nomi e all'alias specificati.</span><span class="sxs-lookup"><span data-stu-id="77cb6-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="77cb6-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77cb6-120">PARAMETERS</span></span>

### <span data-ttu-id="77cb6-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="77cb6-121">-AliasName</span></span>
<span data-ttu-id="77cb6-122">Nome alias</span><span class="sxs-lookup"><span data-stu-id="77cb6-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cb6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77cb6-123">-DefaultProfile</span></span>
<span data-ttu-id="77cb6-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77cb6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77cb6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="77cb6-125">-Name</span></span>
<span data-ttu-id="77cb6-126">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="77cb6-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cb6-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77cb6-127">-Namespace</span></span>
<span data-ttu-id="77cb6-128">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77cb6-128">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cb6-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="77cb6-129">-Queue</span></span>
<span data-ttu-id="77cb6-130">Nome coda</span><span class="sxs-lookup"><span data-stu-id="77cb6-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cb6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77cb6-131">-ResourceGroupName</span></span>
<span data-ttu-id="77cb6-132">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="77cb6-132">Resource Group Name</span></span>

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

### <span data-ttu-id="77cb6-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="77cb6-133">-Topic</span></span>
<span data-ttu-id="77cb6-134">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="77cb6-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77cb6-135">CommonParameters</span></span>
<span data-ttu-id="77cb6-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77cb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="77cb6-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77cb6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77cb6-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77cb6-138">INPUTS</span></span>

### <span data-ttu-id="77cb6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="77cb6-139">System.String</span></span>


## <span data-ttu-id="77cb6-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77cb6-140">OUTPUTS</span></span>

### <span data-ttu-id="77cb6-141">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="77cb6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="77cb6-142">Note</span><span class="sxs-lookup"><span data-stu-id="77cb6-142">NOTES</span></span>

## <span data-ttu-id="77cb6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77cb6-143">RELATED LINKS</span></span>
