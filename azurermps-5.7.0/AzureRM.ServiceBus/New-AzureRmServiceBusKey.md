---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0dc0e2ebf22d995577abd37e2eef2b16b0ea4001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519366"
---
# <span data-ttu-id="78f34-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="78f34-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="78f34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78f34-102">SYNOPSIS</span></span>
<span data-ttu-id="78f34-103">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi Service Bus o la coda o l'argomento.</span><span class="sxs-lookup"><span data-stu-id="78f34-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78f34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78f34-104">SYNTAX</span></span>

### <span data-ttu-id="78f34-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78f34-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f34-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="78f34-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78f34-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="78f34-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f34-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78f34-108">DESCRIPTION</span></span>
<span data-ttu-id="78f34-109">Il cmdlet **New-AzureRmServiceBusKey** genera nuove stringhe di connessione primarie o secondarie per lo spazio dei nomi o le code o gli argomenti e le regole di autorizzazione specificati.</span><span class="sxs-lookup"><span data-stu-id="78f34-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="78f34-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78f34-110">EXAMPLES</span></span>

### <span data-ttu-id="78f34-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="78f34-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="78f34-112">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="78f34-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="78f34-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="78f34-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="78f34-114">Rigenera le stringhe di connessione primarie o secondarie per la coda.</span><span class="sxs-lookup"><span data-stu-id="78f34-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="78f34-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="78f34-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="78f34-116">Rigenera le stringhe di connessione primarie o secondarie per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="78f34-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="78f34-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78f34-117">PARAMETERS</span></span>

### <span data-ttu-id="78f34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f34-118">-DefaultProfile</span></span>
<span data-ttu-id="78f34-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78f34-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f34-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="78f34-120">-Name</span></span>
<span data-ttu-id="78f34-121">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="78f34-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="78f34-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="78f34-122">-Namespace</span></span>
<span data-ttu-id="78f34-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="78f34-123">Namespace Name</span></span>

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

### <span data-ttu-id="78f34-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="78f34-124">-Queue</span></span>
<span data-ttu-id="78f34-125">Nome coda</span><span class="sxs-lookup"><span data-stu-id="78f34-125">Queue Name</span></span>

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

### <span data-ttu-id="78f34-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="78f34-126">-RegenerateKey</span></span>
<span data-ttu-id="78f34-127">Rigenera chiavi-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="78f34-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78f34-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78f34-128">-ResourceGroupName</span></span>
<span data-ttu-id="78f34-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="78f34-129">Resource Group Name</span></span>

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

### <span data-ttu-id="78f34-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="78f34-130">-Topic</span></span>
<span data-ttu-id="78f34-131">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="78f34-131">Topic Name</span></span>

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

### <span data-ttu-id="78f34-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="78f34-132">-Confirm</span></span>
<span data-ttu-id="78f34-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78f34-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f34-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f34-134">-WhatIf</span></span>
<span data-ttu-id="78f34-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78f34-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f34-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78f34-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f34-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f34-137">CommonParameters</span></span>
<span data-ttu-id="78f34-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f34-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="78f34-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f34-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f34-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78f34-140">INPUTS</span></span>

### <span data-ttu-id="78f34-141">System. String</span><span class="sxs-lookup"><span data-stu-id="78f34-141">System.String</span></span>


## <span data-ttu-id="78f34-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78f34-142">OUTPUTS</span></span>

### <span data-ttu-id="78f34-143">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="78f34-143">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="78f34-144">Note</span><span class="sxs-lookup"><span data-stu-id="78f34-144">NOTES</span></span>

## <span data-ttu-id="78f34-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78f34-145">RELATED LINKS</span></span>
