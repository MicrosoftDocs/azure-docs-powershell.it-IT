---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 6292c2fd19ff61e347291d3aba7e9840799e3b93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976558"
---
# <span data-ttu-id="fc35a-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fc35a-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="fc35a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc35a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc35a-103">Aggiorna un'identità assegnata a ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="fc35a-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="fc35a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc35a-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc35a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc35a-105">DESCRIPTION</span></span>
<span data-ttu-id="fc35a-106">Il cmdlet **Set-AzExpressRoutePortIdentity** aggiorna un oggetto Azure ExpressRoutePort locale.</span><span class="sxs-lookup"><span data-stu-id="fc35a-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="fc35a-107">Usare **Set-AzExpressRoutePort** per assegnarlo a ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="fc35a-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="fc35a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc35a-108">EXAMPLES</span></span>

### <span data-ttu-id="fc35a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc35a-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="fc35a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc35a-110">PARAMETERS</span></span>

### <span data-ttu-id="fc35a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc35a-111">-DefaultProfile</span></span>
<span data-ttu-id="fc35a-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc35a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc35a-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fc35a-113">-ExpressRoutePort</span></span>
<span data-ttu-id="fc35a-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fc35a-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc35a-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="fc35a-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="fc35a-116">ResourceId dell'identità assegnata all'utente da assegnare a ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="fc35a-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc35a-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc35a-117">-Confirm</span></span>
<span data-ttu-id="fc35a-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc35a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc35a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc35a-119">-WhatIf</span></span>
<span data-ttu-id="fc35a-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc35a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc35a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc35a-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc35a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc35a-122">CommonParameters</span></span>
<span data-ttu-id="fc35a-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc35a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc35a-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc35a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc35a-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc35a-125">INPUTS</span></span>

### <span data-ttu-id="fc35a-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fc35a-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="fc35a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fc35a-127">System.String</span></span>

## <span data-ttu-id="fc35a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc35a-128">OUTPUTS</span></span>

### <span data-ttu-id="fc35a-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fc35a-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="fc35a-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc35a-130">NOTES</span></span>

## <span data-ttu-id="fc35a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc35a-131">RELATED LINKS</span></span>
[<span data-ttu-id="fc35a-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fc35a-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="fc35a-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fc35a-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="fc35a-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fc35a-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
