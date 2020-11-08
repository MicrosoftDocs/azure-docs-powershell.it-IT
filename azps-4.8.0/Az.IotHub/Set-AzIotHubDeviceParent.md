---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189702"
---
# <span data-ttu-id="c6707-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="c6707-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="c6707-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6707-102">SYNOPSIS</span></span>
<span data-ttu-id="c6707-103">Imposta il dispositivo padre del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="c6707-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="c6707-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6707-104">SYNTAX</span></span>

### <span data-ttu-id="c6707-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6707-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6707-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c6707-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6707-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c6707-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6707-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6707-108">DESCRIPTION</span></span>
<span data-ttu-id="c6707-109">Imposta il dispositivo padre del dispositivo non Edge specificato.</span><span class="sxs-lookup"><span data-stu-id="c6707-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="c6707-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6707-110">EXAMPLES</span></span>

### <span data-ttu-id="c6707-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6707-111">Example 1</span></span>
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

## <span data-ttu-id="c6707-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6707-112">PARAMETERS</span></span>

### <span data-ttu-id="c6707-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6707-113">-DefaultProfile</span></span>
<span data-ttu-id="c6707-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6707-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6707-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c6707-115">-DeviceId</span></span>
<span data-ttu-id="c6707-116">ID del dispositivo non Edge.</span><span class="sxs-lookup"><span data-stu-id="c6707-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="c6707-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c6707-117">-Force</span></span>
<span data-ttu-id="c6707-118">Sovrascrive il dispositivo padre del dispositivo non Edge.</span><span class="sxs-lookup"><span data-stu-id="c6707-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="c6707-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6707-119">-InputObject</span></span>
<span data-ttu-id="c6707-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="c6707-120">IotHub object</span></span>

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

### <span data-ttu-id="c6707-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c6707-121">-IotHubName</span></span>
<span data-ttu-id="c6707-122">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="c6707-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c6707-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="c6707-123">-ParentDeviceId</span></span>
<span data-ttu-id="c6707-124">ID del dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="c6707-124">Id of edge device.</span></span>

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

### <span data-ttu-id="c6707-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6707-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6707-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c6707-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c6707-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6707-127">-ResourceId</span></span>
<span data-ttu-id="c6707-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="c6707-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c6707-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c6707-129">-Confirm</span></span>
<span data-ttu-id="c6707-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6707-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6707-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6707-131">-WhatIf</span></span>
<span data-ttu-id="c6707-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6707-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6707-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6707-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6707-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6707-134">CommonParameters</span></span>
<span data-ttu-id="c6707-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6707-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6707-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6707-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6707-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6707-137">INPUTS</span></span>

### <span data-ttu-id="c6707-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c6707-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c6707-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6707-139">System.String</span></span>

## <span data-ttu-id="c6707-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6707-140">OUTPUTS</span></span>

### <span data-ttu-id="c6707-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="c6707-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="c6707-142">Note</span><span class="sxs-lookup"><span data-stu-id="c6707-142">NOTES</span></span>

## <span data-ttu-id="c6707-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6707-143">RELATED LINKS</span></span>