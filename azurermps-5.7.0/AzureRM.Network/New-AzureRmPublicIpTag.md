---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 56352ff165d2e7dcbf5386e713028fae5c991d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521024"
---
# <span data-ttu-id="2c944-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="2c944-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="2c944-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c944-102">SYNOPSIS</span></span>
<span data-ttu-id="2c944-103">Crea un tag IP.</span><span class="sxs-lookup"><span data-stu-id="2c944-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c944-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c944-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2c944-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c944-105">DESCRIPTION</span></span>
<span data-ttu-id="2c944-106">Il cmdlet **New-AzureRmPublicIpTag** crea un tag IP.</span><span class="sxs-lookup"><span data-stu-id="2c944-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="2c944-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c944-107">EXAMPLES</span></span>

### <span data-ttu-id="2c944-108">1: creare un nuovo tag IP</span><span class="sxs-lookup"><span data-stu-id="2c944-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="2c944-109">Questo comando crea un nuovo tag IP con TagType come "FirstPartyUsage" e contrassegna come "/SQL".</span><span class="sxs-lookup"><span data-stu-id="2c944-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="2c944-110">Viene usato nella creazione di publicIpAddress con questi tag specifici per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="2c944-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="2c944-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c944-111">PARAMETERS</span></span>

### <span data-ttu-id="2c944-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c944-112">-DefaultProfile</span></span>
<span data-ttu-id="2c944-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c944-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c944-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="2c944-114">-IpTagType</span></span>
<span data-ttu-id="2c944-115">Esempio di tipo IpTag: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="2c944-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c944-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c944-116">-Tag</span></span>
<span data-ttu-id="2c944-117">Esempio di valore IpTag:/SQL</span><span class="sxs-lookup"><span data-stu-id="2c944-117">IpTag value Example:/Sql</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c944-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c944-118">-Confirm</span></span>
<span data-ttu-id="2c944-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c944-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c944-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c944-120">-WhatIf</span></span>
<span data-ttu-id="2c944-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c944-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c944-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c944-122">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="2c944-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c944-123">INPUTS</span></span>

### <span data-ttu-id="2c944-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2c944-124">System.String</span></span>


## <span data-ttu-id="2c944-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c944-125">OUTPUTS</span></span>

### <span data-ttu-id="2c944-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="2c944-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>


## <span data-ttu-id="2c944-127">Note</span><span class="sxs-lookup"><span data-stu-id="2c944-127">NOTES</span></span>

## <span data-ttu-id="2c944-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c944-128">RELATED LINKS</span></span>

