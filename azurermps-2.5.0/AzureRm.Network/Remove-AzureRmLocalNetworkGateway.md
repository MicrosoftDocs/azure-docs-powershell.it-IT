---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 7b3fde5feb5dae1ca064b8f5e31bbdfe03e12c7a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866855"
---
# <span data-ttu-id="1b6fc-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fc-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="1b6fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6fc-103">Elimina un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="1b6fc-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b6fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b6fc-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b6fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b6fc-105">DESCRIPTION</span></span>
<span data-ttu-id="1b6fc-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="1b6fc-107">Il cmdlet **Remove-AzureRmLocalNetworkGateway** Elimina l'oggetto che rappresenta il Gateway on-Prem in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="1b6fc-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b6fc-108">EXAMPLES</span></span>

### <span data-ttu-id="1b6fc-109">1: eliminare un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="1b6fc-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="1b6fc-110">Elimina l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="1b6fc-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="1b6fc-111">Nota: prima di tutto, è necessario eliminare tutte le connessioni al gateway di rete locale usando il cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="1b6fc-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="1b6fc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b6fc-112">PARAMETERS</span></span>

### <span data-ttu-id="1b6fc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b6fc-113">-AsJob</span></span>
<span data-ttu-id="1b6fc-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1b6fc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b6fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6fc-115">-DefaultProfile</span></span>
<span data-ttu-id="1b6fc-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b6fc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1b6fc-117">-Force</span></span>
<span data-ttu-id="1b6fc-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1b6fc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b6fc-119">-Name</span></span>
<span data-ttu-id="1b6fc-120">Specifica il nome del gateway di rete locale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1b6fc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b6fc-121">-PassThru</span></span>
<span data-ttu-id="1b6fc-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1b6fc-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1b6fc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b6fc-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b6fc-125">Specifica il nome del gruppo di risorse che contiene il gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="1b6fc-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b6fc-126">-Confirm</span></span>
<span data-ttu-id="1b6fc-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b6fc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b6fc-128">-WhatIf</span></span>
<span data-ttu-id="1b6fc-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b6fc-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b6fc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6fc-131">CommonParameters</span></span>
<span data-ttu-id="1b6fc-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6fc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6fc-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6fc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6fc-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b6fc-134">INPUTS</span></span>

## <span data-ttu-id="1b6fc-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b6fc-135">OUTPUTS</span></span>

## <span data-ttu-id="1b6fc-136">Note</span><span class="sxs-lookup"><span data-stu-id="1b6fc-136">NOTES</span></span>

## <span data-ttu-id="1b6fc-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b6fc-137">RELATED LINKS</span></span>

[<span data-ttu-id="1b6fc-138">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fc-138">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="1b6fc-139">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fc-139">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="1b6fc-140">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1b6fc-140">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


