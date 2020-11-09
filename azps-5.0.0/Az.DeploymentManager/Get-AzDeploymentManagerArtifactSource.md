---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297247"
---
# <span data-ttu-id="a69eb-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a69eb-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="a69eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a69eb-102">SYNOPSIS</span></span>

<span data-ttu-id="a69eb-103">Ottiene l'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a69eb-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="a69eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a69eb-104">SYNTAX</span></span>

### <span data-ttu-id="a69eb-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a69eb-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a69eb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a69eb-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a69eb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a69eb-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a69eb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a69eb-108">DESCRIPTION</span></span>
<span data-ttu-id="a69eb-109">Il cmdlet **Get-AzDeploymentManagerArtifactSource** ottiene un'origine dell'elemento e restituisce un oggetto che rappresenta l'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a69eb-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="a69eb-110">Specificare l'origine dell'elemento per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a69eb-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="a69eb-111">In alternativa, puoi specificare l'oggetto ArtifactSource o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a69eb-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="a69eb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a69eb-112">EXAMPLES</span></span>

### <span data-ttu-id="a69eb-113">Esempio 1: ottenere un'origine dell'elemento</span><span class="sxs-lookup"><span data-stu-id="a69eb-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="a69eb-114">Questo comando ottiene un'origine di elementi denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a69eb-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a69eb-115">Esempio 2: ottenere un'origine dell'elemento usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="a69eb-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="a69eb-116">Questo comando ottiene un'origine di elementi denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a69eb-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a69eb-117">Esempio 3: ottenere un'origine dell'elemento usando un oggetto restituito da New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a69eb-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="a69eb-118">Questo comando ottiene un'origine dell'elemento il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="a69eb-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="a69eb-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a69eb-119">PARAMETERS</span></span>

### <span data-ttu-id="a69eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69eb-120">-DefaultProfile</span></span>
<span data-ttu-id="a69eb-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a69eb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a69eb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a69eb-122">-InputObject</span></span>
<span data-ttu-id="a69eb-123">Oggetto origine elemento.</span><span class="sxs-lookup"><span data-stu-id="a69eb-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="a69eb-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a69eb-124">-Name</span></span>
<span data-ttu-id="a69eb-125">Nome dell'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a69eb-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a69eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="a69eb-127">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="a69eb-127">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a69eb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a69eb-128">-ResourceId</span></span>
<span data-ttu-id="a69eb-129">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a69eb-129">The resource identifier.</span></span>

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

### <span data-ttu-id="a69eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69eb-130">CommonParameters</span></span>
<span data-ttu-id="a69eb-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69eb-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a69eb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69eb-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a69eb-133">INPUTS</span></span>

### <span data-ttu-id="a69eb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a69eb-134">System.String</span></span>

### <span data-ttu-id="a69eb-135">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a69eb-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="a69eb-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a69eb-136">OUTPUTS</span></span>

### <span data-ttu-id="a69eb-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a69eb-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="a69eb-138">Note</span><span class="sxs-lookup"><span data-stu-id="a69eb-138">NOTES</span></span>

## <span data-ttu-id="a69eb-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a69eb-139">RELATED LINKS</span></span>
