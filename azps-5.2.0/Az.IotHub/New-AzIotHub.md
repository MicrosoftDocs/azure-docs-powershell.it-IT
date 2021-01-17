---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 392f9362df1cafdb6c047020b3381a7b16320607
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331864"
---
# <span data-ttu-id="4113d-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="4113d-101">New-AzIotHub</span></span>

## <span data-ttu-id="4113d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4113d-102">SYNOPSIS</span></span>
<span data-ttu-id="4113d-103">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="4113d-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="4113d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4113d-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4113d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4113d-105">DESCRIPTION</span></span>
<span data-ttu-id="4113d-106">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="4113d-106">Creates a new IotHub.</span></span>
<span data-ttu-id="4113d-107">Puoi creare IotHub con le proprietà predefinite o specificare le proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="4113d-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="4113d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4113d-108">EXAMPLES</span></span>

### <span data-ttu-id="4113d-109">Esempio 1 creare un nuovo IotHub con le proprietà predefinite</span><span class="sxs-lookup"><span data-stu-id="4113d-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="4113d-110">Crea una nuova IotHub denominata "myiothub" dell'USK "S1", capacità 1 e posizione "northeurope" inclusa con i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="4113d-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="4113d-111">Esempio 2 creare un nuovo IotHub con la MaxDeliveryCount della coda CloudToDevice impostata su 20</span><span class="sxs-lookup"><span data-stu-id="4113d-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="4113d-112">Crea una nuova IotHub denominata "myiothub" della SKU "S1", capacità 1 e posizione "northeurope" con le proprietà di input avanzate rappresentate da $properties.</span><span class="sxs-lookup"><span data-stu-id="4113d-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="4113d-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-SkuName "S1"-unità 1-location "northeurope"-properties $properties</span><span class="sxs-lookup"><span data-stu-id="4113d-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="4113d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4113d-114">PARAMETERS</span></span>

### <span data-ttu-id="4113d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4113d-115">-DefaultProfile</span></span>
<span data-ttu-id="4113d-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4113d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4113d-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4113d-117">-Location</span></span>
<span data-ttu-id="4113d-118">Posizione in cui deve essere creato il mozzo.</span><span class="sxs-lookup"><span data-stu-id="4113d-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="4113d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4113d-119">-Name</span></span>
<span data-ttu-id="4113d-120">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="4113d-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="4113d-121">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="4113d-121">-Properties</span></span>
<span data-ttu-id="4113d-122">Proprietà dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="4113d-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="4113d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4113d-123">-ResourceGroupName</span></span>
<span data-ttu-id="4113d-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4113d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4113d-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4113d-125">-SkuName</span></span>
<span data-ttu-id="4113d-126">Nome dell'USK</span><span class="sxs-lookup"><span data-stu-id="4113d-126">Name of the sku</span></span>

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

### <span data-ttu-id="4113d-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="4113d-127">-Tag</span></span>
<span data-ttu-id="4113d-128">Tag di istanza Hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="4113d-128">IoT hub instance tags.</span></span> <span data-ttu-id="4113d-129">Elenco delle proprietà in coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4113d-129">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="4113d-130">-Unità</span><span class="sxs-lookup"><span data-stu-id="4113d-130">-Units</span></span>
<span data-ttu-id="4113d-131">Numero di unità</span><span class="sxs-lookup"><span data-stu-id="4113d-131">Number of units</span></span>

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

### <span data-ttu-id="4113d-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4113d-132">-Confirm</span></span>
<span data-ttu-id="4113d-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4113d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4113d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4113d-134">-WhatIf</span></span>
<span data-ttu-id="4113d-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4113d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4113d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4113d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4113d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4113d-137">CommonParameters</span></span>
<span data-ttu-id="4113d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4113d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4113d-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4113d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4113d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4113d-140">INPUTS</span></span>

### <span data-ttu-id="4113d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4113d-141">System.String</span></span>

## <span data-ttu-id="4113d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4113d-142">OUTPUTS</span></span>

### <span data-ttu-id="4113d-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4113d-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="4113d-144">Note</span><span class="sxs-lookup"><span data-stu-id="4113d-144">NOTES</span></span>

## <span data-ttu-id="4113d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4113d-145">RELATED LINKS</span></span>
