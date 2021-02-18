---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 8c3741f7e1a3e25dfbc3a3b6f7fb655e5db19fe8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206611"
---
# <span data-ttu-id="cbcab-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbcab-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="cbcab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbcab-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcab-103">Elimina un Gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="cbcab-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="cbcab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbcab-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbcab-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cbcab-105">DESCRIPTION</span></span>
<span data-ttu-id="cbcab-106">Gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN locale.</span><span class="sxs-lookup"><span data-stu-id="cbcab-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="cbcab-107">Il cmdlet **Remove-AzLocalNetworkGateway** elimina l'oggetto che rappresenta il gateway locale in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cbcab-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="cbcab-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbcab-108">EXAMPLES</span></span>

### <span data-ttu-id="cbcab-109">Esempio 1: Eliminare un Gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="cbcab-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="cbcab-110">Elimina l'oggetto del Gateway di rete locale con il nome "myLocalGW" all'interno del gruppo di risorse "myRG" Nota: è necessario eliminare prima tutte le connessioni al Gateway di rete locale usando il cmdlet **Remove-AzVirtualNetworkGatewayConnection.**</span><span class="sxs-lookup"><span data-stu-id="cbcab-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="cbcab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbcab-111">PARAMETERS</span></span>

### <span data-ttu-id="cbcab-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbcab-112">-AsJob</span></span>
<span data-ttu-id="cbcab-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cbcab-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbcab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcab-114">-DefaultProfile</span></span>
<span data-ttu-id="cbcab-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbcab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbcab-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cbcab-116">-Force</span></span>
<span data-ttu-id="cbcab-117">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="cbcab-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cbcab-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cbcab-118">-Name</span></span>
<span data-ttu-id="cbcab-119">Specifica il nome del gateway di rete locale rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbcab-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cbcab-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbcab-120">-PassThru</span></span>
<span data-ttu-id="cbcab-121">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="cbcab-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cbcab-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cbcab-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cbcab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcab-123">-ResourceGroupName</span></span>
<span data-ttu-id="cbcab-124">Specifica il nome del gruppo di risorse che contiene il gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="cbcab-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="cbcab-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbcab-125">-Confirm</span></span>
<span data-ttu-id="cbcab-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbcab-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbcab-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbcab-127">-WhatIf</span></span>
<span data-ttu-id="cbcab-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cbcab-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbcab-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cbcab-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbcab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcab-130">CommonParameters</span></span>
<span data-ttu-id="cbcab-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbcab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcab-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbcab-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcab-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="cbcab-133">INPUTS</span></span>

### <span data-ttu-id="cbcab-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cbcab-134">System.String</span></span>

## <span data-ttu-id="cbcab-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbcab-135">OUTPUTS</span></span>

### <span data-ttu-id="cbcab-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbcab-136">System.Boolean</span></span>

## <span data-ttu-id="cbcab-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="cbcab-137">NOTES</span></span>

## <span data-ttu-id="cbcab-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbcab-138">RELATED LINKS</span></span>

[<span data-ttu-id="cbcab-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbcab-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="cbcab-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbcab-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="cbcab-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cbcab-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
