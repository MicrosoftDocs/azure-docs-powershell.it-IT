---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507388"
---
# <span data-ttu-id="6878a-101">Set-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6878a-101">Set-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="6878a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6878a-102">SYNOPSIS</span></span>
<span data-ttu-id="6878a-103">Imposta i tag per un PublicIpPrefix esistente</span><span class="sxs-lookup"><span data-stu-id="6878a-103">Sets the Tags for an existing PublicIpPrefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6878a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6878a-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6878a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6878a-105">DESCRIPTION</span></span>
<span data-ttu-id="6878a-106">Il cmdlet **set-AzureRmPublicIpPrefix** imposta i tag per un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="6878a-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="6878a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6878a-107">EXAMPLES</span></span>

### <span data-ttu-id="6878a-108">Impostare i tag per il prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="6878a-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="6878a-109">Il primo comando ottiene un prefisso IP pubblico esistente, il secondo comando imposta la proprietà Tags e il terzo comando Aggiorna l'oggetto esistente.</span><span class="sxs-lookup"><span data-stu-id="6878a-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="6878a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6878a-110">PARAMETERS</span></span>

### <span data-ttu-id="6878a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6878a-111">-AsJob</span></span>
<span data-ttu-id="6878a-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6878a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6878a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6878a-113">-DefaultProfile</span></span>
<span data-ttu-id="6878a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6878a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6878a-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6878a-115">-PublicIpPrefix</span></span>
<span data-ttu-id="6878a-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6878a-116">The PublicIpPrefix</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6878a-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6878a-117">-Confirm</span></span>
<span data-ttu-id="6878a-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6878a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6878a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6878a-119">-WhatIf</span></span>
<span data-ttu-id="6878a-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6878a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6878a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6878a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6878a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6878a-122">CommonParameters</span></span>
<span data-ttu-id="6878a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6878a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6878a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6878a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6878a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6878a-125">INPUTS</span></span>

### <span data-ttu-id="6878a-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6878a-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="6878a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6878a-127">OUTPUTS</span></span>

### <span data-ttu-id="6878a-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6878a-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="6878a-129">Note</span><span class="sxs-lookup"><span data-stu-id="6878a-129">NOTES</span></span>

## <span data-ttu-id="6878a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6878a-130">RELATED LINKS</span></span>
