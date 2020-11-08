---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203717"
---
# <span data-ttu-id="fe2c7-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="fe2c7-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="fe2c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2c7-103">Eseguire una query su un hub molto usando un potente linguaggio simile a SQL.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="fe2c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe2c7-104">SYNTAX</span></span>

### <span data-ttu-id="fe2c7-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe2c7-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe2c7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe2c7-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe2c7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fe2c7-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe2c7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe2c7-108">DESCRIPTION</span></span>
<span data-ttu-id="fe2c7-109">Eseguire una query su un hub molto usato con una potente lingua simile a SQL per recuperare le informazioni riguardanti i gemelli di dispositivi e moduli, i processi e il routing dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="fe2c7-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-languagePer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="fe2c7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe2c7-111">EXAMPLES</span></span>

### <span data-ttu-id="fe2c7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fe2c7-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="fe2c7-113">Eseguire una query su tutti i dati dei dispositivi Twin in un hub di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="fe2c7-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fe2c7-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="fe2c7-115">Query Top 2 Module dati Twin su un dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="fe2c7-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe2c7-116">PARAMETERS</span></span>

### <span data-ttu-id="fe2c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2c7-117">-DefaultProfile</span></span>
<span data-ttu-id="fe2c7-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe2c7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe2c7-119">-InputObject</span></span>
<span data-ttu-id="fe2c7-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="fe2c7-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2c7-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fe2c7-121">-IotHubName</span></span>
<span data-ttu-id="fe2c7-122">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="fe2c7-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2c7-123">-Query</span><span class="sxs-lookup"><span data-stu-id="fe2c7-123">-Query</span></span>
<span data-ttu-id="fe2c7-124">Query utente da eseguire.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-124">User query to be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe2c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe2c7-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fe2c7-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2c7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2c7-127">-ResourceId</span></span>
<span data-ttu-id="fe2c7-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="fe2c7-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2c7-129">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="fe2c7-129">-Top</span></span>
<span data-ttu-id="fe2c7-130">Numero massimo di elementi da restituire.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="fe2c7-131">Per impostazione predefinita, la query non ha un limite.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-131">By default query has no cap.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe2c7-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe2c7-132">-Confirm</span></span>
<span data-ttu-id="fe2c7-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe2c7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe2c7-134">-WhatIf</span></span>
<span data-ttu-id="fe2c7-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe2c7-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe2c7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2c7-137">CommonParameters</span></span>
<span data-ttu-id="fe2c7-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2c7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2c7-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2c7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2c7-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe2c7-140">INPUTS</span></span>

### <span data-ttu-id="fe2c7-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fe2c7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fe2c7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fe2c7-142">System.String</span></span>

## <span data-ttu-id="fe2c7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe2c7-143">OUTPUTS</span></span>

### <span data-ttu-id="fe2c7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fe2c7-144">System.String</span></span>

## <span data-ttu-id="fe2c7-145">Note</span><span class="sxs-lookup"><span data-stu-id="fe2c7-145">NOTES</span></span>

## <span data-ttu-id="fe2c7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe2c7-146">RELATED LINKS</span></span>
