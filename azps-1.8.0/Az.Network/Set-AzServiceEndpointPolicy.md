---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 75cf6bac1913a2baa55a28135ba2d59f5ceaa07f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677925"
---
# <span data-ttu-id="4ecfa-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ecfa-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="4ecfa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ecfa-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecfa-103">Aggiorna un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="4ecfa-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="4ecfa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ecfa-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ecfa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ecfa-105">DESCRIPTION</span></span>
<span data-ttu-id="4ecfa-106">Il cmdlet **set-AzServiceEndpointPolicy** crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="4ecfa-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="4ecfa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ecfa-107">EXAMPLES</span></span>

### <span data-ttu-id="4ecfa-108">Esempio 1: imposta un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="4ecfa-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="4ecfa-109">Questo comando aggiorna un criterio endpoint del servizio denominato Policy1 definito dall'oggetto $serviceEndpointPolicy appartengono alla ResourceGroup "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="4ecfa-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="4ecfa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ecfa-110">PARAMETERS</span></span>

### <span data-ttu-id="4ecfa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecfa-111">-DefaultProfile</span></span>
<span data-ttu-id="4ecfa-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ecfa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ecfa-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ecfa-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4ecfa-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ecfa-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="4ecfa-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ecfa-115">-Confirm</span></span>
<span data-ttu-id="4ecfa-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ecfa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ecfa-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ecfa-117">-WhatIf</span></span>
<span data-ttu-id="4ecfa-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ecfa-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ecfa-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ecfa-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ecfa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecfa-120">CommonParameters</span></span>
<span data-ttu-id="4ecfa-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ecfa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecfa-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ecfa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecfa-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ecfa-123">INPUTS</span></span>

### <span data-ttu-id="4ecfa-124">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ecfa-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4ecfa-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ecfa-125">OUTPUTS</span></span>

### <span data-ttu-id="4ecfa-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ecfa-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4ecfa-127">Note</span><span class="sxs-lookup"><span data-stu-id="4ecfa-127">NOTES</span></span>

## <span data-ttu-id="4ecfa-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ecfa-128">RELATED LINKS</span></span>

[<span data-ttu-id="4ecfa-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ecfa-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="4ecfa-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ecfa-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="4ecfa-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4ecfa-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)