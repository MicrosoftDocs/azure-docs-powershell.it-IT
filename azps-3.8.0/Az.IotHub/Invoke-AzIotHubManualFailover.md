---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021779"
---
# <span data-ttu-id="ed5a3-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="ed5a3-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="ed5a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed5a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5a3-103">Richiamare il processo di failover per l'hub molto per l'area di ripristino di emergenza Geo-associata.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="ed5a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed5a3-104">SYNTAX</span></span>

### <span data-ttu-id="ed5a3-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed5a3-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5a3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed5a3-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5a3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ed5a3-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5a3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed5a3-108">DESCRIPTION</span></span>
<span data-ttu-id="ed5a3-109">Attiverà il failover del tuo hub per la posizione secondaria.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="ed5a3-110">Questa azione causerà il tempo e la perdita di telemetria alla tua soluzione.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="ed5a3-111">Si tratta di un'operazione a esecuzione prolungata che potrebbe richiedere alcuni minuti per terminare.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="ed5a3-112">Per esercitarsi con cautela durante l'uso.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="ed5a3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed5a3-113">EXAMPLES</span></span>

### <span data-ttu-id="ed5a3-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed5a3-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ed5a3-115">Avviare il processo di failover dell'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="ed5a3-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="ed5a3-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ed5a3-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="ed5a3-117">Avviare il processo di failover dell'hub "myiothub" in background.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="ed5a3-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed5a3-118">PARAMETERS</span></span>

### <span data-ttu-id="ed5a3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed5a3-119">-AsJob</span></span>
<span data-ttu-id="ed5a3-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ed5a3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed5a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5a3-121">-DefaultProfile</span></span>
<span data-ttu-id="ed5a3-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed5a3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed5a3-123">-InputObject</span></span>
<span data-ttu-id="ed5a3-124">Oggetto Hub molto</span><span class="sxs-lookup"><span data-stu-id="ed5a3-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="ed5a3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed5a3-125">-Name</span></span>
<span data-ttu-id="ed5a3-126">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="ed5a3-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ed5a3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed5a3-127">-PassThru</span></span>
<span data-ttu-id="ed5a3-128">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-128">Allows to return the boolean object.</span></span> <span data-ttu-id="ed5a3-129">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed5a3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5a3-130">-ResourceGroupName</span></span>
<span data-ttu-id="ed5a3-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ed5a3-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ed5a3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed5a3-132">-ResourceId</span></span>
<span data-ttu-id="ed5a3-133">ID risorsa Hub</span><span class="sxs-lookup"><span data-stu-id="ed5a3-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="ed5a3-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed5a3-134">-Confirm</span></span>
<span data-ttu-id="ed5a3-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5a3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5a3-136">-WhatIf</span></span>
<span data-ttu-id="ed5a3-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed5a3-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed5a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5a3-139">CommonParameters</span></span>
<span data-ttu-id="ed5a3-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed5a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5a3-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed5a3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5a3-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed5a3-142">INPUTS</span></span>

### <span data-ttu-id="ed5a3-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ed5a3-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ed5a3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ed5a3-144">System.String</span></span>

## <span data-ttu-id="ed5a3-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed5a3-145">OUTPUTS</span></span>

### <span data-ttu-id="ed5a3-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed5a3-146">System.Boolean</span></span>

## <span data-ttu-id="ed5a3-147">Note</span><span class="sxs-lookup"><span data-stu-id="ed5a3-147">NOTES</span></span>

## <span data-ttu-id="ed5a3-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed5a3-148">RELATED LINKS</span></span>
