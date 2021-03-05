---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: c331cbb9731024598fe4d2542e734e406ac144ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993536"
---
# <span data-ttu-id="6c1c5-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c1c5-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="6c1c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1c5-103">Rimuove un'istanza di P2SVpnGateway esistente.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="6c1c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c1c5-104">SYNTAX</span></span>

### <span data-ttu-id="6c1c5-105">ByP2SVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c1c5-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c1c5-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6c1c5-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c1c5-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6c1c5-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c1c5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c1c5-108">DESCRIPTION</span></span>
<span data-ttu-id="6c1c5-109">Il cmdlet **Remove-AzP2sVpnGateway** consente di rimuovere un P2SVpnGateway esistente in VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="6c1c5-110">Dopo la rimozione di P2SVpnGateway, la connettività dei client del sito avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="6c1c5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c1c5-111">EXAMPLES</span></span>

### <span data-ttu-id="6c1c5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c1c5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="6c1c5-113">Il cmdlet **Remove-AzP2sVpnGateway** consente di rimuovere un P2SVpnGateway esistente in VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="6c1c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c1c5-114">PARAMETERS</span></span>

### <span data-ttu-id="6c1c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1c5-115">-DefaultProfile</span></span>
<span data-ttu-id="6c1c5-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c1c5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6c1c5-117">-Force</span></span>
<span data-ttu-id="6c1c5-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6c1c5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c1c5-119">-InputObject</span></span>
<span data-ttu-id="6c1c5-120">Oggetto p2sVpnGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1c5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6c1c5-121">-Name</span></span>
<span data-ttu-id="6c1c5-122">Nome P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c1c5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c1c5-123">-PassThru</span></span>
<span data-ttu-id="6c1c5-124">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="6c1c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c1c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="6c1c5-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c1c5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c1c5-127">-ResourceId</span></span>
<span data-ttu-id="6c1c5-128">ID della risorsa Azure per p2sVpnGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1c5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c1c5-129">-Confirm</span></span>
<span data-ttu-id="6c1c5-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c1c5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c1c5-131">-WhatIf</span></span>
<span data-ttu-id="6c1c5-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c1c5-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c1c5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1c5-134">CommonParameters</span></span>
<span data-ttu-id="6c1c5-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c1c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1c5-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c1c5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1c5-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c1c5-137">INPUTS</span></span>

### <span data-ttu-id="6c1c5-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6c1c5-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="6c1c5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6c1c5-139">System.String</span></span>

## <span data-ttu-id="6c1c5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c1c5-140">OUTPUTS</span></span>

### <span data-ttu-id="6c1c5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c1c5-141">System.Boolean</span></span>

## <span data-ttu-id="6c1c5-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c1c5-142">NOTES</span></span>

## <span data-ttu-id="6c1c5-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c1c5-143">RELATED LINKS</span></span>
