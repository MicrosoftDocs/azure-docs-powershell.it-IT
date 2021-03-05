---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 9d5d79f65adbcab7ce61ad125e78189d0f84f9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980590"
---
# <span data-ttu-id="f2711-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f2711-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="f2711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2711-102">SYNOPSIS</span></span>
<span data-ttu-id="f2711-103">Aggiorna l'origine degli elementi.</span><span class="sxs-lookup"><span data-stu-id="f2711-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="f2711-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2711-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2711-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2711-105">DESCRIPTION</span></span>
<span data-ttu-id="f2711-106">Il cmdlet **Set-AzDeploymentManagerArtifactSource** aggiorna un'origine dell'elemento con l'oggetto di origine dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="f2711-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="f2711-107">Il cmdlet restituisce l'oggetto ArtifactSource aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f2711-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="f2711-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2711-108">EXAMPLES</span></span>

### <span data-ttu-id="f2711-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2711-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="f2711-110">Questo comando aggiorna un'origine dell'elemento il cui nome e GruppoSocietà Risorse corrispondono, rispettivamente, alle proprietà Name e ResourceGroupName dell'$artifactSourceObject risorsa.</span><span class="sxs-lookup"><span data-stu-id="f2711-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="f2711-111">L'origine dell'elemento verrebbe aggiornata alle proprietà impostate nel $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="f2711-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="f2711-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2711-112">PARAMETERS</span></span>

### <span data-ttu-id="f2711-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2711-113">-DefaultProfile</span></span>
<span data-ttu-id="f2711-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2711-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2711-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2711-115">-InputObject</span></span>
<span data-ttu-id="f2711-116">Oggetto di origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f2711-116">The artifact source object.</span></span>

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

### <span data-ttu-id="f2711-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2711-117">-Confirm</span></span>
<span data-ttu-id="f2711-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2711-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2711-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2711-119">-WhatIf</span></span>
<span data-ttu-id="f2711-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2711-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2711-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2711-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2711-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2711-122">CommonParameters</span></span>
<span data-ttu-id="f2711-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2711-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2711-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2711-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2711-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2711-125">INPUTS</span></span>

### <span data-ttu-id="f2711-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f2711-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="f2711-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2711-127">OUTPUTS</span></span>

### <span data-ttu-id="f2711-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f2711-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="f2711-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2711-129">NOTES</span></span>

## <span data-ttu-id="f2711-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2711-130">RELATED LINKS</span></span>
