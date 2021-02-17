---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196511"
---
# <span data-ttu-id="c6cbd-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c6cbd-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="c6cbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="c6cbd-103">Crea una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-103">Creates a service topology.</span></span>

## <span data-ttu-id="c6cbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6cbd-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6cbd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c6cbd-105">DESCRIPTION</span></span>
<span data-ttu-id="c6cbd-106">Il cmdlet **New-AzDeploymentManagerServiceTopology** crea una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="c6cbd-107">È possibile modificare l'oggetto ServiceTopology restituito in locale e quindi applicare le modifiche alla topologia usando il cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="c6cbd-108">Oggetto restituito</span><span class="sxs-lookup"><span data-stu-id="c6cbd-108">The returned object</span></span> 

<span data-ttu-id="c6cbd-109">L'oggetto restituito ha un campo ResourceId a cui è possibile fare riferimento in una risorsa di implementazione per indicare che i servizi dichiarati in questa topologia di servizio verranno distribuiti nell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="c6cbd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6cbd-110">EXAMPLES</span></span>

### <span data-ttu-id="c6cbd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c6cbd-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="c6cbd-112">Questo cmdlet crea una nuova topologia di servizio nel gruppo di risorse ContosoResourceGroup con il nome ContosoServiceTopology e nella posizione Stati Uniti centrale.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="c6cbd-113">ResourceId dell'origine dell'elemento indica che gli elementi necessari per le definizioni di unità di servizio in questa topologia devono essere letti dall'origine dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="c6cbd-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c6cbd-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="c6cbd-115">Questo cmdlet crea una nuova topologia di servizio nel gruppo di risorse ContosoResourceGroup con il nome ContosoServiceTopology e nella posizione Stati Uniti centrale.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="c6cbd-116">L'assenza di un riferimento all'origine di un elemento indica che gli elementi necessari per le definizioni di unità di servizio in questa topologia verranno forniti come URI di firma di accesso condiviso assoluti nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="c6cbd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6cbd-117">PARAMETERS</span></span>

### <span data-ttu-id="c6cbd-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="c6cbd-118">-ArtifactSourceId</span></span>
<span data-ttu-id="c6cbd-119">Identificatore dell'origine dell'elemento, in cui vengono archiviati gli elementi che costituiscono la topologia.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="c6cbd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6cbd-120">-DefaultProfile</span></span>
<span data-ttu-id="c6cbd-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6cbd-122">-Location</span><span class="sxs-lookup"><span data-stu-id="c6cbd-122">-Location</span></span>
<span data-ttu-id="c6cbd-123">Posizione della topologia.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-123">The location of the topology.</span></span>

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

### <span data-ttu-id="c6cbd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c6cbd-124">-Name</span></span>
<span data-ttu-id="c6cbd-125">Nome della topologia.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-125">The name of the topology.</span></span>

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

### <span data-ttu-id="c6cbd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6cbd-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6cbd-127">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-127">The resource group.</span></span>

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

### <span data-ttu-id="c6cbd-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6cbd-128">-Tag</span></span>
<span data-ttu-id="c6cbd-129">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-129">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6cbd-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6cbd-130">-Confirm</span></span>
<span data-ttu-id="c6cbd-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6cbd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6cbd-132">-WhatIf</span></span>
<span data-ttu-id="c6cbd-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6cbd-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6cbd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6cbd-135">CommonParameters</span></span>
<span data-ttu-id="c6cbd-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6cbd-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6cbd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6cbd-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="c6cbd-138">INPUTS</span></span>

### <span data-ttu-id="c6cbd-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c6cbd-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c6cbd-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6cbd-140">OUTPUTS</span></span>

### <span data-ttu-id="c6cbd-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c6cbd-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c6cbd-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="c6cbd-142">NOTES</span></span>

## <span data-ttu-id="c6cbd-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6cbd-143">RELATED LINKS</span></span>
