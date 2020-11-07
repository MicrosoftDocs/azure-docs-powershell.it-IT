---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3bc816f690f39b534a134e80df1a86c7bbca5dc1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862894"
---
# <span data-ttu-id="a49a6-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a49a6-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="a49a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a49a6-102">SYNOPSIS</span></span>

## <span data-ttu-id="a49a6-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a49a6-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a49a6-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a49a6-104">DESCRIPTION</span></span>

## <span data-ttu-id="a49a6-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a49a6-105">EXAMPLES</span></span>

### <span data-ttu-id="a49a6-106">Esempio 1: rimuovere un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a49a6-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="a49a6-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a49a6-107">PARAMETERS</span></span>

### <span data-ttu-id="a49a6-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a49a6-108">-AsJob</span></span>
<span data-ttu-id="a49a6-109">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a49a6-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a49a6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a49a6-110">-DefaultProfile</span></span>
<span data-ttu-id="a49a6-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a49a6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a49a6-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a49a6-112">-Force</span></span>
<span data-ttu-id="a49a6-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a49a6-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a49a6-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a49a6-114">-Name</span></span>
<span data-ttu-id="a49a6-115">Nome peer di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a49a6-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="a49a6-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a49a6-116">-PassThru</span></span>
<span data-ttu-id="a49a6-117">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a49a6-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a49a6-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a49a6-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a49a6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a49a6-119">-ResourceGroupName</span></span>
<span data-ttu-id="a49a6-120">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a49a6-120">The resource group name</span></span>

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

### <span data-ttu-id="a49a6-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a49a6-121">-VirtualNetworkName</span></span>
<span data-ttu-id="a49a6-122">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a49a6-122">The virtual network name.</span></span>

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

### <span data-ttu-id="a49a6-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a49a6-123">-Confirm</span></span>
<span data-ttu-id="a49a6-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a49a6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a49a6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a49a6-125">-WhatIf</span></span>
<span data-ttu-id="a49a6-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a49a6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a49a6-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a49a6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a49a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a49a6-128">CommonParameters</span></span>
<span data-ttu-id="a49a6-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a49a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a49a6-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a49a6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a49a6-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a49a6-131">INPUTS</span></span>

## <span data-ttu-id="a49a6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a49a6-132">OUTPUTS</span></span>

## <span data-ttu-id="a49a6-133">Note</span><span class="sxs-lookup"><span data-stu-id="a49a6-133">NOTES</span></span>

## <span data-ttu-id="a49a6-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a49a6-134">RELATED LINKS</span></span>

