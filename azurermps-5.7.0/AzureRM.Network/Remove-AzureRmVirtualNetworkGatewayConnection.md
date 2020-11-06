---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 73bb12aebbe4f67c1aba4526f6ed656e5b6feb09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520696"
---
# <span data-ttu-id="77ef7-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77ef7-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="77ef7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="77ef7-103">Elimina una connessione di gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="77ef7-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77ef7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77ef7-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77ef7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77ef7-105">DESCRIPTION</span></span>
<span data-ttu-id="77ef7-106">La connessione Virtual Network Gateway è l'oggetto che rappresenta il tunnel IPsec (da sito a sito o da VNET a VNET) connesso al gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="77ef7-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="77ef7-107">Il cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** Elimina l'oggetto della connessione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="77ef7-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="77ef7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77ef7-108">EXAMPLES</span></span>

### <span data-ttu-id="77ef7-109">1: eliminare una connessione di gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="77ef7-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="77ef7-110">Elimina l'oggetto della connessione del gateway di rete virtuale con il nome "tunnel" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="77ef7-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="77ef7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77ef7-111">PARAMETERS</span></span>

### <span data-ttu-id="77ef7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ef7-112">-DefaultProfile</span></span>
<span data-ttu-id="77ef7-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77ef7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77ef7-114">-Force</span><span class="sxs-lookup"><span data-stu-id="77ef7-114">-Force</span></span>
<span data-ttu-id="77ef7-115">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77ef7-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77ef7-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="77ef7-116">-Name</span></span>
<span data-ttu-id="77ef7-117">Specifica il nome della connessione del gateway di rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77ef7-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="77ef7-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77ef7-118">-PassThru</span></span>
<span data-ttu-id="77ef7-119">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="77ef7-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="77ef7-120">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="77ef7-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77ef7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ef7-121">-ResourceGroupName</span></span>
<span data-ttu-id="77ef7-122">Specifica il nome del gruppo di risorse che contiene la connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="77ef7-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="77ef7-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77ef7-123">-Confirm</span></span>
<span data-ttu-id="77ef7-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77ef7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77ef7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77ef7-125">-WhatIf</span></span>
<span data-ttu-id="77ef7-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77ef7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77ef7-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77ef7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77ef7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ef7-128">CommonParameters</span></span>
<span data-ttu-id="77ef7-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77ef7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ef7-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77ef7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ef7-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77ef7-131">INPUTS</span></span>

### <span data-ttu-id="77ef7-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="77ef7-132">None</span></span>
<span data-ttu-id="77ef7-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="77ef7-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77ef7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77ef7-134">OUTPUTS</span></span>

## <span data-ttu-id="77ef7-135">Note</span><span class="sxs-lookup"><span data-stu-id="77ef7-135">NOTES</span></span>

## <span data-ttu-id="77ef7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77ef7-136">RELATED LINKS</span></span>

[<span data-ttu-id="77ef7-137">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77ef7-137">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="77ef7-138">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77ef7-138">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="77ef7-139">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="77ef7-139">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)


