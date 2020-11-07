---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686299"
---
# <span data-ttu-id="368c3-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="368c3-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="368c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="368c3-102">SYNOPSIS</span></span>
<span data-ttu-id="368c3-103">Rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="368c3-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="368c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="368c3-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="368c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="368c3-105">DESCRIPTION</span></span>
<span data-ttu-id="368c3-106">Il cmdlet **Remove-AzureRmServiceBusNamespace** rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="368c3-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="368c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="368c3-107">EXAMPLES</span></span>

### <span data-ttu-id="368c3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="368c3-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="368c3-109">Rimuove lo spazio dei nomi Service Bus `SB-Example1` dal gruppo di risorse specificato `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="368c3-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="368c3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="368c3-110">PARAMETERS</span></span>

### <span data-ttu-id="368c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="368c3-111">-DefaultProfile</span></span>
<span data-ttu-id="368c3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="368c3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="368c3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="368c3-113">-Name</span></span>
<span data-ttu-id="368c3-114">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="368c3-114">Namespace Name.</span></span>

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

### <span data-ttu-id="368c3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="368c3-115">-ResourceGroupName</span></span>
<span data-ttu-id="368c3-116">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="368c3-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="368c3-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="368c3-117">-Confirm</span></span>
<span data-ttu-id="368c3-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="368c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="368c3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="368c3-119">-WhatIf</span></span>
<span data-ttu-id="368c3-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="368c3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="368c3-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="368c3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="368c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="368c3-122">CommonParameters</span></span>
<span data-ttu-id="368c3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="368c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="368c3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="368c3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="368c3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="368c3-125">INPUTS</span></span>

### <span data-ttu-id="368c3-126">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="368c3-126">-ResourceGroup</span></span>
 <span data-ttu-id="368c3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="368c3-127">System.String</span></span>

### <span data-ttu-id="368c3-128">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="368c3-128">-NamespaceName</span></span>
 <span data-ttu-id="368c3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="368c3-129">System.String</span></span>

## <span data-ttu-id="368c3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="368c3-130">OUTPUTS</span></span>

### <span data-ttu-id="368c3-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="368c3-131">System.Object</span></span>

## <span data-ttu-id="368c3-132">Note</span><span class="sxs-lookup"><span data-stu-id="368c3-132">NOTES</span></span>

## <span data-ttu-id="368c3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="368c3-133">RELATED LINKS</span></span>

