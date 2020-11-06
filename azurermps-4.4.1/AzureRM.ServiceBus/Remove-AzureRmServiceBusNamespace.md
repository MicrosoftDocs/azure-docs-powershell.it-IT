---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512967"
---
# <span data-ttu-id="77d21-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="77d21-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="77d21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77d21-102">SYNOPSIS</span></span>
<span data-ttu-id="77d21-103">Rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="77d21-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77d21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77d21-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77d21-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77d21-105">DESCRIPTION</span></span>
<span data-ttu-id="77d21-106">Il cmdlet **Remove-AzureRmServiceBusNamespace** rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="77d21-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="77d21-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77d21-107">EXAMPLES</span></span>

### <span data-ttu-id="77d21-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77d21-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="77d21-109">Rimuove lo spazio dei nomi Service Bus `SB-Example1` dal gruppo di risorse specificato `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="77d21-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="77d21-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77d21-110">PARAMETERS</span></span>

### <span data-ttu-id="77d21-111">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="77d21-111">-NamespaceName</span></span>
<span data-ttu-id="77d21-112">Nome dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="77d21-112">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="77d21-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77d21-113">-ResourceGroup</span></span>
<span data-ttu-id="77d21-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="77d21-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="77d21-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77d21-115">-Confirm</span></span>
<span data-ttu-id="77d21-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77d21-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77d21-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77d21-117">-WhatIf</span></span>
<span data-ttu-id="77d21-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77d21-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77d21-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77d21-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77d21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d21-120">CommonParameters</span></span>
<span data-ttu-id="77d21-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d21-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d21-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d21-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77d21-123">INPUTS</span></span>

### <span data-ttu-id="77d21-124">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77d21-124">-ResourceGroup</span></span>
 <span data-ttu-id="77d21-125">System. String</span><span class="sxs-lookup"><span data-stu-id="77d21-125">System.String</span></span>

### <span data-ttu-id="77d21-126">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="77d21-126">-NamespaceName</span></span>
 <span data-ttu-id="77d21-127">System. String</span><span class="sxs-lookup"><span data-stu-id="77d21-127">System.String</span></span>

## <span data-ttu-id="77d21-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77d21-128">OUTPUTS</span></span>

### <span data-ttu-id="77d21-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="77d21-129">System.Object</span></span>

## <span data-ttu-id="77d21-130">Note</span><span class="sxs-lookup"><span data-stu-id="77d21-130">NOTES</span></span>

## <span data-ttu-id="77d21-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77d21-131">RELATED LINKS</span></span>

