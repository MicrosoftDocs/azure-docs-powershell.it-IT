---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 71f5e9805467bc285b991a9aa4ee289b3d807729
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987838"
---
# <span data-ttu-id="e3a9a-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="e3a9a-101">New-AzIotHub</span></span>

## <span data-ttu-id="e3a9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a9a-103">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="e3a9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3a9a-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a9a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a9a-106">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-106">Creates a new IotHub.</span></span>
<span data-ttu-id="e3a9a-107">È possibile creare iotHub con le proprietà predefinite o specificare le proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="e3a9a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3a9a-108">EXAMPLES</span></span>

### <span data-ttu-id="e3a9a-109">Esempio 1: Creare un nuovo IotHub con proprietà predefinite</span><span class="sxs-lookup"><span data-stu-id="e3a9a-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="e3a9a-110">Crea un nuovo IotHub denominato "myiothub" della sku "S1", della capacità 1 e della posizione "nordeuropea" inclusa in Tag.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="e3a9a-111">Esempio 2: Creare un nuovo iotHub con MaxDeliveryCount della coda CloudToDevice impostata su 20</span><span class="sxs-lookup"><span data-stu-id="e3a9a-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="e3a9a-112">Crea un nuovo IotHub denominato "myiothub" della sku "S1", della capacità 1 e della posizione "nordeuropea" con proprietà di input avanzate rappresentate da $properties.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="e3a9a-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span><span class="sxs-lookup"><span data-stu-id="e3a9a-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="e3a9a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3a9a-114">PARAMETERS</span></span>

### <span data-ttu-id="e3a9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a9a-115">-DefaultProfile</span></span>
<span data-ttu-id="e3a9a-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e3a9a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3a9a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e3a9a-117">-Location</span></span>
<span data-ttu-id="e3a9a-118">Posizione in cui deve essere creato l'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="e3a9a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e3a9a-119">-Name</span></span>
<span data-ttu-id="e3a9a-120">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="e3a9a-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="e3a9a-121">-Properties</span><span class="sxs-lookup"><span data-stu-id="e3a9a-121">-Properties</span></span>
<span data-ttu-id="e3a9a-122">Proprietà dell'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="e3a9a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a9a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3a9a-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e3a9a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e3a9a-125">-SKUName</span><span class="sxs-lookup"><span data-stu-id="e3a9a-125">-SkuName</span></span>
<span data-ttu-id="e3a9a-126">Nome della sKU</span><span class="sxs-lookup"><span data-stu-id="e3a9a-126">Name of the sku</span></span>

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

### <span data-ttu-id="e3a9a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3a9a-127">-Tag</span></span>
<span data-ttu-id="e3a9a-128">Tag di istanza dell'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-128">IoT hub instance tags.</span></span> <span data-ttu-id="e3a9a-129">Il bag delle proprietà in coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-129">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a9a-130">-Unità</span><span class="sxs-lookup"><span data-stu-id="e3a9a-130">-Units</span></span>
<span data-ttu-id="e3a9a-131">Numero di unità</span><span class="sxs-lookup"><span data-stu-id="e3a9a-131">Number of units</span></span>

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

### <span data-ttu-id="e3a9a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3a9a-132">-Confirm</span></span>
<span data-ttu-id="e3a9a-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a9a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a9a-134">-WhatIf</span></span>
<span data-ttu-id="e3a9a-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a9a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a9a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a9a-137">CommonParameters</span></span>
<span data-ttu-id="e3a9a-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a9a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a9a-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a9a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a9a-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3a9a-140">INPUTS</span></span>

### <span data-ttu-id="e3a9a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e3a9a-141">System.String</span></span>

## <span data-ttu-id="e3a9a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3a9a-142">OUTPUTS</span></span>

### <span data-ttu-id="e3a9a-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e3a9a-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e3a9a-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3a9a-144">NOTES</span></span>

## <span data-ttu-id="e3a9a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3a9a-145">RELATED LINKS</span></span>
