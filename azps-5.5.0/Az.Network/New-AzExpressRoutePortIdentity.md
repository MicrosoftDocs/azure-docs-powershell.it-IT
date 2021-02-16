---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortIdentity.md
ms.openlocfilehash: d19acf8bb97f3b84b3cd831e4cf91397231f4b08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189687"
---
# <span data-ttu-id="a8248-101">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a8248-101">New-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="a8248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8248-102">SYNOPSIS</span></span>
<span data-ttu-id="a8248-103">Crea un azure ExpressRoutePortIdentity.</span><span class="sxs-lookup"><span data-stu-id="a8248-103">Creates an Azure ExpressRoutePortIdentity.</span></span>

## <span data-ttu-id="a8248-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8248-104">SYNTAX</span></span>

```
New-AzExpressRoutePortIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8248-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8248-105">DESCRIPTION</span></span>
<span data-ttu-id="a8248-106">Il cmdlet **New-AzExpressRoutePortIdentity** crea un oggetto Identità Azure ExpressRoutePort locale.</span><span class="sxs-lookup"><span data-stu-id="a8248-106">The **New-AzExpressRoutePortIdentity** cmdlet creates a local Azure ExpressRoutePort Identity object.</span></span> <span data-ttu-id="a8248-107">Usare **New-AzExpressRoutePort** o **Set-AzExpressRoutePort** per assegnarlo ad Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a8248-107">Use **New-AzExpressRoutePort** or **Set-AzExpressRoutePort** to assign it to Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="a8248-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8248-108">EXAMPLES</span></span>

### <span data-ttu-id="a8248-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8248-109">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    UserAssignedIdentityId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<IdentityName>'
    }
PS C:\> New-AzExpressRoutePortIdentity @parameters
```

## <span data-ttu-id="a8248-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8248-110">PARAMETERS</span></span>

### <span data-ttu-id="a8248-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8248-111">-DefaultProfile</span></span>
<span data-ttu-id="a8248-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8248-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8248-113">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="a8248-113">-UserAssignedIdentityId</span></span>
<span data-ttu-id="a8248-114">ResourceId dell'identità assegnata all'utente da assegnare a ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a8248-114">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="a8248-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8248-115">-Confirm</span></span>
<span data-ttu-id="a8248-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8248-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8248-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8248-117">-WhatIf</span></span>
<span data-ttu-id="a8248-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8248-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8248-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8248-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8248-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8248-120">CommonParameters</span></span>
<span data-ttu-id="a8248-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8248-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8248-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8248-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8248-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8248-123">INPUTS</span></span>

### <span data-ttu-id="a8248-124">System.String</span><span class="sxs-lookup"><span data-stu-id="a8248-124">System.String</span></span>

## <span data-ttu-id="a8248-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8248-125">OUTPUTS</span></span>

### <span data-ttu-id="a8248-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a8248-126">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="a8248-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8248-127">NOTES</span></span>

## <span data-ttu-id="a8248-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8248-128">RELATED LINKS</span></span>
[<span data-ttu-id="a8248-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a8248-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="a8248-130">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a8248-130">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="a8248-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="a8248-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)