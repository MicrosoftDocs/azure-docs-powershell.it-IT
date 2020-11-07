---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 6e20ceb2a6809e1e6010263563006468753cd41c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687690"
---
# <span data-ttu-id="1f9e7-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1f9e7-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="1f9e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9e7-103">Crea una nuova regola di autorizzazione per lo spazio dei nomi Service Bus specificato</span><span class="sxs-lookup"><span data-stu-id="1f9e7-103">Creates a new authorization rule for the specified Service Bus namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f9e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f9e7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f9e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f9e7-105">DESCRIPTION</span></span>
<span data-ttu-id="1f9e7-106">Il cmdlet **New-AzureRmServiceBusNamespaceAuthorizationRule** crea una nuova regola di autorizzazione per lo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="1f9e7-106">The **New-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1f9e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f9e7-107">EXAMPLES</span></span>

### <span data-ttu-id="1f9e7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f9e7-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="1f9e7-109">Crea `AuthoRule1` con i diritti di **ascolto** e **invio** per lo spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="1f9e7-109">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="1f9e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f9e7-110">PARAMETERS</span></span>

### <span data-ttu-id="1f9e7-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f9e7-111">-ResourceGroup</span></span>
<span data-ttu-id="1f9e7-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f9e7-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f9e7-113">-Diritti</span><span class="sxs-lookup"><span data-stu-id="1f9e7-113">-Rights</span></span>
<span data-ttu-id="1f9e7-114">I diritti; ad esempio, @ ("Listen", "Send", "Manage")</span><span class="sxs-lookup"><span data-stu-id="1f9e7-114">The Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e7-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f9e7-115">-Confirm</span></span>
<span data-ttu-id="1f9e7-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f9e7-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f9e7-117">-WhatIf</span></span>
<span data-ttu-id="1f9e7-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f9e7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f9e7-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f9e7-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f9e7-120">-DefaultProfile</span></span>
<span data-ttu-id="1f9e7-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9e7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f9e7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f9e7-122">-Name</span></span>
<span data-ttu-id="1f9e7-123">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="1f9e7-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e7-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1f9e7-124">-Namespace</span></span>
<span data-ttu-id="1f9e7-125">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="1f9e7-125">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9e7-126">CommonParameters</span></span>
<span data-ttu-id="1f9e7-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f9e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9e7-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f9e7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9e7-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f9e7-129">INPUTS</span></span>

### <span data-ttu-id="1f9e7-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f9e7-130">-ResourceGroup</span></span>
 <span data-ttu-id="1f9e7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1f9e7-131">System.String</span></span>
 

### <span data-ttu-id="1f9e7-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1f9e7-132">-NamespaceName</span></span>
 <span data-ttu-id="1f9e7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1f9e7-133">System.String</span></span>
 

### <span data-ttu-id="1f9e7-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="1f9e7-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="1f9e7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1f9e7-135">System.String</span></span>
 

### <span data-ttu-id="1f9e7-136">-Diritti</span><span class="sxs-lookup"><span data-stu-id="1f9e7-136">-Rights</span></span>
 <span data-ttu-id="1f9e7-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="1f9e7-137">System.String []</span></span>

## <span data-ttu-id="1f9e7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f9e7-138">OUTPUTS</span></span>

### <span data-ttu-id="1f9e7-139">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1f9e7-139">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="1f9e7-140">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 tipo: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 location: Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="1f9e7-140">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="1f9e7-141">Note</span><span class="sxs-lookup"><span data-stu-id="1f9e7-141">NOTES</span></span>

## <span data-ttu-id="1f9e7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f9e7-142">RELATED LINKS</span></span>

