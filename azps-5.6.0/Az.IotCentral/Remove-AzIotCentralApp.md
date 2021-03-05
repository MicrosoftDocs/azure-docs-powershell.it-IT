---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 29a53b49e579ab337c2345a15c86c4c27aaffe8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997973"
---
# <span data-ttu-id="e53d1-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e53d1-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="e53d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e53d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e53d1-103">Elimina un'applicazione ioT central.</span><span class="sxs-lookup"><span data-stu-id="e53d1-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="e53d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e53d1-104">SYNTAX</span></span>

### <span data-ttu-id="e53d1-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e53d1-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53d1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e53d1-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53d1-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="e53d1-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e53d1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e53d1-108">DESCRIPTION</span></span>
<span data-ttu-id="e53d1-109">Elimina un'applicazione ioT central esistente.</span><span class="sxs-lookup"><span data-stu-id="e53d1-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="e53d1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e53d1-110">EXAMPLES</span></span>

### <span data-ttu-id="e53d1-111">Esempio 1: Eliminazione e applicazione centrale IoT</span><span class="sxs-lookup"><span data-stu-id="e53d1-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="e53d1-112">Elimina l'applicazione centrale IoT fornita.</span><span class="sxs-lookup"><span data-stu-id="e53d1-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="e53d1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e53d1-113">PARAMETERS</span></span>

### <span data-ttu-id="e53d1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e53d1-114">-AsJob</span></span>
<span data-ttu-id="e53d1-115">Eseguire il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="e53d1-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="e53d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53d1-116">-DefaultProfile</span></span>
<span data-ttu-id="e53d1-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e53d1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e53d1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e53d1-118">-InputObject</span></span>
<span data-ttu-id="e53d1-119">Oggetto di input Iot Central Application.</span><span class="sxs-lookup"><span data-stu-id="e53d1-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e53d1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e53d1-120">-Name</span></span>
<span data-ttu-id="e53d1-121">Nome della risorsa applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="e53d1-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e53d1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e53d1-122">-PassThru</span></span>
<span data-ttu-id="e53d1-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e53d1-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e53d1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e53d1-124">-ResourceGroupName</span></span>
<span data-ttu-id="e53d1-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e53d1-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e53d1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e53d1-126">-ResourceId</span></span>
<span data-ttu-id="e53d1-127">ID risorsa applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="e53d1-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e53d1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e53d1-128">-Confirm</span></span>
<span data-ttu-id="e53d1-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e53d1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e53d1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e53d1-130">-WhatIf</span></span>
<span data-ttu-id="e53d1-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e53d1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e53d1-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e53d1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e53d1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53d1-133">CommonParameters</span></span>
<span data-ttu-id="e53d1-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e53d1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53d1-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e53d1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53d1-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="e53d1-136">INPUTS</span></span>

### <span data-ttu-id="e53d1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e53d1-137">System.String</span></span>

### <span data-ttu-id="e53d1-138">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="e53d1-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="e53d1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e53d1-139">OUTPUTS</span></span>

### <span data-ttu-id="e53d1-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e53d1-140">System.Boolean</span></span>

## <span data-ttu-id="e53d1-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e53d1-141">NOTES</span></span>

## <span data-ttu-id="e53d1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e53d1-142">RELATED LINKS</span></span>
