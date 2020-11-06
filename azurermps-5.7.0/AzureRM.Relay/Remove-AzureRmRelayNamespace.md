---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: 52abd413f94d0c190a6f03b3707efdb544a4b72a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512383"
---
# <span data-ttu-id="4e526-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="4e526-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="4e526-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e526-102">SYNOPSIS</span></span>
<span data-ttu-id="4e526-103">Rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4e526-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e526-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e526-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e526-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e526-105">DESCRIPTION</span></span>
<span data-ttu-id="4e526-106">Il cmdlet **Remove-AzureRmRelayNamespace** rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4e526-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="4e526-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e526-107">EXAMPLES</span></span>

### <span data-ttu-id="4e526-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e526-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="4e526-109">Rimuove lo spazio dei nomi Relay `TestNameSpace-Relay1` dal gruppo di risorse specificato `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="4e526-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="4e526-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e526-110">PARAMETERS</span></span>

### <span data-ttu-id="4e526-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e526-111">-DefaultProfile</span></span>
<span data-ttu-id="4e526-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e526-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e526-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e526-113">-Name</span></span>
<span data-ttu-id="4e526-114">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="4e526-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="4e526-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e526-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e526-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e526-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="4e526-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e526-117">-Confirm</span></span>
<span data-ttu-id="4e526-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e526-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e526-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e526-119">-WhatIf</span></span>
<span data-ttu-id="4e526-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e526-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e526-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e526-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e526-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e526-122">CommonParameters</span></span>
<span data-ttu-id="4e526-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e526-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e526-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e526-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e526-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e526-125">INPUTS</span></span>

### <span data-ttu-id="4e526-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e526-126">-ResourceGroupName</span></span>
 <span data-ttu-id="4e526-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4e526-127">System.String</span></span>

### <span data-ttu-id="4e526-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e526-128">-Name</span></span>
 <span data-ttu-id="4e526-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4e526-129">System.String</span></span>

## <span data-ttu-id="4e526-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e526-130">OUTPUTS</span></span>

### <span data-ttu-id="4e526-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="4e526-131">System.Object</span></span>

## <span data-ttu-id="4e526-132">Note</span><span class="sxs-lookup"><span data-stu-id="4e526-132">NOTES</span></span>

## <span data-ttu-id="4e526-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e526-133">RELATED LINKS</span></span>

