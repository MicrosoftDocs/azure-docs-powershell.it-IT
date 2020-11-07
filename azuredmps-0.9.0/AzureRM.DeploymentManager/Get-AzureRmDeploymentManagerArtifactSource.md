---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685244"
---
# <span data-ttu-id="553d8-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="553d8-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="553d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="553d8-102">SYNOPSIS</span></span>
<span data-ttu-id="553d8-103">Ottiene un'origine di elementi.</span><span class="sxs-lookup"><span data-stu-id="553d8-103">Gets an artifact source.</span></span>

## <span data-ttu-id="553d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="553d8-104">SYNTAX</span></span>

### <span data-ttu-id="553d8-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="553d8-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="553d8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="553d8-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="553d8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="553d8-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="553d8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="553d8-108">DESCRIPTION</span></span>
<span data-ttu-id="553d8-109">Il cmdlet **Get-AzureRmDeploymentManagerArtifactSource** ottiene un'origine dell'elemento e restituisce un oggetto che rappresenta l'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="553d8-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="553d8-110">Specificare l'origine dell'elemento per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="553d8-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="553d8-111">In alternativa, puoi specificare l'oggetto ArtifactSource o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="553d8-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="553d8-112">Puoi modificare l'oggetto localmente e quindi applicare le modifiche apportate all'origine dell'elemento usando il cmdlet Set-AzureRmDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="553d8-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="553d8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="553d8-113">EXAMPLES</span></span>

### <span data-ttu-id="553d8-114">Esempio 1: ottenere un'origine dell'elemento</span><span class="sxs-lookup"><span data-stu-id="553d8-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="553d8-115">Questo comando ottiene un'origine di elementi denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="553d8-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="553d8-116">Esempio 2: ottenere un'origine dell'elemento usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="553d8-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="553d8-117">Questo comando ottiene un'origine di elementi denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="553d8-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="553d8-118">Esempio 3: ottenere un'origine dell'elemento usando un oggetto restituito da New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="553d8-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="553d8-119">Questo comando ottiene un'origine dell'elemento il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="553d8-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="553d8-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="553d8-120">PARAMETERS</span></span>

### <span data-ttu-id="553d8-121">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="553d8-121">-ArtifactSource</span></span>
<span data-ttu-id="553d8-122">Oggetto origine elemento.</span><span class="sxs-lookup"><span data-stu-id="553d8-122">Artifact Source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="553d8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553d8-123">-DefaultProfile</span></span>
<span data-ttu-id="553d8-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="553d8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553d8-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="553d8-125">-Name</span></span>
<span data-ttu-id="553d8-126">Nome dell'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="553d8-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="553d8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="553d8-127">-ResourceGroupName</span></span>
<span data-ttu-id="553d8-128">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="553d8-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="553d8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="553d8-129">-ResourceId</span></span>
<span data-ttu-id="553d8-130">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="553d8-130">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="553d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553d8-131">CommonParameters</span></span>
<span data-ttu-id="553d8-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="553d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553d8-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="553d8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553d8-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="553d8-134">INPUTS</span></span>

### <span data-ttu-id="553d8-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="553d8-135">None</span></span>

## <span data-ttu-id="553d8-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="553d8-136">OUTPUTS</span></span>

### <span data-ttu-id="553d8-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="553d8-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="553d8-138">Note</span><span class="sxs-lookup"><span data-stu-id="553d8-138">NOTES</span></span>

## <span data-ttu-id="553d8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="553d8-139">RELATED LINKS</span></span>

[<span data-ttu-id="553d8-140">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="553d8-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="553d8-141">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="553d8-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="553d8-142">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="553d8-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)