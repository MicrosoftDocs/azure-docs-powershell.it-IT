---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ddc269ecd6f5cb4d1a1d377f656d47b0d18c6c00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508540"
---
# <span data-ttu-id="a0055-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a0055-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="a0055-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0055-102">SYNOPSIS</span></span>
<span data-ttu-id="a0055-103">Elimina un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="a0055-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0055-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0055-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0055-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0055-105">DESCRIPTION</span></span>
<span data-ttu-id="a0055-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="a0055-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="a0055-107">Il cmdlet **Remove-AzureRmLocalNetworkGateway** Elimina l'oggetto che rappresenta il Gateway on-Prem in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a0055-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="a0055-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0055-108">EXAMPLES</span></span>

### <span data-ttu-id="a0055-109">1: eliminare un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="a0055-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="a0055-110">Elimina l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="a0055-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="a0055-111">Nota: prima di tutto, è necessario eliminare tutte le connessioni al gateway di rete locale usando il cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="a0055-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="a0055-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0055-112">PARAMETERS</span></span>

### <span data-ttu-id="a0055-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a0055-113">-Force</span></span>
<span data-ttu-id="a0055-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a0055-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0055-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0055-115">-Name</span></span>
<span data-ttu-id="a0055-116">Specifica il nome del gateway di rete locale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0055-116">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a0055-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0055-117">-PassThru</span></span>
<span data-ttu-id="a0055-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a0055-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a0055-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a0055-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0055-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0055-120">-ResourceGroupName</span></span>
<span data-ttu-id="a0055-121">Specifica il nome del gruppo di risorse che contiene il gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="a0055-121">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="a0055-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0055-122">-Confirm</span></span>
<span data-ttu-id="a0055-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0055-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0055-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0055-124">-WhatIf</span></span>
<span data-ttu-id="a0055-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0055-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0055-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0055-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0055-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0055-127">-DefaultProfile</span></span>
<span data-ttu-id="a0055-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0055-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0055-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0055-129">CommonParameters</span></span>
<span data-ttu-id="a0055-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0055-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0055-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0055-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0055-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0055-132">INPUTS</span></span>

## <span data-ttu-id="a0055-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0055-133">OUTPUTS</span></span>

## <span data-ttu-id="a0055-134">Note</span><span class="sxs-lookup"><span data-stu-id="a0055-134">NOTES</span></span>

## <span data-ttu-id="a0055-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0055-135">RELATED LINKS</span></span>

[<span data-ttu-id="a0055-136">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a0055-136">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="a0055-137">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a0055-137">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="a0055-138">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a0055-138">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


