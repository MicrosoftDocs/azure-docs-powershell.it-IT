---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: ad9c032a4384a82e03704529796a209e8c88f4c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203715"
---
# <span data-ttu-id="89210-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="89210-101">New-AzIotHub</span></span>

## <span data-ttu-id="89210-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89210-102">SYNOPSIS</span></span>
<span data-ttu-id="89210-103">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="89210-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="89210-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89210-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89210-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89210-105">DESCRIPTION</span></span>
<span data-ttu-id="89210-106">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="89210-106">Creates a new IotHub.</span></span>
<span data-ttu-id="89210-107">Puoi creare IotHub con le proprietà predefinite o specificare le proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="89210-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="89210-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89210-108">EXAMPLES</span></span>

### <span data-ttu-id="89210-109">Esempio 1 creare un nuovo IotHub con le proprietà predefinite</span><span class="sxs-lookup"><span data-stu-id="89210-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="89210-110">Crea un nuovo IotHub denominato "myiothub" dell'USK "S1", capacità 1 e posizione "northeurope".</span><span class="sxs-lookup"><span data-stu-id="89210-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="89210-111">Esempio 2 creare un nuovo IotHub con la MaxDeliveryCount della coda CloudToDevice impostata su 20</span><span class="sxs-lookup"><span data-stu-id="89210-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="89210-112">Crea una nuova IotHub denominata "myiothub" della SKU "S1", capacità 1 e posizione "northeurope" con le proprietà di input avanzate rappresentate da $properties.</span><span class="sxs-lookup"><span data-stu-id="89210-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="89210-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-SkuName "S1"-unità 1-location "northeurope"-properties $properties</span><span class="sxs-lookup"><span data-stu-id="89210-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="89210-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89210-114">PARAMETERS</span></span>

### <span data-ttu-id="89210-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89210-115">-DefaultProfile</span></span>
<span data-ttu-id="89210-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="89210-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89210-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="89210-117">-Location</span></span>
<span data-ttu-id="89210-118">Posizione in cui deve essere creato il mozzo.</span><span class="sxs-lookup"><span data-stu-id="89210-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="89210-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="89210-119">-Name</span></span>
<span data-ttu-id="89210-120">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="89210-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="89210-121">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="89210-121">-Properties</span></span>
<span data-ttu-id="89210-122">Proprietà dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="89210-122">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89210-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89210-123">-ResourceGroupName</span></span>
<span data-ttu-id="89210-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="89210-124">Resource Group Name</span></span>

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

### <span data-ttu-id="89210-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="89210-125">-SkuName</span></span>
<span data-ttu-id="89210-126">Nome dell'USK</span><span class="sxs-lookup"><span data-stu-id="89210-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89210-127">-Unità</span><span class="sxs-lookup"><span data-stu-id="89210-127">-Units</span></span>
<span data-ttu-id="89210-128">Numero di unità</span><span class="sxs-lookup"><span data-stu-id="89210-128">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89210-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89210-129">-Confirm</span></span>
<span data-ttu-id="89210-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89210-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89210-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89210-131">-WhatIf</span></span>
<span data-ttu-id="89210-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89210-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89210-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89210-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89210-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89210-134">CommonParameters</span></span>
<span data-ttu-id="89210-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89210-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89210-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89210-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89210-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89210-137">INPUTS</span></span>

### <span data-ttu-id="89210-138">System. String</span><span class="sxs-lookup"><span data-stu-id="89210-138">System.String</span></span>

## <span data-ttu-id="89210-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89210-139">OUTPUTS</span></span>

### <span data-ttu-id="89210-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="89210-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="89210-141">Note</span><span class="sxs-lookup"><span data-stu-id="89210-141">NOTES</span></span>

## <span data-ttu-id="89210-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89210-142">RELATED LINKS</span></span>
