---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022333"
---
# <span data-ttu-id="e2fe5-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e2fe5-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="e2fe5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="e2fe5-103">Aggiorna l'origine degli artefatti.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="e2fe5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2fe5-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2fe5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="e2fe5-106">Il cmdlet **set-AzDeploymentManagerArtifactSource** aggiorna un'origine dell'elemento con l'oggetto origine dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="e2fe5-107">Il cmdlet restituisce l'oggetto ArtifactSource aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="e2fe5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2fe5-108">EXAMPLES</span></span>

### <span data-ttu-id="e2fe5-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e2fe5-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="e2fe5-110">Questo comando aggiorna un'origine dell'elemento il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="e2fe5-111">L'origine dell'elemento verrà aggiornata alle proprietà impostate nel $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="e2fe5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2fe5-112">PARAMETERS</span></span>

### <span data-ttu-id="e2fe5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2fe5-113">-DefaultProfile</span></span>
<span data-ttu-id="e2fe5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2fe5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2fe5-115">-InputObject</span></span>
<span data-ttu-id="e2fe5-116">Oggetto origine elemento.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2fe5-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2fe5-117">-Confirm</span></span>
<span data-ttu-id="e2fe5-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2fe5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2fe5-119">-WhatIf</span></span>
<span data-ttu-id="e2fe5-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2fe5-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2fe5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2fe5-122">CommonParameters</span></span>
<span data-ttu-id="e2fe5-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2fe5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2fe5-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2fe5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2fe5-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2fe5-125">INPUTS</span></span>

### <span data-ttu-id="e2fe5-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e2fe5-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="e2fe5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2fe5-127">OUTPUTS</span></span>

### <span data-ttu-id="e2fe5-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e2fe5-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="e2fe5-129">Note</span><span class="sxs-lookup"><span data-stu-id="e2fe5-129">NOTES</span></span>

## <span data-ttu-id="e2fe5-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2fe5-130">RELATED LINKS</span></span>
