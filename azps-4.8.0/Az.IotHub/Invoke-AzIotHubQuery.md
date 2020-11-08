---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192875"
---
# <span data-ttu-id="27048-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="27048-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="27048-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27048-102">SYNOPSIS</span></span>
<span data-ttu-id="27048-103">Eseguire una query su un hub molto usando un potente linguaggio simile a SQL.</span><span class="sxs-lookup"><span data-stu-id="27048-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="27048-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27048-104">SYNTAX</span></span>

### <span data-ttu-id="27048-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27048-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27048-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27048-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27048-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="27048-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27048-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27048-108">DESCRIPTION</span></span>
<span data-ttu-id="27048-109">Eseguire una query su un hub molto usato con una potente lingua simile a SQL per recuperare le informazioni riguardanti i gemelli di dispositivi e moduli, i processi e il routing dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="27048-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="27048-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-languagePer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="27048-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="27048-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27048-111">EXAMPLES</span></span>

### <span data-ttu-id="27048-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27048-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="27048-113">Eseguire una query su tutti i dati dei dispositivi Twin in un hub di Azure.</span><span class="sxs-lookup"><span data-stu-id="27048-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="27048-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="27048-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="27048-115">Query Top 2 Module dati Twin su un dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="27048-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="27048-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27048-116">PARAMETERS</span></span>

### <span data-ttu-id="27048-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27048-117">-DefaultProfile</span></span>
<span data-ttu-id="27048-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27048-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27048-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27048-119">-InputObject</span></span>
<span data-ttu-id="27048-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="27048-120">IotHub object</span></span>

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

### <span data-ttu-id="27048-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="27048-121">-IotHubName</span></span>
<span data-ttu-id="27048-122">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="27048-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="27048-123">-Query</span><span class="sxs-lookup"><span data-stu-id="27048-123">-Query</span></span>
<span data-ttu-id="27048-124">Query utente da eseguire.</span><span class="sxs-lookup"><span data-stu-id="27048-124">User query to be executed.</span></span>

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

### <span data-ttu-id="27048-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27048-125">-ResourceGroupName</span></span>
<span data-ttu-id="27048-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="27048-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="27048-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27048-127">-ResourceId</span></span>
<span data-ttu-id="27048-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="27048-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="27048-129">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="27048-129">-Top</span></span>
<span data-ttu-id="27048-130">Numero massimo di elementi da restituire.</span><span class="sxs-lookup"><span data-stu-id="27048-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="27048-131">Per impostazione predefinita, la query non ha un limite.</span><span class="sxs-lookup"><span data-stu-id="27048-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="27048-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27048-132">-Confirm</span></span>
<span data-ttu-id="27048-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27048-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27048-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27048-134">-WhatIf</span></span>
<span data-ttu-id="27048-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27048-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27048-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27048-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27048-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27048-137">CommonParameters</span></span>
<span data-ttu-id="27048-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27048-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27048-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27048-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27048-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27048-140">INPUTS</span></span>

### <span data-ttu-id="27048-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="27048-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="27048-142">System. String</span><span class="sxs-lookup"><span data-stu-id="27048-142">System.String</span></span>

## <span data-ttu-id="27048-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27048-143">OUTPUTS</span></span>

### <span data-ttu-id="27048-144">System. String</span><span class="sxs-lookup"><span data-stu-id="27048-144">System.String</span></span>

## <span data-ttu-id="27048-145">Note</span><span class="sxs-lookup"><span data-stu-id="27048-145">NOTES</span></span>

## <span data-ttu-id="27048-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27048-146">RELATED LINKS</span></span>
