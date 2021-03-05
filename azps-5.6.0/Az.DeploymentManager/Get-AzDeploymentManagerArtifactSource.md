---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 819fb3427ae59291c6b6d78a9ce93ee4e519ee13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966366"
---
# <span data-ttu-id="0afc9-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0afc9-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="0afc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afc9-102">SYNOPSIS</span></span>

<span data-ttu-id="0afc9-103">Ottiene l'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0afc9-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="0afc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0afc9-104">SYNTAX</span></span>

### <span data-ttu-id="0afc9-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0afc9-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0afc9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0afc9-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0afc9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0afc9-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0afc9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0afc9-108">DESCRIPTION</span></span>
<span data-ttu-id="0afc9-109">Il cmdlet **Get-AzDeploymentManagerArtifactSource** ottiene un'origine dell'elemento e restituisce un oggetto che rappresenta tale origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0afc9-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="0afc9-110">Specificare l'origine dell'elemento in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0afc9-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="0afc9-111">In alternativa, è possibile specificare l'oggetto ArtifactSource o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0afc9-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="0afc9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0afc9-112">EXAMPLES</span></span>

### <span data-ttu-id="0afc9-113">Esempio 1: Ottenere un'origine dell'elemento</span><span class="sxs-lookup"><span data-stu-id="0afc9-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="0afc9-114">Questo comando ottiene un'origine dell'elemento denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0afc9-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="0afc9-115">Esempio 2: Ottenere un'origine dell'elemento usando l'identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="0afc9-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="0afc9-116">Questo comando ottiene un'origine dell'elemento denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0afc9-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="0afc9-117">Esempio 3: Ottenere un'origine dell'elemento usando un oggetto restituito da New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0afc9-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="0afc9-118">Questo comando ottiene un'origine dell'elemento il cui nome e GruppoSocietà Risorse corrispondono, rispettivamente, alle proprietà Name e ResourceGroupName dell'$artifactSourceObject risorsa.</span><span class="sxs-lookup"><span data-stu-id="0afc9-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="0afc9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0afc9-119">PARAMETERS</span></span>

### <span data-ttu-id="0afc9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afc9-120">-DefaultProfile</span></span>
<span data-ttu-id="0afc9-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0afc9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0afc9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0afc9-122">-InputObject</span></span>
<span data-ttu-id="0afc9-123">Oggetto Origine elemento.</span><span class="sxs-lookup"><span data-stu-id="0afc9-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="0afc9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0afc9-124">-Name</span></span>
<span data-ttu-id="0afc9-125">Nome dell'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0afc9-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="0afc9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afc9-126">-ResourceGroupName</span></span>
<span data-ttu-id="0afc9-127">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0afc9-127">The resource group.</span></span>

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

### <span data-ttu-id="0afc9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0afc9-128">-ResourceId</span></span>
<span data-ttu-id="0afc9-129">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0afc9-129">The resource identifier.</span></span>

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

### <span data-ttu-id="0afc9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afc9-130">CommonParameters</span></span>
<span data-ttu-id="0afc9-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afc9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afc9-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0afc9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afc9-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="0afc9-133">INPUTS</span></span>

### <span data-ttu-id="0afc9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0afc9-134">System.String</span></span>

### <span data-ttu-id="0afc9-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0afc9-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="0afc9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0afc9-136">OUTPUTS</span></span>

### <span data-ttu-id="0afc9-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0afc9-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="0afc9-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="0afc9-138">NOTES</span></span>

## <span data-ttu-id="0afc9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0afc9-139">RELATED LINKS</span></span>
