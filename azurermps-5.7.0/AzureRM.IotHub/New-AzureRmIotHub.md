---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: c24f8f9e95db65b464da6586d9e3499358fc3edd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521038"
---
# <span data-ttu-id="7446c-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="7446c-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="7446c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7446c-102">SYNOPSIS</span></span>
<span data-ttu-id="7446c-103">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="7446c-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7446c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7446c-104">SYNTAX</span></span>

```
New-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7446c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7446c-105">DESCRIPTION</span></span>
<span data-ttu-id="7446c-106">Crea un nuovo IotHub.</span><span class="sxs-lookup"><span data-stu-id="7446c-106">Creates a new IotHub.</span></span>
<span data-ttu-id="7446c-107">Puoi creare IotHub con le proprietà predefinite o specificare l'input proerties.</span><span class="sxs-lookup"><span data-stu-id="7446c-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="7446c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7446c-108">EXAMPLES</span></span>

### <span data-ttu-id="7446c-109">Esempio 1 creare un nuovo IotHub con le proprietà predefinite</span><span class="sxs-lookup"><span data-stu-id="7446c-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="7446c-110">Crea un nuovo IotHub denominato "myiothub" dell'USK "S1", capacità 1 e posizione "northeurope".</span><span class="sxs-lookup"><span data-stu-id="7446c-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="7446c-111">Esempio 2 creare un nuovo IotHub con la MaxDeliveryCount della coda CloudtoDevice impostata su 20</span><span class="sxs-lookup"><span data-stu-id="7446c-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="7446c-112">Crea una nuova IotHub denominata "myiothub" della SKU "S1", capacità 1 e posizione "northeurope" con le proprietà di input avanzate rappresentate da $properties.</span><span class="sxs-lookup"><span data-stu-id="7446c-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>

<span data-ttu-id="7446c-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-SkuName "S1"-unità 1-location "northeurope"-properties $properties</span><span class="sxs-lookup"><span data-stu-id="7446c-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="7446c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7446c-114">PARAMETERS</span></span>

### <span data-ttu-id="7446c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7446c-115">-DefaultProfile</span></span>
<span data-ttu-id="7446c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7446c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7446c-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7446c-117">-Location</span></span>
<span data-ttu-id="7446c-118">Posizione in cui deve essere creato il mozzo.</span><span class="sxs-lookup"><span data-stu-id="7446c-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7446c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7446c-119">-Name</span></span>
<span data-ttu-id="7446c-120">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="7446c-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="7446c-121">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="7446c-121">-Properties</span></span>
<span data-ttu-id="7446c-122">Proprietà dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="7446c-122">Properties of the IoT hub.</span></span> 

```yaml
Type: PSIotHubInputProperties
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7446c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7446c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7446c-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7446c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7446c-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7446c-125">-SkuName</span></span>
<span data-ttu-id="7446c-126">Nome dell'USK</span><span class="sxs-lookup"><span data-stu-id="7446c-126">Name of the sku</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: (All)
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7446c-127">-Unità</span><span class="sxs-lookup"><span data-stu-id="7446c-127">-Units</span></span>
<span data-ttu-id="7446c-128">Numero di unità</span><span class="sxs-lookup"><span data-stu-id="7446c-128">Number of units</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7446c-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7446c-129">-Confirm</span></span>
<span data-ttu-id="7446c-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7446c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7446c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7446c-131">-WhatIf</span></span>
<span data-ttu-id="7446c-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7446c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7446c-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7446c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7446c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7446c-134">CommonParameters</span></span>
<span data-ttu-id="7446c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7446c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7446c-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7446c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7446c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7446c-137">INPUTS</span></span>

### <span data-ttu-id="7446c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7446c-138">System.String</span></span>
<span data-ttu-id="7446c-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSku System. Int64 Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubInputProperties</span><span class="sxs-lookup"><span data-stu-id="7446c-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku System.Int64 Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties</span></span>

## <span data-ttu-id="7446c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7446c-140">OUTPUTS</span></span>

### <span data-ttu-id="7446c-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7446c-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="7446c-142">Note</span><span class="sxs-lookup"><span data-stu-id="7446c-142">NOTES</span></span>

## <span data-ttu-id="7446c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7446c-143">RELATED LINKS</span></span>

