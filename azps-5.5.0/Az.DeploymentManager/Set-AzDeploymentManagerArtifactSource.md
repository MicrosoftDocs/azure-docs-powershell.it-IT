---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208603"
---
# <span data-ttu-id="bf112-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bf112-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="bf112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf112-102">SYNOPSIS</span></span>
<span data-ttu-id="bf112-103">Aggiorna l'origine degli elementi.</span><span class="sxs-lookup"><span data-stu-id="bf112-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="bf112-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf112-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf112-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bf112-105">DESCRIPTION</span></span>
<span data-ttu-id="bf112-106">Il cmdlet **Set-AzDeploymentManagerArtifactSource** aggiorna un'origine dell'elemento con l'oggetto di origine dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="bf112-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="bf112-107">Il cmdlet restituisce l'oggetto ArtifactSource aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bf112-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="bf112-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf112-108">EXAMPLES</span></span>

### <span data-ttu-id="bf112-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bf112-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="bf112-110">Questo comando aggiorna un'origine dell'elemento il cui nome e GruppoSocietà Risorse corrispondono, rispettivamente, alle proprietà Name e ResourceGroupName dell'$artifactSourceObject risorsa.</span><span class="sxs-lookup"><span data-stu-id="bf112-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="bf112-111">L'origine dell'elemento verrebbe aggiornata alle proprietà impostate nel $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="bf112-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="bf112-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf112-112">PARAMETERS</span></span>

### <span data-ttu-id="bf112-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf112-113">-DefaultProfile</span></span>
<span data-ttu-id="bf112-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf112-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf112-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf112-115">-InputObject</span></span>
<span data-ttu-id="bf112-116">Oggetto di origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="bf112-116">The artifact source object.</span></span>

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

### <span data-ttu-id="bf112-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf112-117">-Confirm</span></span>
<span data-ttu-id="bf112-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf112-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf112-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf112-119">-WhatIf</span></span>
<span data-ttu-id="bf112-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf112-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf112-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf112-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf112-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf112-122">CommonParameters</span></span>
<span data-ttu-id="bf112-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf112-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf112-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bf112-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf112-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="bf112-125">INPUTS</span></span>

### <span data-ttu-id="bf112-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bf112-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="bf112-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf112-127">OUTPUTS</span></span>

### <span data-ttu-id="bf112-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bf112-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="bf112-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="bf112-129">NOTES</span></span>

## <span data-ttu-id="bf112-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf112-130">RELATED LINKS</span></span>
