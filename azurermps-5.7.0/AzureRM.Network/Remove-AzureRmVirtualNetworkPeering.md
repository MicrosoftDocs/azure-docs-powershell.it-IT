---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: a128f7c9e9440255ed01b32c4460ffd180655928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521423"
---
# <span data-ttu-id="d65ad-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d65ad-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="d65ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d65ad-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d65ad-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d65ad-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d65ad-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d65ad-104">DESCRIPTION</span></span>

## <span data-ttu-id="d65ad-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d65ad-105">EXAMPLES</span></span>

### <span data-ttu-id="d65ad-106">Esempio 1: rimuovere un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d65ad-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="d65ad-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d65ad-107">PARAMETERS</span></span>

### <span data-ttu-id="d65ad-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d65ad-108">-AsJob</span></span>
<span data-ttu-id="d65ad-109">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d65ad-109">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d65ad-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65ad-110">-DefaultProfile</span></span>
<span data-ttu-id="d65ad-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d65ad-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d65ad-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d65ad-112">-Force</span></span>
<span data-ttu-id="d65ad-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d65ad-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d65ad-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d65ad-114">-Name</span></span>
<span data-ttu-id="d65ad-115">Nome peer di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d65ad-115">The virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d65ad-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d65ad-116">-PassThru</span></span>
<span data-ttu-id="d65ad-117">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d65ad-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d65ad-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d65ad-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d65ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="d65ad-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d65ad-120">The resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d65ad-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d65ad-121">-VirtualNetworkName</span></span>
<span data-ttu-id="d65ad-122">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d65ad-122">The virtual network name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d65ad-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d65ad-123">-Confirm</span></span>
<span data-ttu-id="d65ad-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d65ad-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d65ad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d65ad-125">-WhatIf</span></span>
<span data-ttu-id="d65ad-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d65ad-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d65ad-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d65ad-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d65ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65ad-128">CommonParameters</span></span>
<span data-ttu-id="d65ad-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d65ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65ad-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d65ad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65ad-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d65ad-131">INPUTS</span></span>

### <span data-ttu-id="d65ad-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d65ad-132">None</span></span>
<span data-ttu-id="d65ad-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d65ad-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d65ad-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d65ad-134">OUTPUTS</span></span>

## <span data-ttu-id="d65ad-135">Note</span><span class="sxs-lookup"><span data-stu-id="d65ad-135">NOTES</span></span>

## <span data-ttu-id="d65ad-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d65ad-136">RELATED LINKS</span></span>

