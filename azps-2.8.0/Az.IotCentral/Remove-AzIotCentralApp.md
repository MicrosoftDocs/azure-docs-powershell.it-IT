---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 6043daf907331b970744daffe716e4bbdbc1d6f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674262"
---
# <span data-ttu-id="72026-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="72026-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="72026-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72026-102">SYNOPSIS</span></span>
<span data-ttu-id="72026-103">Elimina un'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="72026-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="72026-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72026-104">SYNTAX</span></span>

### <span data-ttu-id="72026-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72026-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72026-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72026-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72026-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="72026-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72026-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72026-108">DESCRIPTION</span></span>
<span data-ttu-id="72026-109">Elimina un'applicazione centrale di un sacco esistente.</span><span class="sxs-lookup"><span data-stu-id="72026-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="72026-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72026-110">EXAMPLES</span></span>

### <span data-ttu-id="72026-111">Esempio 1 applicazione centrale Elimina e un sacco</span><span class="sxs-lookup"><span data-stu-id="72026-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="72026-112">Elimina l'applicazione centrale disponibile.</span><span class="sxs-lookup"><span data-stu-id="72026-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="72026-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72026-113">PARAMETERS</span></span>

### <span data-ttu-id="72026-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72026-114">-AsJob</span></span>
<span data-ttu-id="72026-115">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="72026-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="72026-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72026-116">-DefaultProfile</span></span>
<span data-ttu-id="72026-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72026-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72026-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72026-118">-InputObject</span></span>
<span data-ttu-id="72026-119">Oggetto di input dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="72026-119">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="72026-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="72026-120">-Name</span></span>
<span data-ttu-id="72026-121">Nome della risorsa dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="72026-121">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="72026-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72026-122">-PassThru</span></span>
<span data-ttu-id="72026-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="72026-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="72026-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72026-124">-ResourceGroupName</span></span>
<span data-ttu-id="72026-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72026-125">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="72026-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72026-126">-ResourceId</span></span>
<span data-ttu-id="72026-127">ID risorsa centrale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="72026-127">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="72026-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72026-128">-Confirm</span></span>
<span data-ttu-id="72026-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72026-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72026-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72026-130">-WhatIf</span></span>
<span data-ttu-id="72026-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72026-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72026-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72026-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72026-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72026-133">CommonParameters</span></span>
<span data-ttu-id="72026-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72026-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72026-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72026-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72026-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72026-136">INPUTS</span></span>

### <span data-ttu-id="72026-137">System. String</span><span class="sxs-lookup"><span data-stu-id="72026-137">System.String</span></span>

### <span data-ttu-id="72026-138">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="72026-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="72026-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72026-139">OUTPUTS</span></span>

### <span data-ttu-id="72026-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72026-140">System.Boolean</span></span>

## <span data-ttu-id="72026-141">Note</span><span class="sxs-lookup"><span data-stu-id="72026-141">NOTES</span></span>

## <span data-ttu-id="72026-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72026-142">RELATED LINKS</span></span>
