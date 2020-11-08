---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201237"
---
# <span data-ttu-id="397eb-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="397eb-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="397eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="397eb-102">SYNOPSIS</span></span>
<span data-ttu-id="397eb-103">Creare un modulo in un dispositivo con un sacco di destinazione in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="397eb-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="397eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="397eb-104">SYNTAX</span></span>

### <span data-ttu-id="397eb-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="397eb-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="397eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="397eb-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="397eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="397eb-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="397eb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="397eb-108">DESCRIPTION</span></span>
<span data-ttu-id="397eb-109">Creare un modulo in un dispositivo con un sacco di destinazione con tipo di autorizzazione diverso in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="397eb-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="397eb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="397eb-110">EXAMPLES</span></span>

### <span data-ttu-id="397eb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="397eb-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod shared_private_key

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="397eb-112">Creare un modulo in un dispositivo di destinazione con l'autorizzazione predefinita (chiave privata condivisa).</span><span class="sxs-lookup"><span data-stu-id="397eb-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="397eb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="397eb-113">PARAMETERS</span></span>

### <span data-ttu-id="397eb-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="397eb-114">-AuthMethod</span></span>
<span data-ttu-id="397eb-115">Il tipo di autorizzazione con cui deve essere creata un'entità.</span><span class="sxs-lookup"><span data-stu-id="397eb-115">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="397eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="397eb-116">-DefaultProfile</span></span>
<span data-ttu-id="397eb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="397eb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="397eb-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="397eb-118">-DeviceId</span></span>
<span data-ttu-id="397eb-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="397eb-119">Target Device Id.</span></span>

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

### <span data-ttu-id="397eb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="397eb-120">-InputObject</span></span>
<span data-ttu-id="397eb-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="397eb-121">IotHub object</span></span>

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

### <span data-ttu-id="397eb-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="397eb-122">-IotHubName</span></span>
<span data-ttu-id="397eb-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="397eb-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="397eb-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="397eb-124">-ModuleId</span></span>
<span data-ttu-id="397eb-125">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="397eb-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="397eb-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="397eb-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="397eb-127">Identificazione personale del certificato autofirmato esplicito da usare per la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="397eb-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="397eb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="397eb-128">-ResourceGroupName</span></span>
<span data-ttu-id="397eb-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="397eb-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="397eb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="397eb-130">-ResourceId</span></span>
<span data-ttu-id="397eb-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="397eb-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="397eb-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="397eb-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="397eb-133">Identificazione personale del certificato autofirmato esplicito da usare per la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="397eb-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="397eb-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="397eb-134">-Confirm</span></span>
<span data-ttu-id="397eb-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="397eb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="397eb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="397eb-136">-WhatIf</span></span>
<span data-ttu-id="397eb-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="397eb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="397eb-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="397eb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="397eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397eb-139">CommonParameters</span></span>
<span data-ttu-id="397eb-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="397eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397eb-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="397eb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397eb-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="397eb-142">INPUTS</span></span>

### <span data-ttu-id="397eb-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="397eb-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="397eb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="397eb-144">System.String</span></span>

## <span data-ttu-id="397eb-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="397eb-145">OUTPUTS</span></span>

### <span data-ttu-id="397eb-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="397eb-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="397eb-147">Note</span><span class="sxs-lookup"><span data-stu-id="397eb-147">NOTES</span></span>

## <span data-ttu-id="397eb-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="397eb-148">RELATED LINKS</span></span>