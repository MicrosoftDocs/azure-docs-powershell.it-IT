---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203898"
---
# <span data-ttu-id="a21ce-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="a21ce-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="a21ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a21ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a21ce-103">Richiamare il processo di failover per l'hub IoT nell'area geografica di ripristino di emergenza associata a un'altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="a21ce-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="a21ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a21ce-104">SYNTAX</span></span>

### <span data-ttu-id="a21ce-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a21ce-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a21ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a21ce-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a21ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a21ce-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a21ce-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a21ce-108">DESCRIPTION</span></span>
<span data-ttu-id="a21ce-109">Attiverà il failover dell'hub IoT nella posizione secondaria.</span><span class="sxs-lookup"><span data-stu-id="a21ce-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="a21ce-110">Questa azione causerà tempi di insod>e perdite di telemetria nella soluzione.</span><span class="sxs-lookup"><span data-stu-id="a21ce-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="a21ce-111">Si tratta di un'operazione a esecuzione lunga che può richiedere alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="a21ce-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="a21ce-112">Esercitarsi con cautela quando lo si usa.</span><span class="sxs-lookup"><span data-stu-id="a21ce-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="a21ce-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a21ce-113">EXAMPLES</span></span>

### <span data-ttu-id="a21ce-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a21ce-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a21ce-115">Avvio del processo di failover dell'hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a21ce-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a21ce-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a21ce-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="a21ce-117">Avvio del processo di failover dell'hub IoT "myiothub" in background.</span><span class="sxs-lookup"><span data-stu-id="a21ce-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="a21ce-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a21ce-118">PARAMETERS</span></span>

### <span data-ttu-id="a21ce-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a21ce-119">-AsJob</span></span>
<span data-ttu-id="a21ce-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a21ce-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a21ce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a21ce-121">-DefaultProfile</span></span>
<span data-ttu-id="a21ce-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a21ce-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a21ce-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a21ce-123">-InputObject</span></span>
<span data-ttu-id="a21ce-124">Oggetto Hub Iot</span><span class="sxs-lookup"><span data-stu-id="a21ce-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="a21ce-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a21ce-125">-Name</span></span>
<span data-ttu-id="a21ce-126">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="a21ce-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a21ce-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a21ce-127">-PassThru</span></span>
<span data-ttu-id="a21ce-128">Consente di restituire l'oggetto booleano.</span><span class="sxs-lookup"><span data-stu-id="a21ce-128">Allows to return the boolean object.</span></span> <span data-ttu-id="a21ce-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a21ce-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a21ce-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a21ce-130">-ResourceGroupName</span></span>
<span data-ttu-id="a21ce-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a21ce-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a21ce-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a21ce-132">-ResourceId</span></span>
<span data-ttu-id="a21ce-133">ID risorsa hub Iot</span><span class="sxs-lookup"><span data-stu-id="a21ce-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="a21ce-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a21ce-134">-Confirm</span></span>
<span data-ttu-id="a21ce-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a21ce-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a21ce-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a21ce-136">-WhatIf</span></span>
<span data-ttu-id="a21ce-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a21ce-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a21ce-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a21ce-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a21ce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21ce-139">CommonParameters</span></span>
<span data-ttu-id="a21ce-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a21ce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21ce-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a21ce-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21ce-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="a21ce-142">INPUTS</span></span>

### <span data-ttu-id="a21ce-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a21ce-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a21ce-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a21ce-144">System.String</span></span>

## <span data-ttu-id="a21ce-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a21ce-145">OUTPUTS</span></span>

### <span data-ttu-id="a21ce-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a21ce-146">System.Boolean</span></span>

## <span data-ttu-id="a21ce-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="a21ce-147">NOTES</span></span>

## <span data-ttu-id="a21ce-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a21ce-148">RELATED LINKS</span></span>
