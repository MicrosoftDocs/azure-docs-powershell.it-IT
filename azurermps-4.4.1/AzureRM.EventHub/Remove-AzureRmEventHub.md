---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521664"
---
# <span data-ttu-id="5096c-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="5096c-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="5096c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5096c-102">SYNOPSIS</span></span>
<span data-ttu-id="5096c-103">Rimuove l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="5096c-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5096c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5096c-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5096c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5096c-105">DESCRIPTION</span></span>
<span data-ttu-id="5096c-106">Il cmdlet Remove-AzureRmEventHub rimuove ed Elimina il hub dell'evento specificato dallo spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="5096c-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="5096c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5096c-107">EXAMPLES</span></span>

### <span data-ttu-id="5096c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5096c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="5096c-109">Rimuove l'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="5096c-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="5096c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5096c-110">PARAMETERS</span></span>

### <span data-ttu-id="5096c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5096c-111">-ResourceGroupName</span></span>
<span data-ttu-id="5096c-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5096c-112">Resource group name.</span></span>

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

### <span data-ttu-id="5096c-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5096c-113">-Confirm</span></span>
<span data-ttu-id="5096c-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5096c-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5096c-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5096c-115">-WhatIf</span></span>
<span data-ttu-id="5096c-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5096c-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5096c-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5096c-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5096c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5096c-118">-Name</span></span>
<span data-ttu-id="5096c-119">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="5096c-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5096c-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5096c-120">-Namespace</span></span>
<span data-ttu-id="5096c-121">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5096c-121">Namespace Name.</span></span>

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

## <span data-ttu-id="5096c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5096c-122">INPUTS</span></span>

### <span data-ttu-id="5096c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5096c-123">System.String</span></span>

## <span data-ttu-id="5096c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5096c-124">OUTPUTS</span></span>

### <span data-ttu-id="5096c-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="5096c-125">System.Object</span></span>

## <span data-ttu-id="5096c-126">Note</span><span class="sxs-lookup"><span data-stu-id="5096c-126">NOTES</span></span>

## <span data-ttu-id="5096c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5096c-127">RELATED LINKS</span></span>

