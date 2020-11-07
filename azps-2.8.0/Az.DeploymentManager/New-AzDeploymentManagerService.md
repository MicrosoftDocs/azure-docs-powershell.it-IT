---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: 50708e5faebff03e63b0b6330bac66c2c409adda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674620"
---
# <span data-ttu-id="1e1dd-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="1e1dd-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="1e1dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1dd-103">Crea un servizio nella topologia di servizio specificata.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="1e1dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e1dd-104">SYNTAX</span></span>

### <span data-ttu-id="1e1dd-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e1dd-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e1dd-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="1e1dd-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e1dd-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="1e1dd-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e1dd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e1dd-108">DESCRIPTION</span></span>
<span data-ttu-id="1e1dd-109">Il cmdlet **New-AzDeploymentManagerService** crea un servizio in una topologia di servizio e restituisce un oggetto che rappresenta tale servizio.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="1e1dd-110">Specificare il servizio in base al nome, alla topologia del servizio e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="1e1dd-111">Il cmdlet restituisce un oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="1e1dd-112">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al servizio usando il cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="1e1dd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e1dd-113">EXAMPLES</span></span>

### <span data-ttu-id="1e1dd-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e1dd-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="1e1dd-115">Crea un nuovo servizio con nome ContosoService1 in topologia di servizio ContosoServiceTopology nel gruppo risorse ContosoResourceGroup, nella posizione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="1e1dd-116">La proprietà TargetLocation indica che il servizio ContosoService1 deve essere distribuito nell'area est degli Stati Uniti nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="1e1dd-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e1dd-117">PARAMETERS</span></span>

### <span data-ttu-id="1e1dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e1dd-118">-DefaultProfile</span></span>
<span data-ttu-id="1e1dd-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e1dd-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1e1dd-120">-Location</span></span>
<span data-ttu-id="1e1dd-121">Posizione della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1dd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e1dd-122">-Name</span></span>
<span data-ttu-id="1e1dd-123">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e1dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e1dd-125">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1dd-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="1e1dd-126">-ServiceTopologyId</span></span>
<span data-ttu-id="1e1dd-127">Identificatore della risorsa della topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1dd-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="1e1dd-128">-ServiceTopologyName</span></span>
<span data-ttu-id="1e1dd-129">Nome della topologia del servizio a cui appartiene il servizio.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-129">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1dd-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="1e1dd-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="1e1dd-131">Oggetto topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1dd-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e1dd-132">-Tag</span></span>
<span data-ttu-id="1e1dd-133">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1dd-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="1e1dd-134">-TargetLocation</span></span>
<span data-ttu-id="1e1dd-135">Determina la posizione in cui verranno distribuite le risorse del servizio.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1dd-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e1dd-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="1e1dd-137">Determina la sottoscrizione a cui verranno distribuite le risorse del servizio.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1dd-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e1dd-138">-Confirm</span></span>
<span data-ttu-id="1e1dd-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e1dd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e1dd-140">-WhatIf</span></span>
<span data-ttu-id="1e1dd-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e1dd-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e1dd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1dd-143">CommonParameters</span></span>
<span data-ttu-id="1e1dd-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e1dd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1dd-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e1dd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1dd-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e1dd-146">INPUTS</span></span>

### <span data-ttu-id="1e1dd-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e1dd-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1e1dd-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e1dd-148">OUTPUTS</span></span>

### <span data-ttu-id="1e1dd-149">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="1e1dd-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="1e1dd-150">Note</span><span class="sxs-lookup"><span data-stu-id="1e1dd-150">NOTES</span></span>

## <span data-ttu-id="1e1dd-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e1dd-151">RELATED LINKS</span></span>