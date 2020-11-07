---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 2b1e781a65eaa6a43c4f8571caf1850f0b04d6cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688516"
---
# <span data-ttu-id="a425f-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a425f-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="a425f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a425f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a425f-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a425f-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a425f-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a425f-104">DESCRIPTION</span></span>

## <span data-ttu-id="a425f-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a425f-105">EXAMPLES</span></span>

### <span data-ttu-id="a425f-106">Esempio 1: rimuovere un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a425f-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="a425f-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a425f-107">PARAMETERS</span></span>

### <span data-ttu-id="a425f-108">-Force</span><span class="sxs-lookup"><span data-stu-id="a425f-108">-Force</span></span>
<span data-ttu-id="a425f-109">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a425f-109">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a425f-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="a425f-110">-Name</span></span>
<span data-ttu-id="a425f-111">Nome peer di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a425f-111">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a425f-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a425f-112">-PassThru</span></span>
<span data-ttu-id="a425f-113">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a425f-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a425f-114">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a425f-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a425f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a425f-115">-ResourceGroupName</span></span>
<span data-ttu-id="a425f-116">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a425f-116">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a425f-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a425f-117">-VirtualNetworkName</span></span>
<span data-ttu-id="a425f-118">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a425f-118">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a425f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a425f-119">-Confirm</span></span>
<span data-ttu-id="a425f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a425f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a425f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a425f-121">-WhatIf</span></span>
<span data-ttu-id="a425f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a425f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a425f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a425f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a425f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a425f-124">-DefaultProfile</span></span>
<span data-ttu-id="a425f-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a425f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a425f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a425f-126">CommonParameters</span></span>
<span data-ttu-id="a425f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a425f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a425f-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a425f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a425f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a425f-129">INPUTS</span></span>

## <span data-ttu-id="a425f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a425f-130">OUTPUTS</span></span>

## <span data-ttu-id="a425f-131">Note</span><span class="sxs-lookup"><span data-stu-id="a425f-131">NOTES</span></span>

## <span data-ttu-id="a425f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a425f-132">RELATED LINKS</span></span>

