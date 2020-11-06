---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 1a96916d0e3bed080e078226a14304b6ee6cecc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521666"
---
# <span data-ttu-id="f0211-101">New-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="f0211-101">New-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="f0211-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0211-102">SYNOPSIS</span></span>
<span data-ttu-id="f0211-103">Crea una nuova chiave primaria o secondaria per la regola di autorizzazione nello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="f0211-103">Creates a new primary or secondary key for the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0211-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0211-104">SYNTAX</span></span>

```
New-AzureRmEventHubNamespaceKey [-ResourceGroup] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f0211-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0211-105">DESCRIPTION</span></span>
<span data-ttu-id="f0211-106">Il cmdlet New-AzureRmEventHubNamespaceKey rigenera la chiave primaria o secondaria per la regola di autorizzazione specificata nello spazio dei nomi Hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="f0211-106">The New-AzureRmEventHubNamespaceKey cmdlet regenerates the primary or secondary key for the for the given authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="f0211-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0211-107">EXAMPLES</span></span>

### <span data-ttu-id="f0211-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0211-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNameSpaceKey -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName  -AuthorizationRuleName MyAuthRuleName -RegenerateKeys PrimaryKey
```

<span data-ttu-id="f0211-109">Rigenera la chiave primaria per la regola di autorizzazione \` MyAuthRuleName \` nello spazio dei nomi Hub eventi mynamespacename \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f0211-109">Regenerates the primary key for the authorization rule \`MyAuthRuleName\` in the Event Hubs namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f0211-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0211-110">PARAMETERS</span></span>

### <span data-ttu-id="f0211-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f0211-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="f0211-112">Nome della regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="f0211-112">Authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0211-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f0211-113">-NamespaceName</span></span>
<span data-ttu-id="f0211-114">Nome dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="f0211-114">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0211-115">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="f0211-115">-RegenerateKeys</span></span>
<span data-ttu-id="f0211-116">Chiave per la rigenerazione: \` PrimaryKey \` o \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="f0211-116">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0211-117">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0211-117">-ResourceGroup</span></span>
<span data-ttu-id="f0211-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f0211-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0211-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0211-119">-Confirm</span></span>
<span data-ttu-id="f0211-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0211-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0211-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0211-121">-WhatIf</span></span>
<span data-ttu-id="f0211-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0211-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0211-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0211-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="f0211-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0211-124">INPUTS</span></span>

### <span data-ttu-id="f0211-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f0211-125">System.String</span></span>

## <span data-ttu-id="f0211-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0211-126">OUTPUTS</span></span>

### <span data-ttu-id="f0211-127">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="f0211-127">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="f0211-128">Note</span><span class="sxs-lookup"><span data-stu-id="f0211-128">NOTES</span></span>

## <span data-ttu-id="f0211-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0211-129">RELATED LINKS</span></span>

