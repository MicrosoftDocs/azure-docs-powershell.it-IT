---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 5d7d73b3c7f49babc9e80929dab7b3fa2adad20a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190945"
---
# <span data-ttu-id="13ffc-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="13ffc-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="13ffc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="13ffc-103">Crea un tag IP.</span><span class="sxs-lookup"><span data-stu-id="13ffc-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="13ffc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13ffc-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13ffc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="13ffc-106">Il cmdlet **New-AzPublicIpTag** crea un tag IP.</span><span class="sxs-lookup"><span data-stu-id="13ffc-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="13ffc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13ffc-107">EXAMPLES</span></span>

### <span data-ttu-id="13ffc-108">Esempio 1: creare un nuovo tag IP</span><span class="sxs-lookup"><span data-stu-id="13ffc-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="13ffc-109">Questo comando crea un nuovo tag IP con TagType come "FirstPartyUsage" e contrassegna come "/SQL".</span><span class="sxs-lookup"><span data-stu-id="13ffc-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="13ffc-110">Viene usato nella creazione di publicIpAddress con questi tag specifici per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="13ffc-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="13ffc-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13ffc-111">PARAMETERS</span></span>

### <span data-ttu-id="13ffc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ffc-112">-DefaultProfile</span></span>
<span data-ttu-id="13ffc-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13ffc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13ffc-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="13ffc-114">-IpTagType</span></span>
<span data-ttu-id="13ffc-115">Esempio di tipo IpTag: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="13ffc-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="13ffc-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="13ffc-116">-Tag</span></span>
<span data-ttu-id="13ffc-117">Esempio di valore IpTag:/SQL</span><span class="sxs-lookup"><span data-stu-id="13ffc-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="13ffc-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="13ffc-118">-Confirm</span></span>
<span data-ttu-id="13ffc-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13ffc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13ffc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13ffc-120">-WhatIf</span></span>
<span data-ttu-id="13ffc-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13ffc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13ffc-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13ffc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13ffc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ffc-123">CommonParameters</span></span>
<span data-ttu-id="13ffc-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ffc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ffc-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13ffc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ffc-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13ffc-126">INPUTS</span></span>

### <span data-ttu-id="13ffc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="13ffc-127">System.String</span></span>

## <span data-ttu-id="13ffc-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13ffc-128">OUTPUTS</span></span>

### <span data-ttu-id="13ffc-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="13ffc-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="13ffc-130">Note</span><span class="sxs-lookup"><span data-stu-id="13ffc-130">NOTES</span></span>

## <span data-ttu-id="13ffc-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13ffc-131">RELATED LINKS</span></span>
