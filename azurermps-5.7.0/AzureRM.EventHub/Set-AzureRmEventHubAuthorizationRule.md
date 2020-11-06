---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4965fb6047ca31d2c5b70276a777235d2a3cb050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515727"
---
# <span data-ttu-id="f3897-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f3897-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="f3897-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3897-102">SYNOPSIS</span></span>
<span data-ttu-id="f3897-103">Aggiorna la regola di autorizzazione specificata in un hub eventi.</span><span class="sxs-lookup"><span data-stu-id="f3897-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3897-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3897-104">SYNTAX</span></span>

### <span data-ttu-id="f3897-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3897-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3897-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3897-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3897-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f3897-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3897-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3897-108">DESCRIPTION</span></span>
<span data-ttu-id="f3897-109">Il cmdlet Set-AzureRmEventHubAuthorizationRule aggiorna la regola di autorizzazione specificata nell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="f3897-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="f3897-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3897-110">EXAMPLES</span></span>

### <span data-ttu-id="f3897-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3897-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="f3897-112">Aggiorna la regola di autorizzazione \` MyAuthRuleName \` per concedere la gestione dei diritti per l'hub dell'evento \` MyEventHubName \` , ambito dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="f3897-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="f3897-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3897-113">PARAMETERS</span></span>

### <span data-ttu-id="f3897-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3897-114">-DefaultProfile</span></span>
<span data-ttu-id="f3897-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3897-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3897-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f3897-116">-EventHub</span></span>
<span data-ttu-id="f3897-117">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="f3897-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3897-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3897-118">-InputObject</span></span>
<span data-ttu-id="f3897-119">Oggetto AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f3897-119">AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3897-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3897-120">-Name</span></span>
<span data-ttu-id="f3897-121">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f3897-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f3897-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3897-122">-Namespace</span></span>
<span data-ttu-id="f3897-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3897-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3897-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3897-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3897-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f3897-125">Resource Group Name</span></span>

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

### <span data-ttu-id="f3897-126">-Diritti</span><span class="sxs-lookup"><span data-stu-id="f3897-126">-Rights</span></span>
<span data-ttu-id="f3897-127">Diritti, ad esempio @ ("ascolta", "Invia", "Gestisci")</span><span class="sxs-lookup"><span data-stu-id="f3897-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3897-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f3897-128">-Confirm</span></span>
<span data-ttu-id="f3897-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3897-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3897-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3897-130">-WhatIf</span></span>
<span data-ttu-id="f3897-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3897-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3897-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3897-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3897-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3897-133">CommonParameters</span></span>
<span data-ttu-id="f3897-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3897-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f3897-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3897-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3897-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3897-136">INPUTS</span></span>

### <span data-ttu-id="f3897-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f3897-137">System.String</span></span>
<span data-ttu-id="f3897-138">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="f3897-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="f3897-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3897-139">OUTPUTS</span></span>

### <span data-ttu-id="f3897-140">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f3897-140">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="f3897-141">Note</span><span class="sxs-lookup"><span data-stu-id="f3897-141">NOTES</span></span>

## <span data-ttu-id="f3897-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3897-142">RELATED LINKS</span></span>
