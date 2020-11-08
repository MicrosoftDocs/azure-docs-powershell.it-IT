---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192743"
---
# <span data-ttu-id="14ca2-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="14ca2-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="14ca2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="14ca2-103">Aggiorna un'identità assegnata a un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="14ca2-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="14ca2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14ca2-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ca2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14ca2-105">DESCRIPTION</span></span>
<span data-ttu-id="14ca2-106">Il cmdlet **set-AzExpressRoutePortIdentity** aggiorna un oggetto ExpressRoutePort Azure locale.</span><span class="sxs-lookup"><span data-stu-id="14ca2-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="14ca2-107">USA **set-AzExpressRoutePort** per assegnarlo a ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="14ca2-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="14ca2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14ca2-108">EXAMPLES</span></span>

### <span data-ttu-id="14ca2-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14ca2-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="14ca2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14ca2-110">PARAMETERS</span></span>

### <span data-ttu-id="14ca2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ca2-111">-DefaultProfile</span></span>
<span data-ttu-id="14ca2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14ca2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14ca2-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="14ca2-113">-ExpressRoutePort</span></span>
<span data-ttu-id="14ca2-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="14ca2-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="14ca2-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="14ca2-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="14ca2-116">ResourceId dell'identità assegnata dall'utente da assegnare a ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="14ca2-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="14ca2-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="14ca2-117">-Confirm</span></span>
<span data-ttu-id="14ca2-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14ca2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14ca2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14ca2-119">-WhatIf</span></span>
<span data-ttu-id="14ca2-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14ca2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14ca2-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14ca2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14ca2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ca2-122">CommonParameters</span></span>
<span data-ttu-id="14ca2-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14ca2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ca2-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14ca2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ca2-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14ca2-125">INPUTS</span></span>

### <span data-ttu-id="14ca2-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="14ca2-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="14ca2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="14ca2-127">System.String</span></span>

## <span data-ttu-id="14ca2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14ca2-128">OUTPUTS</span></span>

### <span data-ttu-id="14ca2-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="14ca2-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="14ca2-130">Note</span><span class="sxs-lookup"><span data-stu-id="14ca2-130">NOTES</span></span>

## <span data-ttu-id="14ca2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14ca2-131">RELATED LINKS</span></span>
[<span data-ttu-id="14ca2-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="14ca2-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="14ca2-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="14ca2-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="14ca2-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="14ca2-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
