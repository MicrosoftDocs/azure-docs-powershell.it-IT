---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 07a29a17a1a7c17a0bbf7b202b019e7d833a5050
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188377"
---
# <span data-ttu-id="898a5-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="898a5-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="898a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="898a5-102">SYNOPSIS</span></span>
<span data-ttu-id="898a5-103">Salva un SecurityPartnerProvider di Azure modificato.</span><span class="sxs-lookup"><span data-stu-id="898a5-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="898a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="898a5-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="898a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="898a5-105">DESCRIPTION</span></span>
<span data-ttu-id="898a5-106">Il cmdlet **set-AzSecurityPartnerProvider** aggiorna un SecurityPartnerProvider di Azure</span><span class="sxs-lookup"><span data-stu-id="898a5-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="898a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="898a5-107">EXAMPLES</span></span>

### <span data-ttu-id="898a5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="898a5-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="898a5-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="898a5-109">PARAMETERS</span></span>

### <span data-ttu-id="898a5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="898a5-110">-AsJob</span></span>
<span data-ttu-id="898a5-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="898a5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="898a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="898a5-112">-DefaultProfile</span></span>
<span data-ttu-id="898a5-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="898a5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="898a5-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="898a5-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="898a5-115">SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="898a5-115">The SecurityPartnerProvider</span></span>

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

### <span data-ttu-id="898a5-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="898a5-116">-Confirm</span></span>
<span data-ttu-id="898a5-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="898a5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="898a5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="898a5-118">-WhatIf</span></span>
<span data-ttu-id="898a5-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="898a5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="898a5-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="898a5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="898a5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="898a5-121">CommonParameters</span></span>
<span data-ttu-id="898a5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="898a5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="898a5-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="898a5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="898a5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="898a5-124">INPUTS</span></span>

### <span data-ttu-id="898a5-125">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="898a5-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="898a5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="898a5-126">OUTPUTS</span></span>

### <span data-ttu-id="898a5-127">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="898a5-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="898a5-128">Note</span><span class="sxs-lookup"><span data-stu-id="898a5-128">NOTES</span></span>

## <span data-ttu-id="898a5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="898a5-129">RELATED LINKS</span></span>
