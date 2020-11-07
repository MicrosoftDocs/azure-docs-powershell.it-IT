---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: cec41bda56da33f22def6c44752effb3d705b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686108"
---
# <span data-ttu-id="07265-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="07265-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="07265-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07265-102">SYNOPSIS</span></span>
<span data-ttu-id="07265-103">Rimuove lo spazio dei nomi degli hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="07265-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07265-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07265-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07265-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07265-105">DESCRIPTION</span></span>
<span data-ttu-id="07265-106">Il cmdlet Remove-AzureRmEventHubNamespace rimuove ed Elimina lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="07265-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="07265-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07265-107">EXAMPLES</span></span>

### <span data-ttu-id="07265-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07265-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="07265-109">Rimuove lo spazio dei nomi degli hub di eventi MyNamespace \` \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="07265-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="07265-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07265-110">PARAMETERS</span></span>

### <span data-ttu-id="07265-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07265-111">-DefaultProfile</span></span>
<span data-ttu-id="07265-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07265-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07265-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="07265-113">-Name</span></span>
<span data-ttu-id="07265-114">Nome dello spazio dei nomi EventHub</span><span class="sxs-lookup"><span data-stu-id="07265-114">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="07265-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07265-115">-ResourceGroupName</span></span>
<span data-ttu-id="07265-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="07265-116">Resource Group Name</span></span>

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

### <span data-ttu-id="07265-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07265-117">-Confirm</span></span>
<span data-ttu-id="07265-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07265-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07265-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07265-119">-WhatIf</span></span>
<span data-ttu-id="07265-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07265-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07265-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07265-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07265-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07265-122">CommonParameters</span></span>
<span data-ttu-id="07265-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07265-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="07265-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07265-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07265-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07265-125">INPUTS</span></span>

### <span data-ttu-id="07265-126">System. String</span><span class="sxs-lookup"><span data-stu-id="07265-126">System.String</span></span>


## <span data-ttu-id="07265-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07265-127">OUTPUTS</span></span>

### <span data-ttu-id="07265-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="07265-128">System.Object</span></span>

## <span data-ttu-id="07265-129">Note</span><span class="sxs-lookup"><span data-stu-id="07265-129">NOTES</span></span>

## <span data-ttu-id="07265-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07265-130">RELATED LINKS</span></span>
