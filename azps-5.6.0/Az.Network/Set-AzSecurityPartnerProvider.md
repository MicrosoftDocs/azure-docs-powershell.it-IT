---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 0a9ed100121c0f6610bcb019571fd1779f28dff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010302"
---
# <span data-ttu-id="cd417-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd417-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="cd417-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd417-102">SYNOPSIS</span></span>
<span data-ttu-id="cd417-103">Salva un Provider SecurityPartnerProvider modificato.</span><span class="sxs-lookup"><span data-stu-id="cd417-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="cd417-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd417-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd417-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd417-105">DESCRIPTION</span></span>
<span data-ttu-id="cd417-106">Il cmdlet **Set-AzSecurityPartnerProvider** aggiorna un provider di sicurezza di Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd417-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="cd417-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd417-107">EXAMPLES</span></span>

### <span data-ttu-id="cd417-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd417-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="cd417-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd417-109">PARAMETERS</span></span>

### <span data-ttu-id="cd417-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd417-110">-AsJob</span></span>
<span data-ttu-id="cd417-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cd417-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd417-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd417-112">-DefaultProfile</span></span>
<span data-ttu-id="cd417-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd417-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd417-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd417-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="cd417-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd417-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="cd417-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd417-116">-Confirm</span></span>
<span data-ttu-id="cd417-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd417-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd417-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd417-118">-WhatIf</span></span>
<span data-ttu-id="cd417-119">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd417-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd417-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd417-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd417-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd417-121">CommonParameters</span></span>
<span data-ttu-id="cd417-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd417-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd417-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd417-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd417-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd417-124">INPUTS</span></span>

### <span data-ttu-id="cd417-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd417-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="cd417-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd417-126">OUTPUTS</span></span>

### <span data-ttu-id="cd417-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd417-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="cd417-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd417-128">NOTES</span></span>

## <span data-ttu-id="cd417-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd417-129">RELATED LINKS</span></span>
