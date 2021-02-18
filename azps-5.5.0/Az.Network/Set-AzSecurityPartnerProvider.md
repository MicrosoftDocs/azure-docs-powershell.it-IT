---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206498"
---
# <span data-ttu-id="3b0c0-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3b0c0-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="3b0c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b0c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0c0-103">Salva un Provider SecurityPartnerProvider modificato.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="3b0c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b0c0-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b0c0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3b0c0-105">DESCRIPTION</span></span>
<span data-ttu-id="3b0c0-106">Il cmdlet **Set-AzSecurityPartnerProvider** aggiorna un provider di sicurezza di Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3b0c0-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="3b0c0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b0c0-107">EXAMPLES</span></span>

### <span data-ttu-id="3b0c0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3b0c0-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="3b0c0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b0c0-109">PARAMETERS</span></span>

### <span data-ttu-id="3b0c0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b0c0-110">-AsJob</span></span>
<span data-ttu-id="3b0c0-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3b0c0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b0c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0c0-112">-DefaultProfile</span></span>
<span data-ttu-id="3b0c0-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b0c0-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3b0c0-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="3b0c0-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3b0c0-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b0c0-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b0c0-116">-Confirm</span></span>
<span data-ttu-id="3b0c0-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b0c0-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b0c0-118">-WhatIf</span></span>
<span data-ttu-id="3b0c0-119">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b0c0-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b0c0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0c0-121">CommonParameters</span></span>
<span data-ttu-id="3b0c0-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0c0-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0c0-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="3b0c0-124">INPUTS</span></span>

### <span data-ttu-id="3b0c0-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3b0c0-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3b0c0-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b0c0-126">OUTPUTS</span></span>

### <span data-ttu-id="3b0c0-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3b0c0-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3b0c0-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="3b0c0-128">NOTES</span></span>

## <span data-ttu-id="3b0c0-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b0c0-129">RELATED LINKS</span></span>
