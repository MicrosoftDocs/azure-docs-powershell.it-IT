---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 958ddffb02aaa6c8ac81f413cca6453f7f87c3a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866661"
---
# <span data-ttu-id="6a3e6-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6a3e6-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="6a3e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3e6-103">Elimina un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="6a3e6-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a3e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a3e6-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a3e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a3e6-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3e6-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="6a3e6-107">Il cmdlet **Get-AzureRmVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="6a3e6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a3e6-108">EXAMPLES</span></span>

### <span data-ttu-id="6a3e6-109">1: eliminare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="6a3e6-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="6a3e6-110">Elimina l'oggetto del gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="6a3e6-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="6a3e6-111">Nota: prima di tutto, è necessario eliminare tutte le connessioni al gateway di rete virtuale usando il cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="6a3e6-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="6a3e6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a3e6-112">PARAMETERS</span></span>

### <span data-ttu-id="6a3e6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a3e6-113">-AsJob</span></span>
<span data-ttu-id="6a3e6-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6a3e6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a3e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3e6-115">-DefaultProfile</span></span>
<span data-ttu-id="6a3e6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a3e6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6a3e6-117">-Force</span></span>
<span data-ttu-id="6a3e6-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a3e6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a3e6-119">-Name</span></span>
<span data-ttu-id="6a3e6-120">Specifica il nome del gateway di rete virtuale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3e6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a3e6-121">-PassThru</span></span>
<span data-ttu-id="6a3e6-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a3e6-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a3e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a3e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a3e6-125">Specifica il nome del gruppo di risorse che contiene il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="6a3e6-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a3e6-126">-Confirm</span></span>
<span data-ttu-id="6a3e6-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a3e6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a3e6-128">-WhatIf</span></span>
<span data-ttu-id="6a3e6-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a3e6-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a3e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3e6-131">CommonParameters</span></span>
<span data-ttu-id="6a3e6-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3e6-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a3e6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3e6-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a3e6-134">INPUTS</span></span>

## <span data-ttu-id="6a3e6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a3e6-135">OUTPUTS</span></span>

## <span data-ttu-id="6a3e6-136">Note</span><span class="sxs-lookup"><span data-stu-id="6a3e6-136">NOTES</span></span>

## <span data-ttu-id="6a3e6-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a3e6-137">RELATED LINKS</span></span>

