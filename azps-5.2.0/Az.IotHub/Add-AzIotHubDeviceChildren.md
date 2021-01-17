---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338896"
---
# <span data-ttu-id="b24d1-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="b24d1-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="b24d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b24d1-102">SYNOPSIS</span></span>
<span data-ttu-id="b24d1-103">Aggiungere dispositivi non Edge come elementi figlio al dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="b24d1-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="b24d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b24d1-104">SYNTAX</span></span>

### <span data-ttu-id="b24d1-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b24d1-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b24d1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b24d1-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b24d1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b24d1-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b24d1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b24d1-108">DESCRIPTION</span></span>
<span data-ttu-id="b24d1-109">Aggiungere un elenco delimitato da virgole di ID dispositivo non Edge come elementi figlio di un dispositivo Edge specificato.</span><span class="sxs-lookup"><span data-stu-id="b24d1-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="b24d1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b24d1-110">EXAMPLES</span></span>

### <span data-ttu-id="b24d1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b24d1-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="b24d1-112">Aggiungere dispositivi non Edge come elementi figlio al dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="b24d1-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="b24d1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b24d1-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="b24d1-114">Aggiungere dispositivi non Edge come elementi figlio al dispositivo Edge indipendentemente il dispositivo non Edge è già un elemento figlio di un altro dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="b24d1-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="b24d1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b24d1-115">PARAMETERS</span></span>

### <span data-ttu-id="b24d1-116">-Bambini</span><span class="sxs-lookup"><span data-stu-id="b24d1-116">-Children</span></span>
<span data-ttu-id="b24d1-117">L'elenco dei dispositivi secondari (separati da virgole) include solo dispositivi non-Edge.</span><span class="sxs-lookup"><span data-stu-id="b24d1-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b24d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24d1-118">-DefaultProfile</span></span>
<span data-ttu-id="b24d1-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b24d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b24d1-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b24d1-120">-DeviceId</span></span>
<span data-ttu-id="b24d1-121">ID del dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="b24d1-121">Id of edge device.</span></span>

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

### <span data-ttu-id="b24d1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b24d1-122">-Force</span></span>
<span data-ttu-id="b24d1-123">Sovrascrive il dispositivo padre del dispositivo non Edge.</span><span class="sxs-lookup"><span data-stu-id="b24d1-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="b24d1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b24d1-124">-InputObject</span></span>
<span data-ttu-id="b24d1-125">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="b24d1-125">IotHub object</span></span>

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

### <span data-ttu-id="b24d1-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b24d1-126">-IotHubName</span></span>
<span data-ttu-id="b24d1-127">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="b24d1-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b24d1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b24d1-128">-ResourceGroupName</span></span>
<span data-ttu-id="b24d1-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b24d1-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b24d1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b24d1-130">-ResourceId</span></span>
<span data-ttu-id="b24d1-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="b24d1-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b24d1-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b24d1-132">-Confirm</span></span>
<span data-ttu-id="b24d1-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b24d1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b24d1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b24d1-134">-WhatIf</span></span>
<span data-ttu-id="b24d1-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b24d1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b24d1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b24d1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b24d1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24d1-137">CommonParameters</span></span>
<span data-ttu-id="b24d1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24d1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24d1-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b24d1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24d1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b24d1-140">INPUTS</span></span>

### <span data-ttu-id="b24d1-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b24d1-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b24d1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b24d1-142">System.String</span></span>

## <span data-ttu-id="b24d1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b24d1-143">OUTPUTS</span></span>

### <span data-ttu-id="b24d1-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="b24d1-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="b24d1-145">Note</span><span class="sxs-lookup"><span data-stu-id="b24d1-145">NOTES</span></span>

## <span data-ttu-id="b24d1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b24d1-146">RELATED LINKS</span></span>
