---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 8c3741f7e1a3e25dfbc3a3b6f7fb655e5db19fe8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188424"
---
# <span data-ttu-id="3ebbe-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ebbe-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="3ebbe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ebbe-102">SYNOPSIS</span></span>
<span data-ttu-id="3ebbe-103">Elimina un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="3ebbe-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="3ebbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ebbe-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ebbe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ebbe-105">DESCRIPTION</span></span>
<span data-ttu-id="3ebbe-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="3ebbe-107">Il cmdlet **Remove-AzLocalNetworkGateway** Elimina l'oggetto che rappresenta il Gateway on-Prem in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="3ebbe-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ebbe-108">EXAMPLES</span></span>

### <span data-ttu-id="3ebbe-109">Esempio 1: eliminare un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="3ebbe-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="3ebbe-110">Elimina l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG" Nota: per prima cosa è necessario eliminare tutte le connessioni al gateway di rete locale usando il cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="3ebbe-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="3ebbe-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ebbe-111">PARAMETERS</span></span>

### <span data-ttu-id="3ebbe-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ebbe-112">-AsJob</span></span>
<span data-ttu-id="3ebbe-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3ebbe-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ebbe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ebbe-114">-DefaultProfile</span></span>
<span data-ttu-id="3ebbe-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ebbe-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3ebbe-116">-Force</span></span>
<span data-ttu-id="3ebbe-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ebbe-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ebbe-118">-Name</span></span>
<span data-ttu-id="3ebbe-119">Specifica il nome del gateway di rete locale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3ebbe-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ebbe-120">-PassThru</span></span>
<span data-ttu-id="3ebbe-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3ebbe-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3ebbe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ebbe-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ebbe-124">Specifica il nome del gruppo di risorse che contiene il gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="3ebbe-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ebbe-125">-Confirm</span></span>
<span data-ttu-id="3ebbe-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ebbe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ebbe-127">-WhatIf</span></span>
<span data-ttu-id="3ebbe-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ebbe-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ebbe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ebbe-130">CommonParameters</span></span>
<span data-ttu-id="3ebbe-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ebbe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ebbe-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ebbe-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ebbe-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ebbe-133">INPUTS</span></span>

### <span data-ttu-id="3ebbe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3ebbe-134">System.String</span></span>

## <span data-ttu-id="3ebbe-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ebbe-135">OUTPUTS</span></span>

### <span data-ttu-id="3ebbe-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ebbe-136">System.Boolean</span></span>

## <span data-ttu-id="3ebbe-137">Note</span><span class="sxs-lookup"><span data-stu-id="3ebbe-137">NOTES</span></span>

## <span data-ttu-id="3ebbe-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ebbe-138">RELATED LINKS</span></span>

[<span data-ttu-id="3ebbe-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ebbe-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="3ebbe-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ebbe-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="3ebbe-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3ebbe-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
