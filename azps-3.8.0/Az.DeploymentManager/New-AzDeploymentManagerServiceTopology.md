---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022341"
---
# <span data-ttu-id="85764-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="85764-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="85764-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85764-102">SYNOPSIS</span></span>
<span data-ttu-id="85764-103">Crea una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="85764-103">Creates a service topology.</span></span>

## <span data-ttu-id="85764-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85764-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85764-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85764-105">DESCRIPTION</span></span>
<span data-ttu-id="85764-106">Il cmdlet **New-AzDeploymentManagerServiceTopology** crea una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="85764-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="85764-107">Puoi modificare l'oggetto ServiceTopology restituito localmente e quindi applicare le modifiche alla topologia usando il cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="85764-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="85764-108">Oggetto restituito</span><span class="sxs-lookup"><span data-stu-id="85764-108">The returned object</span></span> 

<span data-ttu-id="85764-109">L'oggetto restituito ha un campo ResourceId a cui è possibile fare riferimento in una risorsa di implementazione per indicare che i servizi dichiarati in questa topologia di servizio verrebbero distribuiti nell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="85764-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="85764-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85764-110">EXAMPLES</span></span>

### <span data-ttu-id="85764-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85764-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="85764-112">Questo cmdlet crea una nuova topologia di servizio nel gruppo di risorse ContosoResourceGroup con il nome ContosoServiceTopology e in location Central US.</span><span class="sxs-lookup"><span data-stu-id="85764-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="85764-113">L'origine dell'elemento ResourceId indica che gli elementi necessari per le definizioni delle unità di servizio in questa topologia devono essere letti dall'origine dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="85764-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="85764-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="85764-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="85764-115">Questo cmdlet crea una nuova topologia di servizio nel gruppo di risorse ContosoResourceGroup con il nome ContosoServiceTopology e in location Central US.</span><span class="sxs-lookup"><span data-stu-id="85764-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="85764-116">L'assenza di un riferimento di origine dell'elemento indica che gli elementi necessari per le definizioni delle unità di servizio in questa topologia verrebbero forniti come URI SAS assoluti nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="85764-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="85764-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85764-117">PARAMETERS</span></span>

### <span data-ttu-id="85764-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="85764-118">-ArtifactSourceId</span></span>
<span data-ttu-id="85764-119">Identificatore dell'origine dell'elemento, in cui vengono archiviati gli elementi che costituiscono la topologia.</span><span class="sxs-lookup"><span data-stu-id="85764-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="85764-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85764-120">-DefaultProfile</span></span>
<span data-ttu-id="85764-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85764-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85764-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="85764-122">-Location</span></span>
<span data-ttu-id="85764-123">Posizione della topologia.</span><span class="sxs-lookup"><span data-stu-id="85764-123">The location of the topology.</span></span>

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

### <span data-ttu-id="85764-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="85764-124">-Name</span></span>
<span data-ttu-id="85764-125">Nome della topologia.</span><span class="sxs-lookup"><span data-stu-id="85764-125">The name of the topology.</span></span>

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

### <span data-ttu-id="85764-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85764-126">-ResourceGroupName</span></span>
<span data-ttu-id="85764-127">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="85764-127">The resource group.</span></span>

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

### <span data-ttu-id="85764-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="85764-128">-Tag</span></span>
<span data-ttu-id="85764-129">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="85764-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="85764-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85764-130">-Confirm</span></span>
<span data-ttu-id="85764-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85764-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85764-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85764-132">-WhatIf</span></span>
<span data-ttu-id="85764-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85764-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85764-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85764-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85764-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85764-135">CommonParameters</span></span>
<span data-ttu-id="85764-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85764-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85764-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85764-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85764-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85764-138">INPUTS</span></span>

### <span data-ttu-id="85764-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="85764-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="85764-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85764-140">OUTPUTS</span></span>

### <span data-ttu-id="85764-141">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="85764-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="85764-142">Note</span><span class="sxs-lookup"><span data-stu-id="85764-142">NOTES</span></span>

## <span data-ttu-id="85764-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85764-143">RELATED LINKS</span></span>
