---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 1aca9335da67bb3c1144f67fb8f14ad9b2a7f1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509804"
---
# <span data-ttu-id="06637-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06637-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="06637-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06637-102">SYNOPSIS</span></span>
<span data-ttu-id="06637-103">Elimina un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="06637-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06637-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06637-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06637-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06637-105">DESCRIPTION</span></span>
<span data-ttu-id="06637-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="06637-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="06637-107">Il cmdlet **Remove-AzureRmLocalNetworkGateway** Elimina l'oggetto che rappresenta il Gateway on-Prem in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06637-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="06637-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06637-108">EXAMPLES</span></span>

### <span data-ttu-id="06637-109">1: eliminare un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="06637-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="06637-110">Elimina l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="06637-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="06637-111">Nota: prima di tutto, è necessario eliminare tutte le connessioni al gateway di rete locale usando il cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="06637-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="06637-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06637-112">PARAMETERS</span></span>

### <span data-ttu-id="06637-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06637-113">-AsJob</span></span>
<span data-ttu-id="06637-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="06637-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06637-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06637-115">-DefaultProfile</span></span>
<span data-ttu-id="06637-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06637-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06637-117">-Force</span><span class="sxs-lookup"><span data-stu-id="06637-117">-Force</span></span>
<span data-ttu-id="06637-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="06637-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06637-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="06637-119">-Name</span></span>
<span data-ttu-id="06637-120">Specifica il nome del gateway di rete locale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06637-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="06637-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06637-121">-PassThru</span></span>
<span data-ttu-id="06637-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="06637-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06637-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="06637-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06637-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06637-124">-ResourceGroupName</span></span>
<span data-ttu-id="06637-125">Specifica il nome del gruppo di risorse che contiene il gateway di rete locale.</span><span class="sxs-lookup"><span data-stu-id="06637-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="06637-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06637-126">-Confirm</span></span>
<span data-ttu-id="06637-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06637-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06637-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06637-128">-WhatIf</span></span>
<span data-ttu-id="06637-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06637-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06637-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06637-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06637-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06637-131">CommonParameters</span></span>
<span data-ttu-id="06637-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06637-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06637-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06637-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06637-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06637-134">INPUTS</span></span>

### <span data-ttu-id="06637-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="06637-135">None</span></span>
<span data-ttu-id="06637-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="06637-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06637-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06637-137">OUTPUTS</span></span>

## <span data-ttu-id="06637-138">Note</span><span class="sxs-lookup"><span data-stu-id="06637-138">NOTES</span></span>

## <span data-ttu-id="06637-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06637-139">RELATED LINKS</span></span>

[<span data-ttu-id="06637-140">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06637-140">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="06637-141">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06637-141">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="06637-142">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="06637-142">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


