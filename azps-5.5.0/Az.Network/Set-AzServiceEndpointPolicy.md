---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184150"
---
# <span data-ttu-id="c9fac-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9fac-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="c9fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9fac-102">SYNOPSIS</span></span>
<span data-ttu-id="c9fac-103">Aggiorna i criteri degli endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="c9fac-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="c9fac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9fac-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9fac-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9fac-105">DESCRIPTION</span></span>
<span data-ttu-id="c9fac-106">Il cmdlet **Set-AzServiceEndpointPolicy** crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="c9fac-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="c9fac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9fac-107">EXAMPLES</span></span>

### <span data-ttu-id="c9fac-108">Esempio 1: Imposta un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="c9fac-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="c9fac-109">Questo comando aggiorna un criterio endpoint di servizio denominato Criterio1 definito dall'oggetto $serviceEndpointPolicy appartiene al gruppo di risorse "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="c9fac-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="c9fac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9fac-110">PARAMETERS</span></span>

### <span data-ttu-id="c9fac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9fac-111">-DefaultProfile</span></span>
<span data-ttu-id="c9fac-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9fac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9fac-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9fac-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="c9fac-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9fac-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9fac-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9fac-115">-Confirm</span></span>
<span data-ttu-id="c9fac-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9fac-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9fac-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9fac-117">-WhatIf</span></span>
<span data-ttu-id="c9fac-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9fac-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9fac-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9fac-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9fac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9fac-120">CommonParameters</span></span>
<span data-ttu-id="c9fac-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9fac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9fac-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9fac-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9fac-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9fac-123">INPUTS</span></span>

### <span data-ttu-id="c9fac-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9fac-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c9fac-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9fac-125">OUTPUTS</span></span>

### <span data-ttu-id="c9fac-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9fac-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c9fac-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9fac-127">NOTES</span></span>

## <span data-ttu-id="c9fac-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9fac-128">RELATED LINKS</span></span>

[<span data-ttu-id="c9fac-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9fac-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="c9fac-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9fac-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="c9fac-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9fac-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
