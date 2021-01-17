---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475595"
---
# <span data-ttu-id="65953-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="65953-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="65953-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65953-102">SYNOPSIS</span></span>
<span data-ttu-id="65953-103">Configura un nuovo dispositivo Edge dello stack</span><span class="sxs-lookup"><span data-stu-id="65953-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="65953-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65953-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65953-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65953-105">DESCRIPTION</span></span>
<span data-ttu-id="65953-106">Il cmdlet **New-AzStackEdgeDevice** configura un nuovo dispositivo Edge dello stack</span><span class="sxs-lookup"><span data-stu-id="65953-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="65953-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65953-107">EXAMPLES</span></span>

### <span data-ttu-id="65953-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65953-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="65953-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65953-109">PARAMETERS</span></span>

### <span data-ttu-id="65953-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65953-110">-AsJob</span></span>
<span data-ttu-id="65953-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="65953-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65953-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65953-112">-DefaultProfile</span></span>
<span data-ttu-id="65953-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65953-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65953-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="65953-114">-Location</span></span>
<span data-ttu-id="65953-115">Posizione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="65953-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65953-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="65953-116">-Name</span></span>
<span data-ttu-id="65953-117">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="65953-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65953-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65953-118">-ResourceGroupName</span></span>
<span data-ttu-id="65953-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="65953-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65953-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="65953-120">-Sku</span></span>
<span data-ttu-id="65953-121">Le SKU disponibili sono Edge, gateway</span><span class="sxs-lookup"><span data-stu-id="65953-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65953-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65953-122">-Confirm</span></span>
<span data-ttu-id="65953-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65953-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65953-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65953-124">-WhatIf</span></span>
<span data-ttu-id="65953-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65953-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65953-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65953-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65953-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65953-127">CommonParameters</span></span>
<span data-ttu-id="65953-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65953-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65953-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65953-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65953-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65953-130">INPUTS</span></span>

### <span data-ttu-id="65953-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="65953-131">None</span></span>

## <span data-ttu-id="65953-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65953-132">OUTPUTS</span></span>

### <span data-ttu-id="65953-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="65953-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="65953-134">Note</span><span class="sxs-lookup"><span data-stu-id="65953-134">NOTES</span></span>

## <span data-ttu-id="65953-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65953-135">RELATED LINKS</span></span>
