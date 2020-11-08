---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 78ba1323532faa825e80e456f5ae6544eef3c7de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021924"
---
# <span data-ttu-id="43862-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="43862-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="43862-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43862-102">SYNOPSIS</span></span>
<span data-ttu-id="43862-103">Elimina una connessione di gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="43862-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="43862-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43862-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43862-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43862-105">DESCRIPTION</span></span>
<span data-ttu-id="43862-106">La connessione Virtual Network Gateway è l'oggetto che rappresenta il tunnel IPsec (da sito a sito o da VNET a VNET) connesso al gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="43862-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="43862-107">Il cmdlet **Remove-AzVirtualNetworkGatewayConnection** Elimina l'oggetto della connessione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43862-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="43862-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43862-108">EXAMPLES</span></span>

### <span data-ttu-id="43862-109">1: eliminare una connessione di gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="43862-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="43862-110">Elimina l'oggetto della connessione del gateway di rete virtuale con il nome "tunnel" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="43862-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="43862-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43862-111">PARAMETERS</span></span>

### <span data-ttu-id="43862-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43862-112">-DefaultProfile</span></span>
<span data-ttu-id="43862-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43862-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43862-114">-Force</span><span class="sxs-lookup"><span data-stu-id="43862-114">-Force</span></span>
<span data-ttu-id="43862-115">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="43862-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43862-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="43862-116">-Name</span></span>
<span data-ttu-id="43862-117">Specifica il nome della connessione del gateway di rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43862-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="43862-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43862-118">-PassThru</span></span>
<span data-ttu-id="43862-119">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="43862-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43862-120">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="43862-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43862-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43862-121">-ResourceGroupName</span></span>
<span data-ttu-id="43862-122">Specifica il nome del gruppo di risorse che contiene la connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="43862-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="43862-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43862-123">-Confirm</span></span>
<span data-ttu-id="43862-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43862-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43862-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43862-125">-WhatIf</span></span>
<span data-ttu-id="43862-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43862-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43862-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43862-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43862-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43862-128">CommonParameters</span></span>
<span data-ttu-id="43862-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43862-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43862-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43862-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43862-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43862-131">INPUTS</span></span>

### <span data-ttu-id="43862-132">System. String</span><span class="sxs-lookup"><span data-stu-id="43862-132">System.String</span></span>

## <span data-ttu-id="43862-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43862-133">OUTPUTS</span></span>

### <span data-ttu-id="43862-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43862-134">System.Boolean</span></span>

## <span data-ttu-id="43862-135">Note</span><span class="sxs-lookup"><span data-stu-id="43862-135">NOTES</span></span>

## <span data-ttu-id="43862-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43862-136">RELATED LINKS</span></span>

[<span data-ttu-id="43862-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="43862-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="43862-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="43862-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="43862-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="43862-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
