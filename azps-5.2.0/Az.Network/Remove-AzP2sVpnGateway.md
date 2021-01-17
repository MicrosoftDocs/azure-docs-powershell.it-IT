---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328031"
---
# <span data-ttu-id="7741c-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7741c-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="7741c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7741c-102">SYNOPSIS</span></span>
<span data-ttu-id="7741c-103">Rimuove un P2SVpnGateway esistente.</span><span class="sxs-lookup"><span data-stu-id="7741c-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="7741c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7741c-104">SYNTAX</span></span>

### <span data-ttu-id="7741c-105">ByP2SVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7741c-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7741c-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7741c-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7741c-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7741c-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7741c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7741c-108">DESCRIPTION</span></span>
<span data-ttu-id="7741c-109">Il cmdlet **Remove-AzP2sVpnGateway** consente di rimuovere un P2SVpnGateway esistente in VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7741c-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="7741c-110">Tutta la connettività point to site clients non riuscirà dopo la rimozione di P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7741c-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="7741c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7741c-111">EXAMPLES</span></span>

### <span data-ttu-id="7741c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7741c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="7741c-113">Il cmdlet **Remove-AzP2sVpnGateway** consente di rimuovere un P2SVpnGateway esistente in VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7741c-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="7741c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7741c-114">PARAMETERS</span></span>

### <span data-ttu-id="7741c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7741c-115">-DefaultProfile</span></span>
<span data-ttu-id="7741c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7741c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7741c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7741c-117">-Force</span></span>
<span data-ttu-id="7741c-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7741c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7741c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7741c-119">-InputObject</span></span>
<span data-ttu-id="7741c-120">Oggetto p2sVpnGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="7741c-120">The p2sVpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="7741c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7741c-121">-Name</span></span>
<span data-ttu-id="7741c-122">Il nome P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7741c-122">The P2SVpnGateway name.</span></span>

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

### <span data-ttu-id="7741c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7741c-123">-PassThru</span></span>
<span data-ttu-id="7741c-124">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7741c-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="7741c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7741c-125">-ResourceGroupName</span></span>
<span data-ttu-id="7741c-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7741c-126">The resource group name.</span></span>

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

### <span data-ttu-id="7741c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7741c-127">-ResourceId</span></span>
<span data-ttu-id="7741c-128">ID risorsa di Azure per l'p2sVpnGateway da eliminare.</span><span class="sxs-lookup"><span data-stu-id="7741c-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="7741c-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7741c-129">-Confirm</span></span>
<span data-ttu-id="7741c-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7741c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7741c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7741c-131">-WhatIf</span></span>
<span data-ttu-id="7741c-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7741c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7741c-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7741c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7741c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7741c-134">CommonParameters</span></span>
<span data-ttu-id="7741c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7741c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7741c-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7741c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7741c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7741c-137">INPUTS</span></span>

### <span data-ttu-id="7741c-138">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7741c-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="7741c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7741c-139">System.String</span></span>

## <span data-ttu-id="7741c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7741c-140">OUTPUTS</span></span>

### <span data-ttu-id="7741c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7741c-141">System.Boolean</span></span>

## <span data-ttu-id="7741c-142">Note</span><span class="sxs-lookup"><span data-stu-id="7741c-142">NOTES</span></span>

## <span data-ttu-id="7741c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7741c-143">RELATED LINKS</span></span>
