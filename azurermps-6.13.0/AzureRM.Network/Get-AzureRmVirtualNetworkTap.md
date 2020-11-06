---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513747"
---
# <span data-ttu-id="a1b39-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a1b39-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="a1b39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1b39-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b39-103">Ottiene un tocco di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a1b39-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1b39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1b39-104">SYNTAX</span></span>

### <span data-ttu-id="a1b39-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1b39-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b39-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b39-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b39-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1b39-107">DESCRIPTION</span></span>
<span data-ttu-id="a1b39-108">Il cmdlet **Get-AzureRmVirtualNetworkTap** ottiene un tocco di rete virtuale di Azure o un elenco di rubinetti di rete virtuali Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1b39-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="a1b39-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1b39-109">EXAMPLES</span></span>

### <span data-ttu-id="a1b39-110">Esempio 1: ottenere un tocco di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a1b39-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="a1b39-111">Questo comando ottiene un riferimento VirtualNetwork tap per "VirtualTap1" in "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="a1b39-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="a1b39-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1b39-112">PARAMETERS</span></span>

### <span data-ttu-id="a1b39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b39-113">-DefaultProfile</span></span>
<span data-ttu-id="a1b39-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b39-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b39-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1b39-115">-Name</span></span>
<span data-ttu-id="a1b39-116">Nome del tocco.</span><span class="sxs-lookup"><span data-stu-id="a1b39-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b39-117">-ResourceGroupName</span></span>
<span data-ttu-id="a1b39-118">Nome del gruppo di risorse del tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a1b39-118">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b39-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b39-119">-ResourceId</span></span>
<span data-ttu-id="a1b39-120">ResourceId della risorsa VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a1b39-120">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b39-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1b39-121">-Confirm</span></span>
<span data-ttu-id="a1b39-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1b39-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b39-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b39-123">-WhatIf</span></span>
<span data-ttu-id="a1b39-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1b39-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1b39-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1b39-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b39-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b39-126">CommonParameters</span></span>
<span data-ttu-id="a1b39-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b39-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b39-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b39-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b39-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1b39-129">INPUTS</span></span>

### <span data-ttu-id="a1b39-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b39-130">System.String</span></span>

## <span data-ttu-id="a1b39-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1b39-131">OUTPUTS</span></span>

### <span data-ttu-id="a1b39-132">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a1b39-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="a1b39-133">Note</span><span class="sxs-lookup"><span data-stu-id="a1b39-133">NOTES</span></span>

## <span data-ttu-id="a1b39-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1b39-134">RELATED LINKS</span></span>
