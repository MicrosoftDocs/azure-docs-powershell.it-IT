---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200063"
---
# <span data-ttu-id="2aa07-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="2aa07-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="2aa07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aa07-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa07-103">Eliminare una distribuzione Edge IoT.</span><span class="sxs-lookup"><span data-stu-id="2aa07-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="2aa07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2aa07-104">SYNTAX</span></span>

### <span data-ttu-id="2aa07-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2aa07-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa07-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2aa07-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa07-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2aa07-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aa07-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2aa07-108">DESCRIPTION</span></span>
<span data-ttu-id="2aa07-109">Per https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="2aa07-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="2aa07-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2aa07-110">EXAMPLES</span></span>

### <span data-ttu-id="2aa07-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2aa07-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="2aa07-112">Eliminare una distribuzione Edge IoT.</span><span class="sxs-lookup"><span data-stu-id="2aa07-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="2aa07-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2aa07-113">PARAMETERS</span></span>

### <span data-ttu-id="2aa07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa07-114">-DefaultProfile</span></span>
<span data-ttu-id="2aa07-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa07-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aa07-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aa07-116">-InputObject</span></span>
<span data-ttu-id="2aa07-117">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="2aa07-117">IotHub object</span></span>

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

### <span data-ttu-id="2aa07-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2aa07-118">-IotHubName</span></span>
<span data-ttu-id="2aa07-119">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="2aa07-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2aa07-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2aa07-120">-Name</span></span>
<span data-ttu-id="2aa07-121">Identificatore per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2aa07-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="2aa07-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aa07-122">-PassThru</span></span>
<span data-ttu-id="2aa07-123">Consente di restituire l'oggetto booleano.</span><span class="sxs-lookup"><span data-stu-id="2aa07-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="2aa07-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2aa07-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2aa07-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aa07-125">-ResourceGroupName</span></span>
<span data-ttu-id="2aa07-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2aa07-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2aa07-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa07-127">-ResourceId</span></span>
<span data-ttu-id="2aa07-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="2aa07-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2aa07-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2aa07-129">-Confirm</span></span>
<span data-ttu-id="2aa07-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aa07-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aa07-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa07-131">-WhatIf</span></span>
<span data-ttu-id="2aa07-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2aa07-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aa07-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2aa07-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aa07-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa07-134">CommonParameters</span></span>
<span data-ttu-id="2aa07-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa07-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa07-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa07-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa07-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="2aa07-137">INPUTS</span></span>

### <span data-ttu-id="2aa07-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2aa07-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2aa07-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2aa07-139">System.String</span></span>

## <span data-ttu-id="2aa07-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2aa07-140">OUTPUTS</span></span>

### <span data-ttu-id="2aa07-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2aa07-141">System.Boolean</span></span>

## <span data-ttu-id="2aa07-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="2aa07-142">NOTES</span></span>

## <span data-ttu-id="2aa07-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2aa07-143">RELATED LINKS</span></span>
