---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 10c3d087bcde2a88fd33ff3118a40e44af918ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519185"
---
# <span data-ttu-id="e74d0-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e74d0-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="e74d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e74d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e74d0-103">Rimuove lo spazio dei nomi degli hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="e74d0-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e74d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e74d0-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e74d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e74d0-105">DESCRIPTION</span></span>
<span data-ttu-id="e74d0-106">Il cmdlet Remove-AzureRmEventHubNamespace rimuove ed Elimina lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="e74d0-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e74d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e74d0-107">EXAMPLES</span></span>

### <span data-ttu-id="e74d0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e74d0-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="e74d0-109">Rimuove lo spazio dei nomi degli hub di eventi MyNamespace \` \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e74d0-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e74d0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e74d0-110">PARAMETERS</span></span>

### <span data-ttu-id="e74d0-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e74d0-111">-ResourceGroupName</span></span>
<span data-ttu-id="e74d0-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e74d0-112">Resource group name.</span></span>

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

### <span data-ttu-id="e74d0-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e74d0-113">-Confirm</span></span>
<span data-ttu-id="e74d0-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e74d0-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e74d0-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e74d0-115">-WhatIf</span></span>
<span data-ttu-id="e74d0-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e74d0-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e74d0-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e74d0-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e74d0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e74d0-118">-Name</span></span>
<span data-ttu-id="e74d0-119">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="e74d0-119">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="e74d0-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e74d0-120">INPUTS</span></span>

### <span data-ttu-id="e74d0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e74d0-121">System.String</span></span>

## <span data-ttu-id="e74d0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e74d0-122">OUTPUTS</span></span>

### <span data-ttu-id="e74d0-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="e74d0-123">System.Object</span></span>

## <span data-ttu-id="e74d0-124">Note</span><span class="sxs-lookup"><span data-stu-id="e74d0-124">NOTES</span></span>

## <span data-ttu-id="e74d0-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e74d0-125">RELATED LINKS</span></span>

