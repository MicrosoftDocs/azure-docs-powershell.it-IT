---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 65e4259b7b530c7ea003860ab30c9f0c0baa7250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520909"
---
# <span data-ttu-id="63290-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="63290-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="63290-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63290-102">SYNOPSIS</span></span>
<span data-ttu-id="63290-103">Elimina un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="63290-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63290-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63290-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63290-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63290-105">DESCRIPTION</span></span>
<span data-ttu-id="63290-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="63290-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="63290-107">Il cmdlet **Get-AzureRmVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63290-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="63290-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63290-108">EXAMPLES</span></span>

### <span data-ttu-id="63290-109">1: eliminare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="63290-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="63290-110">Elimina l'oggetto del gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG" Nota: per prima cosa è necessario eliminare tutte le connessioni al gateway di rete virtuale usando il cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="63290-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="63290-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63290-111">PARAMETERS</span></span>

### <span data-ttu-id="63290-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63290-112">-AsJob</span></span>
<span data-ttu-id="63290-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="63290-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63290-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63290-114">-DefaultProfile</span></span>
<span data-ttu-id="63290-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63290-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63290-116">-Force</span><span class="sxs-lookup"><span data-stu-id="63290-116">-Force</span></span>
<span data-ttu-id="63290-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="63290-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63290-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="63290-118">-Name</span></span>
<span data-ttu-id="63290-119">Specifica il nome del gateway di rete virtuale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63290-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63290-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63290-120">-PassThru</span></span>
<span data-ttu-id="63290-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="63290-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="63290-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="63290-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="63290-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63290-123">-ResourceGroupName</span></span>
<span data-ttu-id="63290-124">Specifica il nome del gruppo di risorse che contiene il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="63290-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="63290-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63290-125">-Confirm</span></span>
<span data-ttu-id="63290-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63290-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63290-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63290-127">-WhatIf</span></span>
<span data-ttu-id="63290-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63290-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63290-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63290-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63290-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63290-130">CommonParameters</span></span>
<span data-ttu-id="63290-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63290-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63290-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63290-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63290-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63290-133">INPUTS</span></span>

### <span data-ttu-id="63290-134">System. String</span><span class="sxs-lookup"><span data-stu-id="63290-134">System.String</span></span>

## <span data-ttu-id="63290-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63290-135">OUTPUTS</span></span>

### <span data-ttu-id="63290-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63290-136">System.Boolean</span></span>

## <span data-ttu-id="63290-137">Note</span><span class="sxs-lookup"><span data-stu-id="63290-137">NOTES</span></span>

## <span data-ttu-id="63290-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63290-138">RELATED LINKS</span></span>
