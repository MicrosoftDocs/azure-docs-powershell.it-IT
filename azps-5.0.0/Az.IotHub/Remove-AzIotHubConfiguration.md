---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193292"
---
# <span data-ttu-id="70261-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="70261-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="70261-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70261-102">SYNOPSIS</span></span>
<span data-ttu-id="70261-103">Eliminare una configurazione del dispositivo molto.</span><span class="sxs-lookup"><span data-stu-id="70261-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="70261-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70261-104">SYNTAX</span></span>

### <span data-ttu-id="70261-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70261-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70261-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="70261-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70261-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="70261-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70261-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70261-108">DESCRIPTION</span></span>
<span data-ttu-id="70261-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="70261-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="70261-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70261-110">EXAMPLES</span></span>

### <span data-ttu-id="70261-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="70261-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="70261-112">Eliminare una configurazione del dispositivo molto.</span><span class="sxs-lookup"><span data-stu-id="70261-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="70261-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70261-113">PARAMETERS</span></span>

### <span data-ttu-id="70261-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70261-114">-DefaultProfile</span></span>
<span data-ttu-id="70261-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70261-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70261-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70261-116">-InputObject</span></span>
<span data-ttu-id="70261-117">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="70261-117">IotHub object</span></span>

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

### <span data-ttu-id="70261-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="70261-118">-IotHubName</span></span>
<span data-ttu-id="70261-119">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="70261-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="70261-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="70261-120">-Name</span></span>
<span data-ttu-id="70261-121">Identificatore per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="70261-121">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70261-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70261-122">-PassThru</span></span>
<span data-ttu-id="70261-123">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="70261-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="70261-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="70261-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="70261-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70261-125">-ResourceGroupName</span></span>
<span data-ttu-id="70261-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="70261-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="70261-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70261-127">-ResourceId</span></span>
<span data-ttu-id="70261-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="70261-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="70261-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="70261-129">-Confirm</span></span>
<span data-ttu-id="70261-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70261-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70261-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70261-131">-WhatIf</span></span>
<span data-ttu-id="70261-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70261-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70261-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70261-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70261-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70261-134">CommonParameters</span></span>
<span data-ttu-id="70261-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70261-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70261-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70261-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70261-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70261-137">INPUTS</span></span>

### <span data-ttu-id="70261-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="70261-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="70261-139">System. String</span><span class="sxs-lookup"><span data-stu-id="70261-139">System.String</span></span>

## <span data-ttu-id="70261-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70261-140">OUTPUTS</span></span>

### <span data-ttu-id="70261-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70261-141">System.Boolean</span></span>

## <span data-ttu-id="70261-142">Note</span><span class="sxs-lookup"><span data-stu-id="70261-142">NOTES</span></span>

## <span data-ttu-id="70261-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70261-143">RELATED LINKS</span></span>