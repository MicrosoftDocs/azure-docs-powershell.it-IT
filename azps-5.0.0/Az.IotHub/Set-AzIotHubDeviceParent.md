---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203710"
---
# <span data-ttu-id="ad0d4-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="ad0d4-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="ad0d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0d4-103">Imposta il dispositivo padre del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="ad0d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad0d4-104">SYNTAX</span></span>

### <span data-ttu-id="ad0d4-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad0d4-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad0d4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ad0d4-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad0d4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ad0d4-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad0d4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad0d4-108">DESCRIPTION</span></span>
<span data-ttu-id="ad0d4-109">Imposta il dispositivo padre del dispositivo non Edge specificato.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="ad0d4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad0d4-110">EXAMPLES</span></span>

### <span data-ttu-id="ad0d4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad0d4-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="ad0d4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad0d4-112">PARAMETERS</span></span>

### <span data-ttu-id="ad0d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0d4-113">-DefaultProfile</span></span>
<span data-ttu-id="ad0d4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad0d4-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ad0d4-115">-DeviceId</span></span>
<span data-ttu-id="ad0d4-116">ID del dispositivo non Edge.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="ad0d4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ad0d4-117">-Force</span></span>
<span data-ttu-id="ad0d4-118">Sovrascrive il dispositivo padre del dispositivo non Edge.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="ad0d4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad0d4-119">-InputObject</span></span>
<span data-ttu-id="ad0d4-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="ad0d4-120">IotHub object</span></span>

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

### <span data-ttu-id="ad0d4-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ad0d4-121">-IotHubName</span></span>
<span data-ttu-id="ad0d4-122">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="ad0d4-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ad0d4-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="ad0d4-123">-ParentDeviceId</span></span>
<span data-ttu-id="ad0d4-124">ID del dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-124">Id of edge device.</span></span>

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

### <span data-ttu-id="ad0d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad0d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad0d4-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ad0d4-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ad0d4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad0d4-127">-ResourceId</span></span>
<span data-ttu-id="ad0d4-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="ad0d4-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ad0d4-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad0d4-129">-Confirm</span></span>
<span data-ttu-id="ad0d4-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad0d4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad0d4-131">-WhatIf</span></span>
<span data-ttu-id="ad0d4-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad0d4-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad0d4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0d4-134">CommonParameters</span></span>
<span data-ttu-id="ad0d4-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad0d4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0d4-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad0d4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0d4-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad0d4-137">INPUTS</span></span>

### <span data-ttu-id="ad0d4-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ad0d4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ad0d4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ad0d4-139">System.String</span></span>

## <span data-ttu-id="ad0d4-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad0d4-140">OUTPUTS</span></span>

### <span data-ttu-id="ad0d4-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="ad0d4-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="ad0d4-142">Note</span><span class="sxs-lookup"><span data-stu-id="ad0d4-142">NOTES</span></span>

## <span data-ttu-id="ad0d4-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad0d4-143">RELATED LINKS</span></span>
