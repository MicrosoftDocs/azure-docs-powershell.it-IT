---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 11ecb6ed6c74ac7f87fb36723b88acc7c41819fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863102"
---
# <span data-ttu-id="c8602-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="c8602-101">New-AzIotHub</span></span>

## <span data-ttu-id="c8602-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8602-102">SYNOPSIS</span></span>
<span data-ttu-id="c8602-103">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="c8602-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="c8602-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8602-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8602-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8602-105">DESCRIPTION</span></span>
<span data-ttu-id="c8602-106">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="c8602-106">Creates a new IotHub.</span></span>
<span data-ttu-id="c8602-107">Puoi creare IotHub con le proprietà predefinite o specificare le proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="c8602-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="c8602-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8602-108">EXAMPLES</span></span>

### <span data-ttu-id="c8602-109">Esempio 1 creare un nuovo IotHub con le proprietà predefinite</span><span class="sxs-lookup"><span data-stu-id="c8602-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="c8602-110">Crea un nuovo IotHub denominato "myiothub" dell'USK "S1", capacità 1 e posizione "northeurope".</span><span class="sxs-lookup"><span data-stu-id="c8602-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="c8602-111">Esempio 2 creare un nuovo IotHub con la MaxDeliveryCount della coda CloudToDevice impostata su 20</span><span class="sxs-lookup"><span data-stu-id="c8602-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="c8602-112">Crea una nuova IotHub denominata "myiothub" della SKU "S1", capacità 1 e posizione "northeurope" con le proprietà di input avanzate rappresentate da $properties.</span><span class="sxs-lookup"><span data-stu-id="c8602-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="c8602-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-SkuName "S1"-unità 1-location "northeurope"-properties $properties</span><span class="sxs-lookup"><span data-stu-id="c8602-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="c8602-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8602-114">PARAMETERS</span></span>

### <span data-ttu-id="c8602-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8602-115">-DefaultProfile</span></span>
<span data-ttu-id="c8602-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c8602-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8602-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c8602-117">-Location</span></span>
<span data-ttu-id="c8602-118">Posizione in cui deve essere creato il mozzo.</span><span class="sxs-lookup"><span data-stu-id="c8602-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="c8602-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8602-119">-Name</span></span>
<span data-ttu-id="c8602-120">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="c8602-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="c8602-121">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="c8602-121">-Properties</span></span>
<span data-ttu-id="c8602-122">Proprietà dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="c8602-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="c8602-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8602-123">-ResourceGroupName</span></span>
<span data-ttu-id="c8602-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c8602-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c8602-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c8602-125">-SkuName</span></span>
<span data-ttu-id="c8602-126">Nome dell'USK</span><span class="sxs-lookup"><span data-stu-id="c8602-126">Name of the sku</span></span>

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

### <span data-ttu-id="c8602-127">-Unità</span><span class="sxs-lookup"><span data-stu-id="c8602-127">-Units</span></span>
<span data-ttu-id="c8602-128">Numero di unità</span><span class="sxs-lookup"><span data-stu-id="c8602-128">Number of units</span></span>

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

### <span data-ttu-id="c8602-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8602-129">-Confirm</span></span>
<span data-ttu-id="c8602-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8602-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8602-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8602-131">-WhatIf</span></span>
<span data-ttu-id="c8602-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8602-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8602-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8602-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8602-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8602-134">CommonParameters</span></span>
<span data-ttu-id="c8602-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8602-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8602-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8602-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8602-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8602-137">INPUTS</span></span>

### <span data-ttu-id="c8602-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c8602-138">System.String</span></span>

## <span data-ttu-id="c8602-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8602-139">OUTPUTS</span></span>

### <span data-ttu-id="c8602-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c8602-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="c8602-141">Note</span><span class="sxs-lookup"><span data-stu-id="c8602-141">NOTES</span></span>

## <span data-ttu-id="c8602-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8602-142">RELATED LINKS</span></span>
