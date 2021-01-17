---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c88ee9af5d03b50ed80bf677ccff6e7236668756
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386480"
---
# <span data-ttu-id="f820e-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f820e-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="f820e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f820e-102">SYNOPSIS</span></span>
<span data-ttu-id="f820e-103">Aggiornare un modulo in un dispositivo con un sacco di destinazione in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="f820e-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="f820e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f820e-104">SYNTAX</span></span>

### <span data-ttu-id="f820e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f820e-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f820e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f820e-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f820e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f820e-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f820e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f820e-108">DESCRIPTION</span></span>
<span data-ttu-id="f820e-109">Aggiornare un modulo in un dispositivo con un sacco di destinazione in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="f820e-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="f820e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f820e-110">EXAMPLES</span></span>

### <span data-ttu-id="f820e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f820e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod "shared_private_key"

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

<span data-ttu-id="f820e-112">Aggiornare il tipo di autorizzazione di un modulo dispositivo molto.</span><span class="sxs-lookup"><span data-stu-id="f820e-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="f820e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f820e-113">PARAMETERS</span></span>

### <span data-ttu-id="f820e-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="f820e-114">-AuthMethod</span></span>
<span data-ttu-id="f820e-115">Il tipo di autorizzazione con cui deve essere creata un'entità.</span><span class="sxs-lookup"><span data-stu-id="f820e-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="f820e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f820e-116">-DefaultProfile</span></span>
<span data-ttu-id="f820e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f820e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f820e-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f820e-118">-DeviceId</span></span>
<span data-ttu-id="f820e-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f820e-119">Target Device Id.</span></span>

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

### <span data-ttu-id="f820e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f820e-120">-InputObject</span></span>
<span data-ttu-id="f820e-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="f820e-121">IotHub object</span></span>

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

### <span data-ttu-id="f820e-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f820e-122">-IotHubName</span></span>
<span data-ttu-id="f820e-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="f820e-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f820e-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="f820e-124">-ModuleId</span></span>
<span data-ttu-id="f820e-125">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f820e-125">Target Module Id.</span></span>

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

### <span data-ttu-id="f820e-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="f820e-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="f820e-127">Identificazione personale del certificato autofirmato esplicito da usare per la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="f820e-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="f820e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f820e-128">-ResourceGroupName</span></span>
<span data-ttu-id="f820e-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f820e-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f820e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f820e-130">-ResourceId</span></span>
<span data-ttu-id="f820e-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="f820e-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f820e-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="f820e-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="f820e-133">Identificazione personale del certificato autofirmato esplicito da usare per la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="f820e-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="f820e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f820e-134">-Confirm</span></span>
<span data-ttu-id="f820e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f820e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f820e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f820e-136">-WhatIf</span></span>
<span data-ttu-id="f820e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f820e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f820e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f820e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f820e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f820e-139">CommonParameters</span></span>
<span data-ttu-id="f820e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f820e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f820e-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f820e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f820e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f820e-142">INPUTS</span></span>

### <span data-ttu-id="f820e-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f820e-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f820e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f820e-144">System.String</span></span>

## <span data-ttu-id="f820e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f820e-145">OUTPUTS</span></span>

### <span data-ttu-id="f820e-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="f820e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="f820e-147">Note</span><span class="sxs-lookup"><span data-stu-id="f820e-147">NOTES</span></span>

## <span data-ttu-id="f820e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f820e-148">RELATED LINKS</span></span>