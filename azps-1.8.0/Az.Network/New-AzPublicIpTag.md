---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 7e4bfae0479d4f37f6a73c8e07239112267ac182
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678243"
---
# <span data-ttu-id="c73e2-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="c73e2-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="c73e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c73e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c73e2-103">Crea un tag IP.</span><span class="sxs-lookup"><span data-stu-id="c73e2-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="c73e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c73e2-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c73e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c73e2-105">DESCRIPTION</span></span>
<span data-ttu-id="c73e2-106">Il cmdlet **New-AzPublicIpTag** crea un tag IP.</span><span class="sxs-lookup"><span data-stu-id="c73e2-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="c73e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c73e2-107">EXAMPLES</span></span>

### <span data-ttu-id="c73e2-108">1: creare un nuovo tag IP</span><span class="sxs-lookup"><span data-stu-id="c73e2-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="c73e2-109">Questo comando crea un nuovo tag IP con TagType come "FirstPartyUsage" e contrassegna come "/SQL".</span><span class="sxs-lookup"><span data-stu-id="c73e2-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="c73e2-110">Viene usato nella creazione di publicIpAddress con questi tag specifici per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="c73e2-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="c73e2-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c73e2-111">PARAMETERS</span></span>

### <span data-ttu-id="c73e2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73e2-112">-DefaultProfile</span></span>
<span data-ttu-id="c73e2-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c73e2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c73e2-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="c73e2-114">-IpTagType</span></span>
<span data-ttu-id="c73e2-115">Esempio di tipo IpTag: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="c73e2-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c73e2-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="c73e2-116">-Tag</span></span>
<span data-ttu-id="c73e2-117">Esempio di valore IpTag:/SQL</span><span class="sxs-lookup"><span data-stu-id="c73e2-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c73e2-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c73e2-118">-Confirm</span></span>
<span data-ttu-id="c73e2-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c73e2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c73e2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c73e2-120">-WhatIf</span></span>
<span data-ttu-id="c73e2-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c73e2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c73e2-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c73e2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c73e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73e2-123">CommonParameters</span></span>
<span data-ttu-id="c73e2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c73e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73e2-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c73e2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73e2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c73e2-126">INPUTS</span></span>

### <span data-ttu-id="c73e2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c73e2-127">System.String</span></span>

## <span data-ttu-id="c73e2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c73e2-128">OUTPUTS</span></span>

### <span data-ttu-id="c73e2-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="c73e2-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="c73e2-130">Note</span><span class="sxs-lookup"><span data-stu-id="c73e2-130">NOTES</span></span>

## <span data-ttu-id="c73e2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c73e2-131">RELATED LINKS</span></span>
