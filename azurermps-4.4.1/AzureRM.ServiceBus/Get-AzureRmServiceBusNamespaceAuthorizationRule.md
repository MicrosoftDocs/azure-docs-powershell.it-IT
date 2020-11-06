---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516015"
---
# <span data-ttu-id="4ac4e-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4ac4e-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="4ac4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ac4e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac4e-103">Ottiene una descrizione della regola di autorizzazione specificata per uno spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="4ac4e-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ac4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ac4e-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ac4e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ac4e-105">DESCRIPTION</span></span>
<span data-ttu-id="4ac4e-106">Il cmdlet **Get-AzureRmServiceBusNamespaceAuthorizationRule** ottiene la descrizione della regola di autorizzazione specificata nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="4ac4e-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="4ac4e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ac4e-107">EXAMPLES</span></span>

### <span data-ttu-id="4ac4e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ac4e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="4ac4e-109">Restituisce la descrizione della regola di autorizzazione specificata per uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="4ac4e-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="4ac4e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ac4e-110">PARAMETERS</span></span>

### <span data-ttu-id="4ac4e-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4ac4e-111">-ResourceGroup</span></span>
<span data-ttu-id="4ac4e-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ac4e-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ac4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac4e-113">-DefaultProfile</span></span>
<span data-ttu-id="4ac4e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ac4e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ac4e-115">-Name</span></span>
<span data-ttu-id="4ac4e-116">Nome AuthorizationRule dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="4ac4e-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac4e-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4ac4e-117">-Namespace</span></span>
<span data-ttu-id="4ac4e-118">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="4ac4e-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="4ac4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac4e-119">CommonParameters</span></span>
<span data-ttu-id="4ac4e-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac4e-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac4e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac4e-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ac4e-122">INPUTS</span></span>

### <span data-ttu-id="4ac4e-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4ac4e-123">-ResourceGroup</span></span>
 <span data-ttu-id="4ac4e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4ac4e-124">System.String</span></span>
 

### <span data-ttu-id="4ac4e-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4ac4e-125">-NamespaceName</span></span>
 <span data-ttu-id="4ac4e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4ac4e-126">System.String</span></span>
 

### <span data-ttu-id="4ac4e-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="4ac4e-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="4ac4e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4ac4e-128">System.String</span></span>

## <span data-ttu-id="4ac4e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ac4e-129">OUTPUTS</span></span>

### <span data-ttu-id="4ac4e-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4ac4e-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="4ac4e-131">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 tipo: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 location: Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="4ac4e-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="4ac4e-132">Note</span><span class="sxs-lookup"><span data-stu-id="4ac4e-132">NOTES</span></span>

## <span data-ttu-id="4ac4e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ac4e-133">RELATED LINKS</span></span>

