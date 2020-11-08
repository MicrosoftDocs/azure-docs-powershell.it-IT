---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192919"
---
# <span data-ttu-id="9d83b-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9d83b-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="9d83b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d83b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d83b-103">Aggiorna la regola di autorizzazione specificata in un hub eventi.</span><span class="sxs-lookup"><span data-stu-id="9d83b-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="9d83b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d83b-104">SYNTAX</span></span>

### <span data-ttu-id="9d83b-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d83b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d83b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9d83b-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d83b-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9d83b-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d83b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d83b-108">DESCRIPTION</span></span>
<span data-ttu-id="9d83b-109">Il cmdlet Set-AzEventHubAuthorizationRule aggiorna la regola di autorizzazione specificata nell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="9d83b-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="9d83b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d83b-110">EXAMPLES</span></span>

### <span data-ttu-id="9d83b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d83b-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="9d83b-112">Aggiorna la regola di autorizzazione \` MyAuthRuleName \` per concedere la gestione dei diritti per l'hub dell'evento \` MyEventHubName \` , ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="9d83b-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="9d83b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d83b-113">PARAMETERS</span></span>

### <span data-ttu-id="9d83b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d83b-114">-DefaultProfile</span></span>
<span data-ttu-id="9d83b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d83b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d83b-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="9d83b-116">-EventHub</span></span>
<span data-ttu-id="9d83b-117">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="9d83b-117">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d83b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d83b-118">-InputObject</span></span>
<span data-ttu-id="9d83b-119">Oggetto AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9d83b-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d83b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d83b-120">-Name</span></span>
<span data-ttu-id="9d83b-121">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9d83b-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="9d83b-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d83b-122">-Namespace</span></span>
<span data-ttu-id="9d83b-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d83b-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d83b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d83b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9d83b-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9d83b-125">Resource Group Name</span></span>

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

### <span data-ttu-id="9d83b-126">-Diritti</span><span class="sxs-lookup"><span data-stu-id="9d83b-126">-Rights</span></span>
<span data-ttu-id="9d83b-127">Diritti, ad esempio @ ("ascolta", "Invia", "Gestisci")</span><span class="sxs-lookup"><span data-stu-id="9d83b-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d83b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d83b-128">-Confirm</span></span>
<span data-ttu-id="9d83b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d83b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d83b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d83b-130">-WhatIf</span></span>
<span data-ttu-id="9d83b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d83b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d83b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d83b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d83b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d83b-133">CommonParameters</span></span>
<span data-ttu-id="9d83b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d83b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d83b-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d83b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d83b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d83b-136">INPUTS</span></span>

### <span data-ttu-id="9d83b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9d83b-137">System.String</span></span>

### <span data-ttu-id="9d83b-138">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9d83b-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="9d83b-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="9d83b-139">System.String[]</span></span>

## <span data-ttu-id="9d83b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d83b-140">OUTPUTS</span></span>

### <span data-ttu-id="9d83b-141">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9d83b-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9d83b-142">Note</span><span class="sxs-lookup"><span data-stu-id="9d83b-142">NOTES</span></span>

## <span data-ttu-id="9d83b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d83b-143">RELATED LINKS</span></span>
