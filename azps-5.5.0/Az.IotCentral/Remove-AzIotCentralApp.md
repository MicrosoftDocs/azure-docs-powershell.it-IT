---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 5a9dc29d9cb078473a777279c5bdb648a1b9388e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187639"
---
# <span data-ttu-id="b4ef3-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="b4ef3-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="b4ef3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ef3-103">Elimina un'applicazione ioT central.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="b4ef3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4ef3-104">SYNTAX</span></span>

### <span data-ttu-id="b4ef3-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4ef3-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ef3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4ef3-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ef3-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4ef3-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ef3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4ef3-108">DESCRIPTION</span></span>
<span data-ttu-id="b4ef3-109">Elimina un'applicazione centrale IoT esistente.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="b4ef3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4ef3-110">EXAMPLES</span></span>

### <span data-ttu-id="b4ef3-111">Esempio 1: Eliminazione e applicazione centrale IoT</span><span class="sxs-lookup"><span data-stu-id="b4ef3-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="b4ef3-112">Elimina l'applicazione centrale IoT fornita.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="b4ef3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4ef3-113">PARAMETERS</span></span>

### <span data-ttu-id="b4ef3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4ef3-114">-AsJob</span></span>
<span data-ttu-id="b4ef3-115">Eseguire il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="b4ef3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ef3-116">-DefaultProfile</span></span>
<span data-ttu-id="b4ef3-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ef3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4ef3-118">-InputObject</span></span>
<span data-ttu-id="b4ef3-119">Oggetto di input Iot Central Application.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-119">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="b4ef3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b4ef3-120">-Name</span></span>
<span data-ttu-id="b4ef3-121">Nome della risorsa applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-121">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="b4ef3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4ef3-122">-PassThru</span></span>
<span data-ttu-id="b4ef3-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b4ef3-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b4ef3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ef3-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4ef3-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-125">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="b4ef3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4ef3-126">-ResourceId</span></span>
<span data-ttu-id="b4ef3-127">ID risorsa applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-127">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="b4ef3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4ef3-128">-Confirm</span></span>
<span data-ttu-id="b4ef3-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ef3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ef3-130">-WhatIf</span></span>
<span data-ttu-id="b4ef3-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4ef3-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ef3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ef3-133">CommonParameters</span></span>
<span data-ttu-id="b4ef3-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ef3-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4ef3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ef3-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4ef3-136">INPUTS</span></span>

### <span data-ttu-id="b4ef3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b4ef3-137">System.String</span></span>

### <span data-ttu-id="b4ef3-138">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="b4ef3-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="b4ef3-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4ef3-139">OUTPUTS</span></span>

### <span data-ttu-id="b4ef3-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4ef3-140">System.Boolean</span></span>

## <span data-ttu-id="b4ef3-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4ef3-141">NOTES</span></span>

## <span data-ttu-id="b4ef3-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4ef3-142">RELATED LINKS</span></span>
