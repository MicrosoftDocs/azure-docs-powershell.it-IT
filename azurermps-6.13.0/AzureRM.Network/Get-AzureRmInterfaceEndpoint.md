---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515108"
---
# <span data-ttu-id="47e3d-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="47e3d-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="47e3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="47e3d-103">Il cmdlet Get-AzureRmInterfaceEndpoint ottiene un endpoint di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="47e3d-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47e3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47e3d-104">SYNTAX</span></span>

### <span data-ttu-id="47e3d-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47e3d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47e3d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47e3d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47e3d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47e3d-107">DESCRIPTION</span></span>
<span data-ttu-id="47e3d-108">Il cmdlet **Get-AzureRmInterfaceEndpoint** ottiene un endpoint di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="47e3d-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="47e3d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47e3d-109">EXAMPLES</span></span>

### <span data-ttu-id="47e3d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47e3d-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="47e3d-111">Questo comando ottiene l'endpoint di interfaccia denominato InterfaceEndpoint1 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="47e3d-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="47e3d-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="47e3d-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="47e3d-113">Questo comando ottiene l'endpoint dell'interfaccia con resourceId/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 e lo archivia nella variabile $interfaceendpoint.</span><span class="sxs-lookup"><span data-stu-id="47e3d-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="47e3d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47e3d-114">PARAMETERS</span></span>

### <span data-ttu-id="47e3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e3d-115">-DefaultProfile</span></span>
<span data-ttu-id="47e3d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47e3d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e3d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="47e3d-117">-Name</span></span>
<span data-ttu-id="47e3d-118">Nome dell'endpoint di interfaccia</span><span class="sxs-lookup"><span data-stu-id="47e3d-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e3d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e3d-119">-ResourceGroupName</span></span>
<span data-ttu-id="47e3d-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="47e3d-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e3d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47e3d-121">-ResourceId</span></span>
<span data-ttu-id="47e3d-122">{{Fill ResourceId Description}}</span><span class="sxs-lookup"><span data-stu-id="47e3d-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e3d-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47e3d-123">-Confirm</span></span>
<span data-ttu-id="47e3d-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47e3d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e3d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e3d-125">-WhatIf</span></span>
<span data-ttu-id="47e3d-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47e3d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47e3d-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47e3d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e3d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e3d-128">CommonParameters</span></span>
<span data-ttu-id="47e3d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e3d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="47e3d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e3d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e3d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47e3d-131">INPUTS</span></span>

### <span data-ttu-id="47e3d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="47e3d-132">System.String</span></span>


## <span data-ttu-id="47e3d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47e3d-133">OUTPUTS</span></span>

### <span data-ttu-id="47e3d-134">Microsoft. Azure. Commands. Network. Models. PSInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="47e3d-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="47e3d-135">Note</span><span class="sxs-lookup"><span data-stu-id="47e3d-135">NOTES</span></span>

## <span data-ttu-id="47e3d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47e3d-136">RELATED LINKS</span></span>
